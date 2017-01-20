---
title: "Declare-Anweisungen sind in generischen Typen oder in Typen, die in generischen Typen enthalten sind, nicht zul&#228;ssig"
ms.custom: na
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "BC32075"
  - "vbc32075"
helpviewer_keywords: 
  - "BC32075"
ms.assetid: c620b67e-70f8-42ac-8292-e9ea484904c3
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Declare-Anweisungen sind in generischen Typen oder in Typen, die in generischen Typen enthalten sind, nicht zul&#228;ssig
Eine `Declare`\-Anweisung wird als Teil einer generischen Klasse oder Struktur oder einer in einer generischen Klasse oder Struktur deklarierten Klasse oder Struktur verwendet.  
  
 Visual Basic und .NET Framework unterstützen derzeit keine Kombination von externen Verweisen und generischen Typen. Der Compiler benötigt alle Parameter und den Rückgabetyp einer externen Prozedur, um sie ordnungsgemäß aufrufen zu können.  
  
 **Fehler\-ID:** BC32075  
  
### So beheben Sie diesen Fehler  
  
-   Verschieben Sie die `Declare`\-Anweisung an eine Position außerhalb des Bereichs eines generischen Typs, oder entfernen Sie sie ganz.  
  
## Siehe auch  
 [Declare Statement](../Topic/Declare%20Statement.md)   
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)