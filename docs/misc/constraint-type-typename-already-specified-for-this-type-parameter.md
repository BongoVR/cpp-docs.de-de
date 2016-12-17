---
title: "Der Einschr&#228;nkungstyp &quot;&lt;Typname&gt;&quot; wurde bereits f&#252;r diesen Typparameter angegeben"
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
  - "BC32071"
  - "vbc32071"
helpviewer_keywords: 
  - "BC32071"
ms.assetid: 6b0e85e9-3ac8-4181-97de-ca690b95a63c
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Der Einschr&#228;nkungstyp &quot;&lt;Typname&gt;&quot; wurde bereits f&#252;r diesen Typparameter angegeben
Eine Einschränkungsliste enthält eine Klassen\- oder Schnittstelleneinschränkung mehrfach.  
  
 Eine Einschränkungsliste erzwingt Anforderungen an das Typargument, das an den Typparameter übergeben wird. Sie können die folgenden Anforderungen in beliebiger Kombination angeben:  
  
-   Das Typargument muss mindestens eine Schnittstelle implementieren.  
  
-   Das Typargument darf von höchstens einer Klasse erben.  
  
 Ein Typ kann denselben Typ nicht mehrmals implementieren oder mehrmals von diesem erben, und Sie können einen Typ nur einmal in derselben Einschränkungsliste angeben.  
  
 **Fehler\-ID:** BC32071  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie alle redundanten Angaben derselben Klasse oder Schnittstelle. Die Angabe darf nur einmal in der Einschränkungsliste enthalten sein.  
  
## Siehe auch  
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)