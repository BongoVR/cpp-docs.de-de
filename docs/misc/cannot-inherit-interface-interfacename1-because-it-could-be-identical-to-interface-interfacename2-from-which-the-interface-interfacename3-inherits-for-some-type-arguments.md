---
title: "Die Schnittstelle &#39;&lt;Schnittstellennname1&gt;&#39; kann nicht geerbt werden, da sie mit Schnittstelle &#39;&lt;Schnittstellennname2&gt;&#39; identisch sein kann, von der die Schnittstelle &#39;&lt;Schnittstellennname3&gt;&#39; einige Typargumente erbt."
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
  - "bc32123"
  - "vbc32123"
helpviewer_keywords: 
  - "BC32123"
ms.assetid: 2b8fa1f0-3d43-45c6-99d0-328151479b43
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "shoag"
manager: "wpickett"
---
# Die Schnittstelle &#39;&lt;Schnittstellennname1&gt;&#39; kann nicht geerbt werden, da sie mit Schnittstelle &#39;&lt;Schnittstellennname2&gt;&#39; identisch sein kann, von der die Schnittstelle &#39;&lt;Schnittstellennname3&gt;&#39; einige Typargumente erbt.
Eine generische Schnittstelle erbt von mindestens zwei generischen Schnittstellen, und zwei der Vererbungen können einen Konflikt mit bestimmten Werten von Typargumenten verursachen.  
  
 Dieser Fehler kann durch die folgenden Anweisungen generiert werden.  
  
```  
Public Interface interfaceA(Of u) End Interface Public Interface interfaceX(Of v) Inherits interfaceA(Of v) End Interface Public Interface derivedInterface(Of t1, t2) Inherits interfaceA(Of t1), interfaceX(Of t2) End Interface  
```  
  
 Wenn die Erstellung oder Implementierung von `derivedInterface` durch Angeben desselben Typs für `t1` und `t2` erfolgt, muss sie zwei Versionen von `interfaceA` mit identischen Typargumenten erben. Dies führt zu einer Mehrdeutigkeit in Bezug auf die Version, auf die zugegriffen werden soll.  
  
 **Fehler\-ID:** BC32123  
  
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