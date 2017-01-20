---
title: "&#39;Equals&#39; kann nicht Werte vom Typ &#39;&lt;Typ1&gt;&#39; mit Werten vom Typ &#39;&lt;Typ2&gt;&#39; vergleichen."
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc36621"
  - "bc36621"
helpviewer_keywords: 
  - "BC36621"
ms.assetid: bd40bf57-3a12-407a-8622-7e428850c77c
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;Equals&#39; kann nicht Werte vom Typ &#39;&lt;Typ1&gt;&#39; mit Werten vom Typ &#39;&lt;Typ2&gt;&#39; vergleichen.
Ein `Equals`\-Operator in einer `Join`\- oder `Group Join`\-Klausel hat versucht, einen Datentyp mit einem anderen Datentyp in einer nicht definierten Weise zu vergleichen. Ein Beispiel hierfür ist ein Vergleich eines `Boolean`\-Werts mit einem `Date`\-Typ.  
  
 **Fehler\-ID:** BC36621  
  
### So beheben Sie diesen Fehler  
  
-   Stellen Sie sicher, dass die Werte auf jeder Seite des `Equals`\-Operators in einen gemeinsamen Datentyp konvertiert werden können. Hier folgen einige Optionen, um dies zu erreichen:  
  
    -   Verwenden Sie die `CType`\-Funktion, um einen oder mehrere der Werte in einen bestimmten Typ zu konvertieren.  
  
    -   Verwenden Sie die <xref:System.Convert>\-Klasse oder Konvertierungsmethoden, um einen oder mehrere der Werte in einen gemeinsamen, unveränderlichen Datentyp zu konvertieren.  
  
    -   Konvertieren Sie die Werte mithilfe der `ToString`\-Methode in Zeichenfolgen.  
  
## Siehe auch  
 [CType\-Funktion](../Topic/CType%20Function%20\(Visual%20Basic\).md)   
 [Type Conversions in Visual Basic](../Topic/Type%20Conversions%20in%20Visual%20Basic.md)   
 [Join Clause](../Topic/Join%20Clause%20\(Visual%20Basic\).md)   
 [Group Join Clause](../Topic/Group%20Join%20Clause%20\(Visual%20Basic\).md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ](../Topic/LINQ%20in%20Visual%20Basic.md)