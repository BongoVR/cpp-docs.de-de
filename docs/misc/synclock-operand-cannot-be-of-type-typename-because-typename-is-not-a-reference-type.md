---
title: "Der SyncLock-Operand kann nicht den Typ &#39;&lt;typname&gt;&#39; haben, da &#39;&lt;typname&gt;&#39; kein Verweistyp ist."
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
  - "vbc30582"
  - "bc30582"
helpviewer_keywords: 
  - "BC30582"
ms.assetid: 953aecf2-629a-4272-94bd-abf88f785e63
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Der SyncLock-Operand kann nicht den Typ &#39;&lt;typname&gt;&#39; haben, da &#39;&lt;typname&gt;&#39; kein Verweistyp ist.
Die `SyncLock`\-Anweisung erlaubt die Synchronisierung von Anweisungen für einen einzelnen Ausdruck, indem sie sicherstellt, dass die gleichen Anweisungen nicht von mehreren Threads zur gleichen Zeit ausgeführt werden. Der Typ des Ausdrucks in einer `SyncLock`\-Anweisung muss ein Verweistyp, wie etwa eine Klasse, ein Modul, eine Schnittstelle, ein Array oder ein Delegat sein.  
  
 **Fehler\-ID:** BC30582  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie den Typ in einen geeigneten Verweistyp.  
  
## Siehe auch  
 [SyncLock Statement](../Topic/SyncLock%20Statement.md)   
 [NICHT im BUILD: Multithreading in Visual Basic](assetId:///c731a50c-09c1-4468-9646-54c86b75d269)