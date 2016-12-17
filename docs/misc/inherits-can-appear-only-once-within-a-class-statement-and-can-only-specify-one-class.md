---
title: "In einer Class-Anweisung darf „Inherits“ nur einmal verwendet werden und kann nur eine Klasse angeben."
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
  - "vbc30121"
  - "bc30121"
helpviewer_keywords: 
  - "BC30121"
ms.assetid: 4ac5b018-5632-4661-8ac6-dbda2f8c4dfe
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# In einer Class-Anweisung darf „Inherits“ nur einmal verwendet werden und kann nur eine Klasse angeben.
Mehrere `Inherits`\-Anweisungen werden in der gleichen Klasse verwendet, oder eine `Inherits`\-Anweisung gibt mehr als eine Klasse an. Eine Klasse kann nur von einer Basisklasse erben.  
  
 **Fehler\-ID:** BC30121  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie alle überzähligen `Inherits`\-Anweisungen, und stellen Sie sicher, dass die verbleibende `Inherits`\-Anweisung nur eine Basisklasse angibt.  
  
## Siehe auch  
 [Inherits Statement](../Topic/Inherits%20Statement.md)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)