---
title: 'Vorgehensweise: verwenden ein Nachrichtenblockfilters | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- message-block filters, using [Concurrency Runtime]
- using message-block filters [Concurrency Runtime]
ms.assetid: db6b99fb-288d-4477-96dc-b9751772ebb2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 92de322142e56eb9907da2e19d350c3af9c8a7d9
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="how-to-use-a-message-block-filter"></a>Gewusst wie: Verwenden eines Nachrichtenblockfilters
In diesem Dokument wird veranschaulicht, wie mit einer Filterfunktion ermöglicht wird, dass ein asynchroner Nachrichtenblock eine Nachricht auf der Grundlage der Nutzlast dieser Nachricht annimmt oder ablehnt.  
  
 Wenn Sie ein Nachrichtenblockobjekt wie z. B. Erstellen einer [Concurrency:: unbounded_buffer](reference/unbounded-buffer-class.md), [Call](../../parallel/concrt/reference/call-class.md), oder ein [Concurrency:: transformer](../../parallel/concrt/reference/transformer-class.md), können Sie eine angeben*filter-Funktion* , der bestimmt, ob der Nachrichtenblock Nachricht akzeptiert oder eine abgelehnt. Eine Filterfunktion ist eine hilfreiche Möglichkeit, um sicherzustellen, dass nur bestimmte Werte von einem Nachrichtenblock empfangen werden.  
  
 Filterfunktionen sind wichtig, da sie Sie zum Verbinden von Nachrichtenblöcken Formular ermöglichen *Datenflussnetzwerke*. Nachrichtenblöcke in einem Datenflussnetzwerk steuern den Datenfluss, indem sie nur Nachrichten verarbeiten, die bestimmte Kriterien erfüllen. Vergleichen Sie dies mit dem Ablaufsteuerungsmodell, in dem der Datenfluss mit Steuerungsstrukturen, z. B. Bedingungsanweisungen, Schleifen usw., gesteuert wird.  
  
 Dieses Dokument enthält ein einfaches Beispiel für die Verwendung eines Nachrichtenfilters. Zusätzliche Beispiele, mit denen Nachrichtenfilter und das Datenflussmodell Nachrichtenblöcke verbinden, finden Sie unter [Exemplarische Vorgehensweise: Erstellen eines Datenfluss-Agents](../../parallel/concrt/walkthrough-creating-a-dataflow-agent.md) und [Exemplarische Vorgehensweise: Erstellen einer Bildverarbeitungsnetzwerks](../../parallel/concrt/walkthrough-creating-an-image-processing-network.md) .  
  
## <a name="example"></a>Beispiel  
 Betrachten Sie die folgende Funktion `count_primes`, die die grundlegende Verwendung eines Nachrichtenblocks veranschaulicht, der keine eingehenden Nachrichten filtert. Der Nachrichtenblock fügt Primzahlen eine [Std:: vector](../../standard-library/vector-class.md) Objekt. Die `count_primes`-Funktion sendet Zahlen an den Nachrichtenblock, empfängt die Ausgabewerte des Nachrichtenblocks und gibt die Zahlen, die Primzahlen sind, an die Konsole aus.  
  
 [!code-cpp[concrt-primes-filter#1](../../parallel/concrt/codesnippet/cpp/how-to-use-a-message-block-filter_1.cpp)]  
  
 Das `transformer`-Objekt verarbeitet alle Eingabewerte. Es benötigt jedoch nur die Werte, bei denen es sich um Primzahlen handelt. Die Anwendung kann zwar so geschrieben werden kann, dass der Nachrichtenabsender nur Primzahlen sendet, jedoch können die Anforderungen des Nachrichtenempfängers nicht immer bekannt sein.  
  
## <a name="example"></a>Beispiel  
 Die folgende Funktion `count_primes_filter` führt die gleiche Aufgabe wie die `count_primes`-Funktion aus. Das `transformer`-Objekt in dieser Version verwendet jedoch eine Filterfunktion, damit nur die Werte angenommen werden, die Primzahlen sind. Die Funktion, die die Aktion ausführt, empfängt nur Primzahlen. Daher muss sie die `is_prime`-Funktion nicht aufrufen.  
  
 Da das `transformer`-Objekt nur Primzahlen empfängt, kann das `transformer`-Objekt selbst die Primzahlen enthalten. Das bedeutet, dass das `transformer`-Objekt in diesem Beispiel nicht benötigt wird, um dem `vector`-Objekt die Primzahlen hinzuzufügen.  
  
 [!code-cpp[concrt-primes-filter#2](../../parallel/concrt/codesnippet/cpp/how-to-use-a-message-block-filter_2.cpp)]  
  
 Das `transformer`-Objekt verarbeitet jetzt nur die Werte, die Primzahlen sind. Im vorherigen Beispiel verarbeitet das `transformer`-Objekt alle Nachrichten. Daher muss im vorherigen Beispiel die gleiche Anzahl von Nachrichten empfangen werden, wie gesendet wurden. In diesem Beispiel anhand des Ergebnisses der [Concurrency:: Send](reference/concurrency-namespace-functions.md#send) Funktion, um zu bestimmen, wie viele Nachrichten zum Empfangen von der `transformer` Objekt. Die `send`-Funktion gibt `true` zurück, wenn der Nachrichtenpuffer die Nachricht annimmt, und `false`, wenn der Nachrichtenpuffer die Nachricht ablehnt. Daher stimmt die Häufigkeit, mit der der Nachrichtenpuffer die Nachricht annimmt, mit der Anzahl der Primzahlen überein.  
  
## <a name="example"></a>Beispiel  
 Der folgende Code veranschaulicht das vollständige Beispiel. In dem Beispiel werden die `count_primes`-Funktion und die `count_primes_filter`-Funktion aufgerufen.  
  
 [!code-cpp[concrt-primes-filter#3](../../parallel/concrt/codesnippet/cpp/how-to-use-a-message-block-filter_3.cpp)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Kopieren Sie den Beispielcode und fügen Sie ihn in ein Visual Studio-Projekt, oder fügen Sie ihn in eine Datei mit dem Namen `primes-filter.cpp` und dann den folgenden Befehl in eine Visual Studio-Eingabeaufforderungsfenster ausführen.  
  
 **CL.exe/EHsc / Primes-filter.cpp**  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Eine Filterfunktion kann eine Lambda-Funktion, ein Funktionsobjekt oder ein Funktionszeiger sein. Jede Filterfunktion nimmt eines der folgenden Formate an:  
  
```Output  
bool (T)  
bool (T const &)  
```  
  
 Um das unnötige Kopieren von Daten zu vermeiden, verwenden Sie das zweite Format bei einem aggregierten Typ, der anhand des Werts übertragen wird.  
  
## <a name="see-also"></a>Siehe auch  
 [Asynchronous Agents Library](../../parallel/concrt/asynchronous-agents-library.md)   
 [Exemplarische Vorgehensweise: Erstellen eines Datenfluss-Agents](../../parallel/concrt/walkthrough-creating-a-dataflow-agent.md)   
 [Exemplarische Vorgehensweise: Erstellen einer Bildverarbeitungsnetzwerks](../../parallel/concrt/walkthrough-creating-an-image-processing-network.md)   
 [transformer-Klasse](../../parallel/concrt/reference/transformer-class.md)
