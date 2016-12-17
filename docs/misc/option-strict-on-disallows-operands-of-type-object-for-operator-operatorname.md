---
title: "&quot;Option Strict On&quot; l&#228;sst keine Operanden des Typs &quot;Object&quot; f&#252;r den Operator &quot;&lt;Operatorname&gt;&quot; zu."
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
  - "bc32013"
  - "vbc32013"
helpviewer_keywords: 
  - "BC32013"
ms.assetid: cd197da8-2676-453b-884b-3231fb6f909d
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;Option Strict On&quot; l&#228;sst keine Operanden des Typs &quot;Object&quot; f&#252;r den Operator &quot;&lt;Operatorname&gt;&quot; zu.
"Option Strict On" lässt keine Operanden des Typs "Object" für den Operator "\<Operatorname\>" zu. Verwenden Sie den Is\-Operator, um die Objektidentität zu testen.  
  
 Einen arithmetischen Vergleichsoperator wie `=` wird mit mindestens einer Objektvariablen verwendet, wenn `Option Strict` auf `On` eingestellt ist.  
  
 **Fehler\-ID:** BC32013  
  
### So beheben Sie diesen Fehler  
  
1.  Aktivieren Sie `Option Strict Off`, wenn Objektvariablen numerische Werte enthalten und Sie einen arithmetischen Vergleich beabsichtigen.  
  
2.  Verwenden Sie für Vergleiche der Objektidentität den `Is`\-Operator.  
  
## Siehe auch  
 [Comparison Operators](../Topic/Comparison%20Operators%20\(Visual%20Basic\).md)   
 [Is Operator](../Topic/Is%20Operator%20\(Visual%20Basic\).md)   
 [Option Strict Statement](../Topic/Option%20Strict%20Statement.md)