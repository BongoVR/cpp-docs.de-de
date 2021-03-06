---
title: Exportieren aus einer DLL | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- exporting DLLs [C++], about exporting from DLLs
- exporting functions [C++], DLLs (exporting from)
- exporting DLLs [C++]
- DLLs [C++], exporting from
- DLL exports [C++]
- functions [C++], exporting
- exports table [C++]
ms.assetid: a08f86c4-5996-460b-ae54-da2b764045f0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 07efe3d73b3f78dfb30e85ffad6434e2907c36c4
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="exporting-from-a-dll"></a>Exportieren aus einer DLL  
  
Das Layout einer DLL-Datei ähnelt dem einer EXE-Datei. Ein wichtiger Unterschied besteht jedoch darin, dass eine DLL-Datei über eine Exporttabelle verfügt. Die Exporttabelle umfasst die Namen aller Funktionen, die von der DLL in andere ausführbare Dateien exportiert werden. Die Funktionen sind Einstiegspunkte in die DLL. Andere ausführbare Dateien können nur auf die in der Exporttabelle genannten Funktionen zugreifen. Alle weiteren Funktionen in der DLL sind privat, d. h. ausschließlich auf die DLL bezogen. Die Exporttabelle einer DLL kann angezeigt werden, mithilfe der [DUMPBIN](../build/reference/dumpbin-reference.md) Tool mit der Option/Exports.  
  
 Es gibt zwei Methoden zum Exportieren von Funktionen aus einer DLL:  
  
-   Erzeugen Sie eine Moduldefinitionsdatei (.def), und verwenden Sie beim Erstellen der DLL diese DEF-Datei. Verwenden Sie diesen Ansatz, wenn Sie möchten [Exportieren von Funktionen aus einer DLL über die Ordnungszahl statt über den Namen](../build/exporting-functions-from-a-dll-by-ordinal-rather-than-by-name.md).  
  
-   Verwenden Sie das Schlüsselwort **__declspec(dllexport)** in der Definition der Funktion.  
  
 Wenn Sie Funktionen mit beiden Methoden exportieren, stellen Sie sicher, verwenden die [__stdcall](../cpp/stdcall.md) Aufrufkonvention.  
  
## <a name="what-do-you-want-to-do"></a>Wie möchten Sie vorgehen?  
  
-   [Exportieren Sie aus einer DLL mithilfe von DEF-Dateien](../build/exporting-from-a-dll-using-def-files.md)  
  
-   [Exportieren Sie aus einer DLL mithilfe von __declspec(dllexport)](../build/exporting-from-a-dll-using-declspec-dllexport.md)  
  
-   [Exportieren Sie und importieren Sie mithilfe von AFX_EXT_CLASS](../build/exporting-and-importing-using-afx-ext-class.md)  
  
-   [Exportieren von C++-Funktionen zur Verwendung in ausführbaren c-Dateien](../build/exporting-cpp-functions-for-use-in-c-language-executables.md)  
  
-   [Exportieren von C-Funktionen zur Verwendung in ausführbaren C oder C++-Dateien](../build/exporting-c-functions-for-use-in-c-or-cpp-language-executables.md)  
  
-   [Exportieren von Funktionen aus einer DLL über die Ordnungszahl statt über den Namen](../build/exporting-functions-from-a-dll-by-ordinal-rather-than-by-name.md)  
  
-   [Welche Exportmethode ermitteln](../build/determining-which-exporting-method-to-use.md)  
  
-   [Welche Verknüpfungsmethode ermitteln](../build/linking-an-executable-to-a-dll.md#determining-which-linking-method-to-use)  
  
-   [Initialisieren einer DLL](../build/run-time-library-behavior.md#initializing-a-dll)  
  
## <a name="what-do-you-want-to-know-more-about"></a>Worüber möchten Sie mehr erfahren?  
  
-   [Importieren in eine Anwendung](../build/importing-into-an-application.md)  
  
-   [Importieren und Exportieren von Inlinefunktionen](../build/importing-and-exporting-inline-functions.md)  
  
-   [Gegenseitige Importe](../build/mutual-imports.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Importieren und Exportieren](../build/importing-and-exporting.md)