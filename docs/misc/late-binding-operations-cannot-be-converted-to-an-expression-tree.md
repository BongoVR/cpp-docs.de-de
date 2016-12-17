---
title: "Vorg&#228;nge f&#252;r sp&#228;tes Binden k&#246;nnen nicht in eine Ausdrucksbaumstruktur konvertiert werden"
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
  - "vbc36604"
  - "bc36604"
helpviewer_keywords: 
  - "BC36604"
ms.assetid: 6fd66d12-8c99-46e0-9095-fe1b29fd2692
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "shoag"
manager: "wpickett"
---
# Vorg&#228;nge f&#252;r sp&#228;tes Binden k&#246;nnen nicht in eine Ausdrucksbaumstruktur konvertiert werden
Es wurde versucht, einen Vorgang für spätes Binden in eine Ausdrucksbaumstruktur zu konvertieren. Dies ist ungültig. Dieser Fehler wird beispielsweise durch den folgenden Code verursacht.  
  
```vb#  
Option Strict Off Module Module1 Sub Main() '' Not valid. ' Test(Function(someInstance) someInstance.SomeProperty) End Sub Sub Test(ByVal ex As Expressions.Expression(Of Func(Of Object, Object))) End Sub End Module  
```  
  
 **Fehler\-ID:** BC36604  
  
## Siehe auch  
 [Early and Late Binding](../Topic/Early%20and%20Late%20Binding%20\(Visual%20Basic\).md)   
 [NICHT IM BUILD: Ausdrucksbaumstrukturen in LINQ](assetId:///1a2e8e74-4bbc-45ab-9a46-2b6cfce3bcb2)