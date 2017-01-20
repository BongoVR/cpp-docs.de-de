---
title: "Die Throw-Anweisung kann au&#223;erhalb einer Catch-Anweisung oder innerhalb einer Finally-Anweisung den Operanden nicht auslassen."
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
  - "vbc30666"
  - "bc30666"
helpviewer_keywords: 
  - "BC30666"
ms.assetid: a208a6ea-0e36-4bf1-8984-4de1a0e38a2a
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Die Throw-Anweisung kann au&#223;erhalb einer Catch-Anweisung oder innerhalb einer Finally-Anweisung den Operanden nicht auslassen.
`Throw`\-Anweisungen außerhalb einer `Catch`\-Anweisung müssen den Namen eines Ausnahmeobjekts angeben.  
  
 **Fehler\-ID:** BC30666  
  
### So beheben Sie diesen Fehler  
  
1.  Geben Sie den Namen eines von `System.Exception` abgeleiteten Ausnahmeobjekts an.  
  
2.  Strukturieren Sie den Code neu, damit sich die `Throw`\-Anweisung innerhalb eines `Catch`\-Blocks befindet.  
  
## Siehe auch  
 [Throw Statement](../Topic/Throw%20Statement%20\(Visual%20Basic\).md)   
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)   
 [Ausnahmeklasse in Visual Basic](assetId:///9aac396f-34ca-4afb-8e6c-e523cb690ba9)   
 [Ausnahmen\- und Fehlerbehandlung in Visual Basic](assetId:///3e351e73-cf23-40ab-8b60-05794160529e)