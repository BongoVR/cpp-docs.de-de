---
title: "„For“ muss mit einem entsprechenden „Next“ abgeschlossen werden."
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
  - "vbc30084"
  - "bc30084"
helpviewer_keywords: 
  - "BC30084"
ms.assetid: 4c5e49c2-7343-4487-b5f8-a38c97ba895b
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# „For“ muss mit einem entsprechenden „Next“ abgeschlossen werden.
Eine `For`\-Anweisung tritt ohne entsprechende `Next`\-Anweisung auf. Zum Beenden der `For`\-Schleife muss eine `Next`\-Anweisung angegeben werden.  
  
 **Fehler\-ID:** BC30084  
  
### So beheben Sie diesen Fehler  
  
-   Wenn diese `For`\-Schleife Teil einer Reihe von geschachtelten Schleifen ist, stellen Sie sicher, dass jede Schleife korrekt abgeschlossen wird.  
  
-   Fügen Sie eine `Next`\-Anweisung ans Ende der `For`\-Schleife hinzu.  
  
## Siehe auch  
 [For...Next\-Anweisung](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)