---
title: "MSBuild Error MSB3023"
ms.custom: na
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "MSBuild.Copy.NeedsDestination"
helpviewer_keywords: 
  - "MSB3023"
ms.assetid: 3505ad1e-d54f-4cb4-a299-ac03684cb391
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "mblome"
manager: "douge"
---
# MSBuild Error MSB3023
**Es wurde kein Ziel für den Kopiervorgang angegeben.  Geben Sie entweder \<Attribut\> oder \<Attribut\> an.**  
  
 Für die `Copy`\-Aufgabe muss unter Verwendung eines der Aufgabenattribute `DestinationFiles`oder `DestinationDirectory` ein Ziel angegeben werden.  
  
### So beheben Sie diesen Fehler  
  
-   Geben Sie entweder `DestinationFiles`oder`DestinationDirectory` für die `Copy`\-Aufgabe an.  
  
## Siehe auch  
 [Copy Task](../Topic/Copy%20Task.md)   
 [Tasks](../Topic/MSBuild%20Tasks.md)