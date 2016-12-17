---
title: "Das durch das DefaultEvent-Attribut angegebene &#39;&lt;Ereignisname&gt;&#39;-Ereignis ist f&#252;r diese Klasse nicht &#246;ffentlich zugreifbar"
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
  - "vbc30770"
  - "bc30770"
helpviewer_keywords: 
  - "BC30770"
ms.assetid: 7524fba7-2a37-4bc3-b789-87d73a166575
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Das durch das DefaultEvent-Attribut angegebene &#39;&lt;Ereignisname&gt;&#39;-Ereignis ist f&#252;r diese Klasse nicht &#246;ffentlich zugreifbar
Das <xref:System.ComponentModel.DefaultEventAttribute>\-Attribut muss den Namen des öffentlich zugreifbaren Ereignisses in der Klasse angeben, auf die das Attribut angewendet wird.  
  
 **Fehler\-ID:** BC30770  
  
### So beheben Sie diesen Fehler  
  
1.  Stellen Sie sicher, dass die Klasse ein öffentlich zugreifbares Ereignis definiert.  
  
2.  Stellen Sie sicher, dass der Name des Ereignisses in der Klasse mit dem Namen übereinstimmt, der durch das <xref:System.ComponentModel.DefaultEventAttribute>\-Attribut angegeben wird.  
  
## Siehe auch  
 <xref:System.ComponentModel.DefaultEventAttribute>   
 [Event Statement](../Topic/Event%20Statement.md)   
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Public](../Topic/Public%20\(Visual%20Basic\).md)