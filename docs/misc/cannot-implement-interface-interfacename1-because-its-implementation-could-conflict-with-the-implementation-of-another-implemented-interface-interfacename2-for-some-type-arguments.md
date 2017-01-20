---
title: "Die Schnittstelle &#39;&lt;schnittstellenname1&gt;&#39; kann nicht implementiert werden, da ihre Implementierung aufgrund einiger Typargumente einen Konflikt mit der ebenfalls implementierten Schnittstelle &#39;&lt;schnittstellenname2&gt;&#39; verursachen w&#252;rde"
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
  - "BC32072"
  - "vbc32072"
helpviewer_keywords: 
  - "BC32072"
ms.assetid: af1cc688-c8cf-4cb2-a8a9-310f5139fe7b
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Die Schnittstelle &#39;&lt;schnittstellenname1&gt;&#39; kann nicht implementiert werden, da ihre Implementierung aufgrund einiger Typargumente einen Konflikt mit der ebenfalls implementierten Schnittstelle &#39;&lt;schnittstellenname2&gt;&#39; verursachen w&#252;rde
Eine Klassendeklaration enthält eine `Implements`\-Anweisung, die zwei oder mehr Schnittstellen angibt, aber mindestens eine der Schnittstellen ist generisch, und zwei der Implementierungen könnten bei bestimmten Werten der Typargumente im Konflikt stehen.  
  
 Dieser Fehler kann durch die folgenden Anweisungen generiert werden.  
  
```  
Public Interface iFace1 Sub testSub(ByVal arg As String) End Interface Public Interface iFace2(Of t) Sub testSub(ByVal arg As t) End Interface Public Class testClass Implements iFace1, iFace2(Of String) End Class  
```  
  
 Da `iFace2` mithilfe von `String` konstruiert wird, muss `testClass` zwei Versionen von `testSub` mit identischen Signaturen implementieren. Dies führt zu einer Mehrdeutigkeit in Bezug auf die Version, auf die zugegriffen werden soll.  
  
 **Fehler\-ID:** BC32072  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie das der generischen Schnittstelle übergebene Typargument so, dass kein Konflikt auftritt.  
  
     \- oder \-  
  
-   Entfernen Sie die `Implements`\-Anweisung aus einer der Schnittstellen, die zum Konflikt bei der Implementierung führen.  
  
## Siehe auch  
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Interface Statement](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Implements Statement](../Topic/Implements%20Statement.md)   
 [NICHT IM BUILD: Implements\-Schlüsselwort und Implements\-Anweisung](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)   
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)