---
title: "&quot;Catch&quot; kann nicht au&#223;erhalb einer Try-Anweisung verwendet werden"
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
  - "bc30380"
  - "vbc30380"
helpviewer_keywords: 
  - "BC30380"
ms.assetid: 73ce950d-881f-4532-8024-40a4930abd32
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;Catch&quot; kann nicht au&#223;erhalb einer Try-Anweisung verwendet werden
`Catch` muss innerhalb eines `Try...Catch...Finally`\-Anweisungsblocks angezeigt werden. Entweder ist die `Catch`\-Anweisung im `Try`\-Block unnötig, oder die `Catch`\-Anweisung befindet sich außerhalb des entsprechenden `Try`\-Blocks.  
  
 **Fehler\-ID:** BC30380  
  
### So beheben Sie diesen Fehler  
  
1.  Löschen Sie die `Catch`\-Anweisung, wenn sie unnötig ist, oder platzieren Sie sie in einem `Try...Catch...Finally`\-Anweisungsblock.  
  
## Siehe auch  
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)   
 [Übersicht über die strukturierte Ausnahmebehandlung für Visual Basic](assetId:///bb81af80-a735-4873-9711-6151a48e418a)