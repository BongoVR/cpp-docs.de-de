---
title: "Der &lt;Operator&gt;-Operator muss einen Parameter haben."
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
  - "bc33014"
  - "vbc33014"
helpviewer_keywords: 
  - "BC33014"
ms.assetid: 512a5724-a6c5-4437-a608-7d6b10e68d49
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Der &lt;Operator&gt;-Operator muss einen Parameter haben.
Ein unärer Operator ist ohne Parameter oder mit mehreren Parametern definiert.  
  
 Ein unärer Operator muss genau einen Parameter haben.  
  
 **Fehler\-ID:** BC33014  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie die Definition so, dass sie genau einen Parameter angibt.  
  
-   Wenn Sie zwei Parameter benötigen, müssen Sie einen binären Operator definieren.  
  
-   Wenn Sie keine oder mehr als zwei Parameter benötigen, müssen Sie die [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md) zum Definieren einer `Function`\-Prozedur anstelle eines Operators verwenden.  
  
## Siehe auch  
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)