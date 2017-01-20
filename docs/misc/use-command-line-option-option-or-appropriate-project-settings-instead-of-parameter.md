---
title: "Verwenden Sie die Befehlszeilenoption &#39;&lt;option&gt;&#39; oder geeignete Projekteinstellungen anstelle von &#39;&lt;parameter&gt;&#39;"
ms.custom: na
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc41008"
  - "vbc41008"
helpviewer_keywords: 
  - "BC41008"
ms.assetid: 1c5d6d7a-b767-4dae-aa61-d7fa81d5aad1
caps.latest.revision: 4
caps.handback.revision: "4"
ms.author: "shoag"
manager: "wpickett"
---
# Verwenden Sie die Befehlszeilenoption &#39;&lt;option&gt;&#39; oder geeignete Projekteinstellungen anstelle von &#39;&lt;parameter&gt;&#39;
Das bevorzugte Verfahren zum Angeben einer Datei, die einen öffentlichen Schlüssel für eine Assembly, einen Container für öffentliche Schlüssel für eine Assembly oder eine partiell signierte Assembly enthält, besteht in der Verwendung der [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)]\-Compileroptionen. Wir empfehlen nicht die Verwendung der Attribute <xref:System.Reflection.AssemblyKeyFileAttribute>, <xref:System.Reflection.AssemblyKeyNameAttribute> und <xref:System.Reflection.AssemblyDelaySignAttribute> im Code.  
  
 **Fehler\-ID:** BC41008  
  
### So beheben Sie diesen Fehler  
  
1.  Verwenden Sie die Compileroption [\/keyfile](../Topic/-keyfile.md), [\/keycontainer](../Topic/-keycontainer.md) oder [\/delaysign](../Topic/-delaysign.md) [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] anstelle des Attributs <xref:System.Reflection.AssemblyKeyFileAttribute>, <xref:System.Reflection.AssemblyKeyNameAttribute> oder <xref:System.Reflection.AssemblyDelaySignAttribute> im Code.  
  
## Siehe auch  
 [Gewusst wie: Erstellen von signierten Friend\-Assemblys](../Topic/How%20to:%20Create%20Signed%20Friend%20Assemblies%20\(C%23%20and%20Visual%20Basic\).md)   
 [Visual Basic Command\-Line Compiler](../Topic/Visual%20Basic%20Command-Line%20Compiler.md)   
 [\/keyfile](../Topic/-keyfile.md)   
 [\/keycontainer](../Topic/-keycontainer.md)   
 [\/delaysign](../Topic/-delaysign.md)