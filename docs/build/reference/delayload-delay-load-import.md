---
title: -DELAYLOAD (Laden von Import verzögern) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /delayload
- VC.Project.VCLinkerTool.DelayLoadDLLS
dev_langs:
- C++
helpviewer_keywords:
- DELAYLOAD linker option
- -DELAYLOAD linker option
- /DELAYLOAD linker option
- delayed loading of DLLs, /DELAYLOAD option
ms.assetid: 39ea0f1e-5c01-450f-9c75-2d9761ff9b28
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 74d65caa8a0ea140f93bf156e3c14a85232e6e56
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="delayload-delay-load-import"></a>/DELAYLOAD (Laden von Import verzögern)
```  
/DELAYLOAD:dllname  
```  
  
## <a name="parameters"></a>Parameter  
 `dllname`  
 Der Name einer DLL, die mit einer Verzögerung geladen werden soll.  
  
## <a name="remarks"></a>Hinweise  
 Die /DELAYLOAD-Option bewirkt, dass die durch `dllname` angegebene DLL nur beim ersten Aufruf einer Funktion in dieser DLL vom Programm geladen wird. Weitere Informationen finden Sie unter [Linkerunterstützung für verzögert geladene DLLs](../../build/reference/linker-support-for-delay-loaded-dlls.md). Sie können diese Option so oft wie notwendig verwenden, um die von Ihnen gewünschte Anzahl von DLLs festzulegen. Beim Verknüpfen des Programms müssen Sie "Delayimp.lib" verwenden. Sie können aber auch eine eigene Hilfsfunktion für das verzögerte Laden implementieren.  
  
 Die [/DELAY](../../build/reference/delay-delay-load-import-settings.md) Option gibt an, zum Binden und laden die Optionen für die einzelnen verzögert geladenen DLLs.  
  
### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest  
  
1.  Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [arbeiten mit Projekteigenschaften](../../ide/working-with-project-properties.md).  
  
2.  In der **Linker** Ordner, wählen Sie die **Eingabe** Eigenschaftenseite.  
  
3.  Ändern der **verzögert geladene DLLs** Eigenschaft.  
  
### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest  
  
-   Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.DelayLoadDLLs%2A>.  
  
## <a name="see-also"></a>Siehe auch  
 [Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)   
 [Linkeroptionen](../../build/reference/linker-options.md)