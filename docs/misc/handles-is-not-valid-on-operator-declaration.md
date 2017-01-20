---
title: "&quot;Handles&quot; ist f&#252;r Operatordeklaration nicht g&#252;ltig."
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
  - "bc33003"
  - "vbc33003"
helpviewer_keywords: 
  - "BC33003"
ms.assetid: 8336402c-9393-4e8e-834d-55c2268f24f6
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;Handles&quot; ist f&#252;r Operatordeklaration nicht g&#252;ltig.
In einer [Operator Statement](../Topic/Operator%20Statement.md) ist das Schlüsselwort [Handles](../Topic/Handles%20Clause%20\(Visual%20Basic\).md) angegeben.  
  
 Ereignisse können nur in einer `Sub`\-Prozedur behandelt werden. In einer `Operator`\-Prozedur ist dies nicht möglich. Weitere Informationen zu Ereignishandlern finden Sie unter [How to: Call an Event Handler in Visual Basic](../Topic/How%20to:%20Call%20an%20Event%20Handler%20in%20Visual%20Basic.md).  
  
 Eine `Operator`\-Prozedur erfordert sowohl das Schlüsselwort `Public` als auch das Schlüsselwort `Shared`, und ein Konvertierungsoperator erfordert entweder das Schlüsselwort `Widening` oder das Schlüsselwort `Narrowing`. Weitere Informationen finden Sie unter [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md).  
  
 **Fehler\-ID:** BC33003  
  
### So beheben Sie diesen Fehler  
  
-   Wenn in dieser Prozedur Ereignisse behandelt werden sollen, müssen Sie sie in eine `Sub`\-Prozedur umschreiben.  
  
-   Soll in dieser Prozedur ein Operator definiert werden, entfernen Sie das `Handles`\-Schlüsselwort aus der Deklaration.  
  
## Siehe auch  
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)