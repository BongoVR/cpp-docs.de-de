---
title: "Eine Eigenschaft, die als &quot;ReadOnly&quot; deklariert ist, darf kein &quot;Set&quot; haben."
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
  - "vbc30022"
  - "bc30022"
helpviewer_keywords: 
  - "BC30022"
ms.assetid: a22eff96-8c18-47c4-9ef0-f98b2ab8a5d8
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Eine Eigenschaft, die als &quot;ReadOnly&quot; deklariert ist, darf kein &quot;Set&quot; haben.
Die `Set`\-Prozedur schreibt den Wert einer Eigenschaft. In `ReadOnly`\-Eigenschaften kann nicht geschrieben werden.  
  
 **Fehler\-ID:** BC30022  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie das Schlüsselwort "`ReadOnly`" aus der `Property`\-Anweisung, oder entfernen Sie die `Set`\-Prozedur aus dem Eigenschaftentext.  
  
## Siehe auch  
 [Property Statement](../Topic/Property%20Statement.md)   
 [Set Statement](../Topic/Set%20Statement%20\(Visual%20Basic\).md)   
 [ReadOnly](../Topic/ReadOnly%20\(Visual%20Basic\).md)