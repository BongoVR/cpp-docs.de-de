---
title: "&quot;Exit While&quot; kann nur innerhalb einer While-Anweisung verwendet werden."
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
  - "vbc30097"
  - "bc30097"
helpviewer_keywords: 
  - "BC30097"
ms.assetid: cf0a3e09-5252-4198-bb27-c103c98d9f19
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;Exit While&quot; kann nur innerhalb einer While-Anweisung verwendet werden.
Eine `Exit While`\-Anweisung befindet sich außerhalb eines `While`\-Blocks.`Exit While` ist nur zwischen einer `While`\- und einer entsprechenden `End While`\-Anweisung gültig.  
  
 **Fehler\-ID:** BC30097  
  
### So beheben Sie diesen Fehler  
  
1.  Stellen Sie sicher, dass eine gültige `While`\-Anweisung vor `Exit While` steht und eine gültige `End While`\-Anweisung darauf folgt.  
  
2.  Stellen Sie sicher, dass andere Steuerungsstrukturen innerhalb des `While`\-Blocks ordnungsgemäß beendet werden.  
  
## Siehe auch  
 [While...End While Statement](../Topic/While...End%20While%20Statement%20\(Visual%20Basic\).md)