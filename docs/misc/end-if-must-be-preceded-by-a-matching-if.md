---
title: "„End If“ muss ein entsprechendes „If“ voranstehen."
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
  - "bc30087"
  - "vbc30087"
helpviewer_keywords: 
  - "BC30087"
ms.assetid: 81c056bb-267e-44ef-9a44-3a41273090ea
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# „End If“ muss ein entsprechendes „If“ voranstehen.
Eine `End If`\-Anweisung tritt ohne entsprechende `If`\-Anweisung auf.`End If` muss eine `If`\-Anweisung vorangestellt sein.  
  
 **Fehler\-ID:** BC30087  
  
### So beheben Sie diesen Fehler  
  
1.  Wenn dieser `If`\-Block Teil einer Reihe von geschachtelten `If`\-Blöcken ist, stellen Sie sicher, dass jeder Block korrekt beendet wird.  
  
2.  Stellen Sie sicher, dass andere Steuerungsstrukturen innerhalb des `If`\-Blocks ordnungsgemäß beendet werden.  
  
3.  Stellen Sie sicher, dass dieser `If`\-Block korrekt formatiert ist.  
  
## Siehe auch  
 [If...Then...Else Statement](../Topic/If...Then...Else%20Statement%20\(Visual%20Basic\).md)