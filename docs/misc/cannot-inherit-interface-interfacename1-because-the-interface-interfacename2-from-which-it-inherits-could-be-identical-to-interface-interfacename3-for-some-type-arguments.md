---
title: "Die Schnittstelle &quot;&lt;Schnittstellennname1&gt;&quot; kann nicht geerbt werden, da die Schnittstelle &quot;&lt;Schnittstellennname2&gt;&quot;, von der geerbt wird, bei manchen Typargumenten m&#246;glicherweise mit der Schnittstelle &quot;&lt;Schnittstellennname3&gt;&quot; identisch ist."
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
  - "bc32121"
  - "vbc32121"
helpviewer_keywords: 
  - "BC32121"
ms.assetid: 56b1167e-f626-4a27-8395-9d396cc209f2
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "shoag"
manager: "wpickett"
---
# Die Schnittstelle &quot;&lt;Schnittstellennname1&gt;&quot; kann nicht geerbt werden, da die Schnittstelle &quot;&lt;Schnittstellennname2&gt;&quot;, von der geerbt wird, bei manchen Typargumenten m&#246;glicherweise mit der Schnittstelle &quot;&lt;Schnittstellennname3&gt;&quot; identisch ist.
Eine generische Schnittstelle erbt von mindestens zwei generischen Schnittstellen, und zwei der Vererbungen können einen Konflikt mit bestimmten Werten von Typargumenten verursachen.  
  
 Dieser Fehler kann durch die folgenden Anweisungen generiert werden.  
  
```  
Public Interface interfaceA(Of u) Inherits interfaceX(Of u) End Interface Public Interface interfaceX(Of v) End Interface Public Interface derivedInterface(Of t1, t2) Inherits interfaceA(Of t1), interfaceX(Of t2) End Interface  
```  
  
 Wenn die Erstellung oder Implementierung von `derivedInterface` durch Angeben desselben Typs für `t1` und `t2` erfolgt, muss sie zwei Versionen von `interfaceX` mit identischen Typargumenten erben. Dies führt zu einer Mehrdeutigkeit in Bezug auf die Version, auf die zugegriffen werden soll.  
  
 **Fehler\-ID:** BC32121  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie eines der für die abgeleitete Schnittstelle angegebenen Typargumente, sodass kein Konflikt auftritt.  
  
     \- oder \-  
  
-   Entfernen Sie eine der Schnittstellen, die den potenziellen Vererbungs\- oder Implementierungskonflikt auslösen, aus der `Inherits`\-Anweisung.  
  
## Siehe auch  
 [NICHT IM BUILD: Übersicht über Schnittstellen](assetId:///f96bb470-c1b8-4c73-89bc-6f536b798da1)   
 [Interface Statement](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)   
 [Inherits Statement](../Topic/Inherits%20Statement.md)   
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)