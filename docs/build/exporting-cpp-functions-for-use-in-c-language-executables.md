---
title: Exportieren von C++-Funktionen zur Verwendung in ausführbaren c Dateien | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- functions [C++], C++ functions in C executables
- exporting DLLs [C++], C++ functions in C executables
- exporting functions [C++], C++ functions in C executables
- functions [C++], exporting
ms.assetid: 80b9e982-f52d-4312-a891-f73cc69f3c2b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cf5f348675752ff9c0b548693c442812fa6be697
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="exporting-c-functions-for-use-in-c-language-executables"></a>Exportieren von C++-Funktionen zur Verwendung in ausführbaren C-Dateien  
  
Falls eine DLL in C++ geschriebene Funktionen enthält und auf diese Funktionen über ein C-Sprachmodul zugegriffen werden soll, sollten Sie diese Funktionen mit C-Bindung anstatt mit C++-Bindung deklarieren. Sofern nicht anders angegeben, verwendet der C++-Compiler die typsichere Namensgebung (auch Namensergänzung genannt) sowie die Aufrufkonventionen von C++, wodurch ein von C durchgeführter Aufruf sich schwierig gestalten kann.  
  
Geben Sie zum Angeben von C-Bindung `extern "C"` für die Funktionsdeklarationen. Zum Beispiel:  
  
```  
extern "C" __declspec( dllexport ) int MyFunc(long parm1);  
```  
  
## <a name="what-do-you-want-to-do"></a>Wie möchten Sie vorgehen?  
  
-   [Exportieren Sie aus einer DLL mithilfe von DEF-Dateien](../build/exporting-from-a-dll-using-def-files.md)  
  
-   [Exportieren Sie aus einer DLL mithilfe von __declspec(dllexport)](../build/exporting-from-a-dll-using-declspec-dllexport.md)  
  
-   [Exportieren Sie und importieren Sie mithilfe von AFX_EXT_CLASS](../build/exporting-and-importing-using-afx-ext-class.md)  
  
-   [Exportieren von C-Funktionen zur Verwendung in ausführbaren C oder C++-Dateien](../build/exporting-c-functions-for-use-in-c-or-cpp-language-executables.md)  
  
-   [Welche Exportmethode ermitteln](../build/determining-which-exporting-method-to-use.md)  
  
-   [Importieren Sie in eine Anwendung mithilfe von "__declspec(dllimport)" "](../build/importing-into-an-application-using-declspec-dllimport.md)  
  
-   [Initialisieren einer DLL](../build/run-time-library-behavior.md#initializing-a-dll)  
  
## <a name="what-do-you-want-to-know-more-about"></a>Worüber möchten Sie mehr erfahren?  
  
-   [Ergänzte Namen](../build/reference/decorated-names.md)  
  
-   [Verwenden von "extern" zur Angabe der Verknüpfung](../cpp/using-extern-to-specify-linkage.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Exportieren aus einer DLL](../build/exporting-from-a-dll.md)