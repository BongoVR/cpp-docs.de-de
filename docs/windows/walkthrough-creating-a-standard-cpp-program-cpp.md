---
title: 'Exemplarische Vorgehensweise: Erstellen eines standardmäßigen C++-Programms (C++) | Microsoft Docs'
ms.custom: get-started-article
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- vcfirstapp
- vccreatefirst
dev_langs:
- C++
helpviewer_keywords:
- command-line applications [C++], standard
- standard applications [C++]
ms.assetid: 48217e35-d892-46b7-93e3-f6f0b7e2da35
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f563e318f2defcbf36139f1f6d49e3986db5f946
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="walkthrough-creating-a-standard-c-program-c"></a>Exemplarische Vorgehensweise: Erstellen eines standardmäßigen C++-Programms (C++)
Mit Visual C++ können in der integrierten Entwicklungsumgebung (IDE) von Visual Studio standardmäßige C++-Programme erstellt werden. Durch Ausführen der Schritte in dieser exemplarischen Vorgehensweise können Sie ein Projekt erstellen, dem Projekt eine neue Datei hinzufügen, die Datei bearbeiten, um C++-Code hinzuzufügen und das Programm anschließend mithilfe von [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] kompilieren und ausführen.  
  
 Sie können ein eigenes C++-Programm eingeben oder eines der Beispielprogramme verwenden. Das Beispielprogramm in dieser exemplarischen Vorgehensweise ist eine Konsolenanwendung. Diese Anwendung verwendet die `set` Container in der C++-Standardbibliothek.  
  
 Visual C++ entspricht dem 2003 C++-Standard, wobei folgende wichtigen Ausnahmen: zweistufige Namenssuche, Ausnahmespezifikationen und Export. Darüber hinaus unterstützt Visual C++ mehrere C ++ 0 X-Funktionen, z. B. Lambdas, Auto, Static_assert, Rvalue-Verweise und Extern-Vorlagen.  
  
> [!NOTE]
>  Wenn die Kompatibilität mit dem Standard erforderlich ist, verwenden Sie die **"/ Za"** Compileroption, um Microsoft-Erweiterungen für den Standard zu deaktivieren. Weitere Informationen finden Sie unter [/Za, / Ze (Spracherweiterungen deaktivieren)](../build/reference/za-ze-disable-language-extensions.md).  
  
## <a name="prerequisites"></a>Erforderliche Komponenten  
 Zur Durchführung dieser exemplarischen Vorgehensweise benötigen Sie Grundkenntnisse in C++.  
  
### <a name="to-create-a-project-and-add-a-source-file"></a>So erstellen Sie ein neues Projekt und fügen eine Quelldatei hinzu  
  
1.  Erstellen Sie ein Projekt, zeigen, um **neu** auf die **Datei** Menü, und klicken Sie dann auf **Projekt**.  
  
2.  In der **Visual C++** projekttypenbereich, klicken Sie auf **Win32**, und klicken Sie dann auf **Win32-Konsolenanwendung**.  
  
3.  Geben Sie einen Namen für das Projekt ein.  
  
     Standardmäßig erhält die Lösung, in der das Projekt enthalten ist, den gleichen Namen wie das Projekt. Sie können jedoch auch einen anderen Namen eingeben. Sie können auch einen anderen Speicherort für das Projekt eingeben.  
  
     Klicken Sie auf **OK**, um das Projekt zu erstellen.  
  
4.  In der **Win32-Anwendungsassistenten**, klicken Sie auf **Weiter**Option **leeres Projekt**, und klicken Sie dann auf **Fertig stellen**.  
  
5.  Wenn **Projektmappen-Explorer** nicht angezeigt wird, auf die **Ansicht** Menü klicken Sie auf **Projektmappen-Explorer**.  
  
6.  Fügen Sie dem Projekt folgendermaßen eine neue Quelldatei hinzu:  
  
    1.  In **Projektmappen-Explorer**, mit der rechten Maustaste die **Quelldateien** Ordner, zeigen Sie auf **hinzufügen**, und klicken Sie dann auf **neues Element**.  
  
    2.  In der **Code** Knoten, klicken Sie auf **C++-Datei (.cpp)**, geben Sie einen Namen für die Datei, und klicken Sie dann auf **hinzufügen**.  
  
     Die CPP-Datei wird im Quelldateiordner im **Projektmappen-Explorer**, und die Datei wird in der Visual Studio-Editor geöffnet.  
  
7.  Geben Sie in der Datei im Editor ein gültiges C++-Programm, das die C++-Standardbibliothek verwendet, oder kopieren Sie eines der Beispielprogramme, und fügen Sie ihn in der Datei.  
  
8.  Speichern Sie die Datei.  
  
9. Klicken Sie im Menü **Erstellen** auf **Projektmappe erstellen**.  
  
     Die **Ausgabe** Fenster werden Informationen zum Kompilierungsprozess angezeigt, z. B. den Speicherort des Buildprotokolls und eine Meldung, die den Buildstatus angezeigt.  
  
10. Auf der **Debuggen** Menü klicken Sie auf **Starten ohne Debugging**.  
  
     Wenn Sie das Beispielprogramm verwendet haben, wird ein Befehlsfenster angezeigt. Dieses gibt an, ob bestimmte ganze Zahlen im Set enthalten sind.  
  
## <a name="next-steps"></a>Nächste Schritte  
 **Vorherige:** [Konsolenanwendungen in Visual C++](../windows/console-applications-in-visual-cpp.md). **Weiter:**[Exemplarische Vorgehensweise: Kompilieren eines systemeigenen C++-Programms in der Befehlszeile](../build/walkthrough-compiling-a-native-cpp-program-on-the-command-line.md).  
  
## <a name="see-also"></a>Siehe auch  
 [C++-Sprachreferenz](../cpp/cpp-language-reference.md)   
 [C++-Standardbibliothek](../standard-library/cpp-standard-library-reference.md)