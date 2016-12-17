---
title: "Der Operator &quot;&lt;Operatorname&gt;&quot; ist nicht f&#252;r die Typen &quot;&lt;Typname1&gt;&quot; und &quot;&lt;Typname2 &gt;&quot; definiert."
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
  - "vbc31080"
  - "bc31080"
helpviewer_keywords: 
  - "BC31080"
ms.assetid: d2f77450-2bf2-4b1e-b95f-dbc7878f2777
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Der Operator &quot;&lt;Operatorname&gt;&quot; ist nicht f&#252;r die Typen &quot;&lt;Typname1&gt;&quot; und &quot;&lt;Typname2 &gt;&quot; definiert.
Der Operator "\<Operatorname\>" ist nicht für die Typen "\<Typname1\>" und "\<Typname2 \>" definiert. Verwenden Sie den Is\-Operator, um zwei Verweistypen zu vergleichen.  
  
 Es wurde versucht, einen Operator auf eine Weise zu verwenden, die für die angegebenen Typen nicht geeignet ist. Dieser Fehler kann verursacht werden, wenn Sie den Operator "\=" anstelle des `Is`\-Operators verwenden, um zwei Objekte zu vergleichen.  
  
 **Fehler\-ID:** BC31080  
  
### So beheben Sie diesen Fehler  
  
1.  Verwenden Sie den `Is`\-Operator, um zwei Verweistypen zu vergleichen.  
  
2.  Verwenden Sie den `Not`\-Operator in Verbindung mit dem `Is`\-Operator, um Ungleichheit anzugeben. Zum Beispiel:  
  
     [!CODE [VbVbalrOOP#89](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#89)]  
  
## Siehe auch  
 [Is Operator](../Topic/Is%20Operator%20\(Visual%20Basic\).md)   
 [\= Operator](../Topic/=%20Operator%20\(Visual%20Basic\).md)   
 [Not Operator](../Topic/Not%20Operator%20\(Visual%20Basic\).md)