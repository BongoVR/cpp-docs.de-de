---
title: "&#39;With&#39; muss mit einem entsprechenden &#39;End With&#39; abgeschlossen werden."
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
  - "bc30085"
  - "vbc30085"
helpviewer_keywords: 
  - "BC30085"
ms.assetid: aa88f4d0-be5f-4efe-a4ef-80e6d6124e6e
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;With&#39; muss mit einem entsprechenden &#39;End With&#39; abgeschlossen werden.
Eine `With`\-Anweisung tritt ohne eine entsprechende `End With`\-Anweisung auf. Zum Beenden des `With`\-Blocks muss eine `End With`\-Anweisung verwendet werden.  
  
 **Fehler\-ID:** BC30085  
  
### So beheben Sie diesen Fehler  
  
-   Wenn dieser `With`\-Block Teil einer Reihe von geschachtelten `With`\-Blöcken ist, stellen Sie sicher, dass jeder Block ordnungsgemäß abgeschlossen wird.  
  
-   Fügen Sie eine `End With`\-Anweisung am Ende des `With`\-Blocks hinzu.  
  
## Siehe auch  
 [With...End With Statement](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md)