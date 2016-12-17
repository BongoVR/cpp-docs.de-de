---
title: "Die Next-Steuerungsvariable stimmt nicht mit der For-Schleifensteuerungsvariablen  &#39;&lt;Variablenname&gt;&#39; &#252;berein."
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
  - "vbc30070"
  - "bc30070"
helpviewer_keywords: 
  - "BC30070"
ms.assetid: e9e96008-b053-4fa0-8966-decaad99fecd
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Die Next-Steuerungsvariable stimmt nicht mit der For-Schleifensteuerungsvariablen  &#39;&lt;Variablenname&gt;&#39; &#252;berein.
Die Steuerungsvariable in der `Next`\-Anweisung einer `For...Next`\-Schleife muss mit der Variablen in der entsprechenden entsprechen `For`\-Anweisung übereinstimmen.  
  
 **Fehler\-ID:** BC30070  
  
### So beheben Sie diesen Fehler  
  
1.  Überprüfen Sie die Schreibweise der Variablen in der `Next`\-Anweisung und in der entsprechenden `For`\-Anweisung, um sicherzustellen, dass sie übereinstimmt.  
  
2.  Vergewissern Sie sich, dass keine Teile der umschließenden Schleife versehentlich gelöscht wurden.  
  
3.  Wenn diese Schleife Teil einer Reihe von geschachtelten Schleifen ist, überprüfen Sie, ob jede Schleife ordnungsgemäß abgeschlossen wird.  
  
## Siehe auch  
 [For...Next\-Anweisung](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)