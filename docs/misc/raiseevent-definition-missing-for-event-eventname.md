---
title: "Die &#39;RaiseEvent&#39;-Definition fehlt f&#252;r das Ereignis &#39;&lt;Ereignistname&gt;&#39;."
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
  - "vbc31132"
  - "bc31132"
helpviewer_keywords: 
  - "BC31132"
ms.assetid: 8f3442fd-2ed1-4dbc-83a8-f0860ec022ac
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "shoag"
manager: "wpickett"
---
# Die &#39;RaiseEvent&#39;-Definition fehlt f&#252;r das Ereignis &#39;&lt;Ereignistname&gt;&#39;.
Wenn ein Ereignis als `Custom` deklariert wird, muss es eine Prozedur zum Auslösen des Ereignisses bereitstellen.  
  
 **Fehler\-ID:** BC31132  
  
### So beheben Sie diesen Fehler  
  
1.  Fügen Sie eine `RaiseEvent`\-Deklaration zwischen der `Custom Event`\-Anweisung und der `End Event`\-Anweisung ein.  
  
2.  Stellen Sie sicher, dass andere Prozeduren innerhalb der Ereignisdeklaration richtig abgeschlossen werden.  
  
## Siehe auch  
 [RaiseEvent Statement](../Topic/RaiseEvent%20Statement.md)   
 [Event Statement](../Topic/Event%20Statement.md)