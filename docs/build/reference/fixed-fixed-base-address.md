---
title: -FIXED (Feste Basisadresse) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /fixed
- VC.Project.VCLinkerTool.FixedBaseAddress
dev_langs:
- C++
helpviewer_keywords:
- preferred base address for loading program
- /FIXED linker option
- -FIXED linker option
- FIXED linker option
ms.assetid: 929bba5e-b7d8-40ed-943e-056aa3710fc5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 08b1193b7cfe58aed45e4feec598a49227eafc87
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="fixed-fixed-base-address"></a>/FIXED (Feste Basisadresse)
```  
/FIXED[:NO]  
```  
  
## <a name="remarks"></a>Hinweise  
 Weist das Betriebssystem an, das Programm nur an seine bevorzugte Basisadresse zu laden. Wenn diese Basisadresse nicht zur Verfügung steht, lädt das Betriebssystem die Datei nicht. Weitere Informationen finden Sie unter [/BASE (Basisadresse)](../../build/reference/base-base-address.md).  
  
 Für eine DLL ist "/FIXED:NO" die Standardeinstellung; bei anderen Projekttypen lautet die Standardeinstellung "/FIXED".  
  
 Bei Angabe von "/FIXED" generiert LINK keinen Verschiebungsabschnitt im Programm. Wenn das Betriebssystem das Programm zur Laufzeit nicht an der angegebenen Adresse laden kann, wird eine Fehlermeldung ausgegeben, und der Ladevorgang wird nicht ausgeführt.  
  
 Bei Angabe von "/FIXED:NO" wird ein Verschiebungsabschnitt im Programm generiert.  
  
### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest  
  
1.  Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [arbeiten mit Projekteigenschaften](../../ide/working-with-project-properties.md).  
  
2.  Wählen Sie die **Linker** Ordner.  
  
3.  Wählen Sie die **Befehlszeile** Eigenschaftenseite.  
  
4.  Geben Sie den Optionsnamen und festlegen, der **Zusatzoptionen** Feld.  
  
### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest  
  
-   Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.  
  
## <a name="see-also"></a>Siehe auch  
 [Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)   
 [Linkeroptionen](../../build/reference/linker-options.md)