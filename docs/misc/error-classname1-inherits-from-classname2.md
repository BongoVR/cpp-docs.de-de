---
title: "&lt;Fehler&gt;: &quot;&lt;Klassenname1 &gt;&quot;erbt von &quot;&lt;Klassenname2&gt;&quot;"
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
  - "bc30256"
  - "vbc30256"
helpviewer_keywords: 
  - "BC30256"
ms.assetid: 170a12ee-87ef-4a49-8c84-ebf57fac435e
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;Fehler&gt;: &quot;&lt;Klassenname1 &gt;&quot;erbt von &quot;&lt;Klassenname2&gt;&quot;
Es wurde eine wechselseitige \(zirkuläre\) Vererbungshierarchie festgestellt. Für eine Klasse ist festgelegt, dass sie von sich selbst oder von einer anderen Klasse erbt, die unmittelbar oder letztendlich von ihr erbt.  
  
 Diese Meldung kann mehrmals angezeigt werden, um den zirkulären Vererbungspfad zu verfolgen.  
  
 **Fehler\-ID:** BC30256  
  
### So beheben Sie diesen Fehler  
  
-   Unterbrechen Sie die Zirkularität, indem Sie mindestens eine `Inherits`\-Anweisung im zirkulären Vererbungspfad entfernen.  
  
## Siehe auch  
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)