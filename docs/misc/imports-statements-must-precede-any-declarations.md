---
title: "Imports-Anweisungen m&#252;ssen vor Deklarationen stehen"
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
  - "vbc30465"
  - "bc30465"
helpviewer_keywords: 
  - "BC30465"
ms.assetid: 726365f6-d6fc-454a-a43b-afa41bfea82a
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "shoag"
manager: "wpickett"
---
# Imports-Anweisungen m&#252;ssen vor Deklarationen stehen
Eine `Imports`\-Anweisung folgt auf eine Deklarationsanweisung innerhalb einer Quelldatei.  
  
 Die `Imports`\-Anweisung importiert Namespacenamen aus referenzierten Projekten und Assemblys sowie Namespacenamen, die im selben Projekt wie dem definiert sind, in dem sie erscheint.`Imports`\-Anweisungen müssen vor Verweisen auf Bezeichner in einer Quelldatei platziert werden.  
  
 **Fehler\-ID:** BC30465  
  
### So beheben Sie diesen Fehler  
  
-   Verschieben Sie die `Imports`\-Anweisung an den Anfang der Quelldatei vor die Deklarationsanweisungen.  
  
## Siehe auch  
 [Imports Statement \(.NET Namespace and Type\)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md)