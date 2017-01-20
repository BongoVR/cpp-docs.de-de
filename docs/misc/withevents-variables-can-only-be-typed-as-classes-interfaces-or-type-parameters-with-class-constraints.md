---
title: "WithEvents-Variablen k&#246;nnen nur als Klassen, Schnittstellen oder Typparameter mit Klasseneinschr&#228;nkungen typisiert werden."
ms.custom: na
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc30413"
  - "bc30413"
helpviewer_keywords: 
  - "BC30413"
ms.assetid: 11ddf207-2760-425f-b4c2-bb9fe6da36ea
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# WithEvents-Variablen k&#246;nnen nur als Klassen, Schnittstellen oder Typparameter mit Klasseneinschr&#228;nkungen typisiert werden.
Sie haben eine Variable deklariert, die in Verbindung mit `WithEvents` als Struktur typisiert ist, also eine nicht zulässige Verwendung des `WithEvents`\-Modifizierers.  
  
 **Fehler\-ID:** BC30413  
  
### So beheben Sie diesen Fehler  
  
1.  Verwenden Sie `AddHandler`, um in einer Struktur definierte Ereignisse zu behandeln.  
  
## Siehe auch  
 [NICHT IM BUILD: WithEvents und die Handles\-Klausel](assetId:///072b9cf6-6298-46f1-849e-4edc1631564c)   
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [AddHandler Statement](../Topic/AddHandler%20Statement.md)