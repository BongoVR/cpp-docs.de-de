---
title: "Ein Typparameter ist in einer Implements-Klausel nicht zul&#228;ssig."
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
  - "vbc32056"
  - "bc32056"
helpviewer_keywords: 
  - "BC32056"
ms.assetid: a62d773b-e878-4817-8638-da49849477d7
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Ein Typparameter ist in einer Implements-Klausel nicht zul&#228;ssig.
Eine `Implements`\-Klausel in einem generischen Typ gibt einen Typparameter als zu implementierenden Member an.  
  
 Eine `Implements`\-Klausel muss eine Schnittstelle und einen Member angegeben. Sie kann einen Typparameter an die Schnittstelle übergeben, aber sie kann ihn nicht an den Member übergeben oder als den Namen des Members verwenden.  
  
 Dieser Fehler kann durch die folgenden Anweisungen generiert werden.  
  
```  
Class c1(Of t) Implements i1(Of t) Public Sub doSomething() Implements t End Class  
```  
  
 **Fehler\-ID:** BC32056  
  
### So beheben Sie diesen Fehler  
  
-   Geben Sie nach dem `Implements`\-Schlüsselwort den Schnittstellennamen und einen echten Member der Schnittstelle an. Sie können den Typparameter ggf. an die Schnittstelle übergeben.  
  
    ```  
    Public Sub doSomething() Implements i1(Of t).doSomething  
    ```  
  
## Siehe auch  
 [Implements](../Topic/Implements%20Clause%20\(Visual%20Basic\).md)   
 [NICHT IM BUILD: Implements\-Schlüsselwort und Implements\-Anweisung](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)   
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)