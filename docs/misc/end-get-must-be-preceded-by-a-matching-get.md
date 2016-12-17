---
title: "„End Get“ muss ein entsprechendes „Get“ voranstehen."
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
  - "bc30630"
  - "vbc30630"
helpviewer_keywords: 
  - "BC30630"
ms.assetid: d858076a-9088-4ad0-9766-95029476bf9b
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# „End Get“ muss ein entsprechendes „Get“ voranstehen.
`End Get` dient zum Beenden von `Get`\-Eigenschaftenprozeduren. Das `End Get`\-Konstrukt wurde außerhalb einer `Get`\-Eigenschaftenprozedur gefunden.  
  
 **Fehler\-ID:** BC30630  
  
### So beheben Sie diesen Fehler  
  
1.  Stellen Sie sicher, dass die `Get`\-Eigenschaftenprozedur nach einem `Property`\-Schlüsselwort und vor dem `End Property`\-Konstrukt deklariert wird.  
  
2.  Stellen Sie sicher, dass die `Get`\-Eigenschaftenprozedur mit dem `Get`\-Schlüsselwort beginnt und mit dem `End Get`\-Konstrukt endet.  
  
## Siehe auch  
 [Property Statement](../Topic/Property%20Statement.md)   
 [Property Changes in Visual Basic](assetId:///1c138efa-9bc2-44d7-80a0-f3a7c2510264)