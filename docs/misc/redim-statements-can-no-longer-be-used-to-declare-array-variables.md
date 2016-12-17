---
title: "Die Anweisung &quot;ReDim&quot; kann nicht mehr zum Deklarieren eines Arrays verwendet werden"
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
  - "bc30811"
  - "vbc30811"
helpviewer_keywords: 
  - "BC30811"
ms.assetid: 9227a06e-a997-4b16-9977-19e2bce9035b
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Die Anweisung &quot;ReDim&quot; kann nicht mehr zum Deklarieren eines Arrays verwendet werden
`ReDim` kann nur verwendet werden, um die Größe eines vorhandenen Arrays zu ändern.  
  
 **Fehler\-ID:** BC30811  
  
### So beheben Sie diesen Fehler  
  
-   Geben Sie die Größe des Arrays bei der Deklaration an; Beispiel:  
  
    ```  
    Dim X(20) As Integer  
    ```  
  
## Siehe auch  
 [Arrays Summary](../Topic/Arrays%20Summary%20\(Visual%20Basic\).md)   
 [ReDim Statement](../Topic/ReDim%20Statement%20\(Visual%20Basic\).md)   
 [ReDim Statement Changes in Visual Basic](assetId:///b4da14db-ff23-490f-b3c6-d7ae1b649532)