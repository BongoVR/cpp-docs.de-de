---
title: C-Laufzeitbibliothek zur Threadsteuerung Funktionen | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- _beginthread function
- _endthread function
- threading [C++], controlling threads
- multithreading [C++], controlling threads
- _beginthreadex function
- _endthreadex function
ms.assetid: 39d0529c-c392-4c6f-94f5-105d1e8054e4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4a505bae156edba6798812b807d7ab5c6ea9e396
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="c-run-time-library-functions-for-thread-control"></a>Funktionen der C-Laufzeitbibliothek zur Threadsteuerung
Alle Win32-Programme weisen mindestens einen Thread auf. Jeder Thread kann zusätzliche Threads generieren. Ein Thread kann seine Aufgabe schnell abschließen oder während der gesamten Lebensdauer eines Programms aktiv bleiben.  
  
 Die LIBCMT und MSVCRT C-Laufzeitbibliotheken bieten die folgenden Funktionen für Threaderstellung und Beendigung: [_beginthread, _beginthreadex](../c-runtime-library/reference/beginthread-beginthreadex.md) und [_endthread, _endthreadex](../c-runtime-library/reference/endthread-endthreadex.md).  
  
 Mit der `_beginthread`-Funktion und der `_beginthreadex`-Funktion wird ein neuer Thread erstellt; wenn der Vorgang erfolgreich war, wird ein Threadbezeichner zurückgegeben. Der Thread wird nach abgeschlossener Ausführung automatisch beendet. Er kann sich jedoch durch Aufruf von `_endthread` oder `_endthreadex` auch selbsttätig beenden.  
  
> [!NOTE]
>  Wenn Sie beabsichtigen, C-Laufzeitroutinen von einem Programm aus aufzurufen, das mit Libcmt.lib erstellt wurde, müssen Sie die Threads über die `_beginthread`-Funktion oder über die `_beginthreadex`-Funktion starten. Verwenden Sie nicht die Win32-Funktionen `ExitThread` und `CreateThread`. Bei der Verwendung von `SuspendThread` tritt möglicherweise ein Deadlock auf, wenn mehrere blockierte Threads darauf warten, dass der unterbrochene Thread den Zugriffsvorgang auf eine C-Laufzeitdatenstruktur abschließt.  
  
##  <a name="_core_the__beginthread_function"></a> Die _beginthread und _beginthreadex-Funktion  
 Die `_beginthread`-Funktion und die `_beginthreadex`-Funktion erstellen einen neuen Thread. Ein Thread nutzt den Code und die Datensegmente eines Prozesses gemeinsam mit anderen Threads in diesem Prozess, verfügt jedoch über eigene, eindeutige Registerwerte, Stapelspeicher und eine aktuelle Anweisungsadresse. Das System weist jedem Thread seine bestimmte CPU-Zeit zu, damit alle Threads in einem Prozess gleichzeitig ausgeführt werden können.  
  
 `_beginthread` und `_beginthreadex` ähneln den [CreateThread](http://msdn.microsoft.com/library/windows/desktop/ms682453) -Funktion in der Win32-API, weisen jedoch folgende Unterschiede:  
  
-   Sie initialisieren bestimmte Variablen der C-Laufzeitbibliothek. Dies ist nur von Bedeutung, wenn Sie die C-Laufzeitbibliothek in Threads verwenden.  
  
-   Mit `CreateThread` können Sicherheitsattribute gesteuert werden. Mit dieser Funktion können Sie einen Thread starten, der sich im angehaltenen Status befindet.  
  
 `_beginthread` und `_beginthreadex` geben ein Handle für den neuen Thread zurück, wenn der Vorgang erfolgreich war. Bei einem Fehler wird ein Fehlercode zurückgegeben.  
  
##  <a name="_core_the__endthread_function"></a> Die _endthread und _endthreadex-Funktion  
 Die [_endthread](../c-runtime-library/reference/endthread-endthreadex.md) -Funktion beendet einen Thread erstellt, indem `_beginthread` (und analog `_endthreadex` beendet einen Thread erstellt, indem `_beginthreadex`). Threads werden automatisch beendet, wenn sie abgeschlossen sind. `_endthread` und `_endthreadex` sind zum bedingten Beenden aus einem Thread heraus sinnvoll. Ein für die Kommunikationsverarbeitung verantwortlicher Thread kann z. B. seine Aktivität einstellen, wenn die Steuerung des Kommunikationsanschlusses derzeit nicht möglich ist.  
  
## <a name="see-also"></a>Siehe auch  
 [Multithreading bei C und Win32](../parallel/multithreading-with-c-and-win32.md)