---
title: "Compilerfehler CS0841"
ms.custom: na
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0841"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0841"
ms.assetid: eb67c244-a930-4291-ae2a-5832e8916ed7
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0841
Die Variable 'Name' kann erst verwendet werden, nachdem sie deklariert wurde.  
  
 Eine Variable muss deklariert werden, bevor sie verwendet werden kann.  
  
### So beheben Sie diesen Fehler  
  
1.  Verschieben Sie die Variablendeklaration vor die Zeile, in der der Fehler aufgetreten ist.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0841 generiert:  
  
```  
// cs0841.cs using System; public class C { public static int Main() { j = 5; // CS0841 int j; // To fix, move this line up. return 1; } }  
```