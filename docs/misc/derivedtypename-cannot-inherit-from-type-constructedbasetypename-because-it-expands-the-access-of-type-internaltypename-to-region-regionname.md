---
title: "&#39;&lt;Abgeleiteter_Typname&gt;&#39; erweitert den Zugriff des &#39;&lt;Interner_Typname&gt;&#39;-Typs auf die Region &lt;Region&gt; &#39;&lt;Regionsname&gt;&#39; und kann daher nicht vom &#39;&lt;Konstruierter_Basistypname&gt;&#39;-&lt;Typ&gt; erben."
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
  - "vbc30921"
  - "BC30921"
helpviewer_keywords: 
  - "BC30921"
ms.assetid: b0dd971a-80e2-4d37-925b-854d17411546
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;Abgeleiteter_Typname&gt;&#39; erweitert den Zugriff des &#39;&lt;Interner_Typname&gt;&#39;-Typs auf die Region &lt;Region&gt; &#39;&lt;Regionsname&gt;&#39; und kann daher nicht vom &#39;&lt;Konstruierter_Basistypname&gt;&#39;-&lt;Typ&gt; erben.
Eine abgeleitete Klasse oder Schnittstelle versucht, die Zugriffsebene eines internen Typs zu erweitern, indem sie diesen als Typargument für eine Basisklasse oder Schnittstelle verwendet.  
  
 Dieser Fehler kann durch folgenden Code generiert werden.  
  
```  
Public Class containingClass Public Class baseClass(Of t) End Class Friend Class derivedClass Inherits baseClass(Of internalStructure) End Class Private Structure internalStructure Dim firstMember As Integer End Structure End Class  
```  
  
 Code außerhalb der `containingClass` darf nicht auf die `internalStructure` zugreifen. Allerdings kann jeder Code in derselben Assembly auf die `derivedClass` zugreifen. Daher kann die `derivedClass` die `baseClass` nicht erben, wenn sie die `internalStructure` als Typargument verwendet, da auf diese Weise die `internalStructure` in der gesamten definierenden Coderegion verfügbar gemacht würde.  
  
 **Fehler\-ID:** BC30921  
  
### So beheben Sie diesen Fehler  
  
-   Passen Sie die Zugriffsebenen der Klassen oder Schnittstellen so an, dass der abgeleitete Typ die Zugriffsebene des internen Typs nicht erweitert.  
  
     \- oder \-  
  
-   Wenn Sie die Zugriffsebenen nicht anpassen können, verwenden Sie beim Erstellen der Basisklasse oder Schnittstelle den internen Typ nicht als Typargument.  
  
## Siehe auch  
 [Inherits Statement](../Topic/Inherits%20Statement.md)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)   
 [Access Levels in Visual Basic](../Topic/Access%20Levels%20in%20Visual%20Basic.md)   
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)