---
title: "&quot;Option Strict On&quot; erfordert in allen Methodenparametern eine As-Klausel."
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
  - "vbc30211"
  - "bc30211"
helpviewer_keywords: 
  - "BC30211"
ms.assetid: 855795ce-8499-4525-a1de-cbb8ba364cd7
caps.latest.revision: 4
caps.handback.revision: "4"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;Option Strict On&quot; erfordert in allen Methodenparametern eine As-Klausel.
Eine Methode enthält einen Parameter ohne eine `As`\-Klausel. Wenn `Option Strict` aktiviert ist, muss jede Variable, jede Eigenschaft, jedes Prozedurargument und jede Funktionsrückgabe mit einer `As`\-Klausel zur Angabe des Datentyps deklariert werden, z. B. `Sub GetData(ByVal filter As String)`.  
  
 **Fehler\-ID:** BC30211  
  
### So beheben Sie diesen Fehler  
  
-   Überprüfen, ob das `As`\-Schlüsselwort falsch geschrieben ist.  
  
-   Geben Sie eine `As`\-Klausel für die deklarierte Variable an, oder deaktivieren Sie `Option Strict`.  
  
## Siehe auch  
 [Option Strict Statement](../Topic/Option%20Strict%20Statement.md)   
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)