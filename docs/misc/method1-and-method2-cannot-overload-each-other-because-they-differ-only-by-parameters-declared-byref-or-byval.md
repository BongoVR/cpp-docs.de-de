---
title: "„method1“ und „method2“ k&#246;nnen sich nicht gegenseitig &#252;berladen, da sie sich nur durch Parameter unterscheiden, die als „ByRef“ oder „ByVal“ deklariert sind."
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
  - "bc30345"
  - "vbc30345"
helpviewer_keywords: 
  - "BC30345"
ms.assetid: 82af13b1-2641-4881-b25a-c782974bded1
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# „method1“ und „method2“ k&#246;nnen sich nicht gegenseitig &#252;berladen, da sie sich nur durch Parameter unterscheiden, die als „ByRef“ oder „ByVal“ deklariert sind.
Sie haben versucht, eine Methode mit einer anderen Methode zu überladen, die sich von der ersten nur durch einen als `ByRef` oder `ByVal` deklarierten Parameter unterscheidet.  
  
 **Fehler\-ID:** BC30345  
  
### So beheben Sie diesen Fehler  
  
-   Stellen Sie sicher, dass die Methoden sich durch mehr als den Namen des `ByRef`\- oder `ByVal`\-Parameters unterscheiden.  
  
## Siehe auch  
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Considerations in Overloading Procedures](../Topic/Considerations%20in%20Overloading%20Procedures%20\(Visual%20Basic\).md)