---
title: "Eigenschaftenzugriff muss der Eigenschaft zugewiesen werden oder deren Wert verwenden."
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
  - "bc30545"
  - "vbc30545"
helpviewer_keywords: 
  - "BC30545"
ms.assetid: df271c05-1e7a-44e8-bf53-79f06ef916ab
caps.latest.revision: 11
caps.handback.revision: "10"
ms.author: "shoag"
manager: "wpickett"
---
# Eigenschaftenzugriff muss der Eigenschaft zugewiesen werden oder deren Wert verwenden.
Sie haben versucht, auf eine Eigenschaft zuzugreifen, ohne eine Zuweisung vorzunehmen oder ihren Wert zu verwenden. Der folgende Code veranschaulicht dies:  
  
 [!CODE [VbVbalrErrorSamples#1](VbVbalrErrorSamples#1)]  
  
 **Fehler\-ID:** BC30545  
  
### So beheben Sie diesen Fehler  
  
-   Weisen Sie der Eigenschaft einen Wert zu, wie im folgenden Beispiel dargestellt:  
  
     [!CODE [VbVbalrErrorSamples#3](VbVbalrErrorSamples#3)]  
  
     \- oder \-  
  
-   Verwenden Sie den Wert der Eigenschaft, wie im folgenden Beispiel gezeigt:  
  
     [!CODE [VbVbalrErrorSamples#2](VbVbalrErrorSamples#2)]  
  
## Siehe auch  
 [Eigenschaftenprozeduren](../Topic/Property%20Procedures%20\(Visual%20Basic\).md)   
 [Assignment Operators](../Topic/Assignment%20Operators%20\(Visual%20Basic\).md)