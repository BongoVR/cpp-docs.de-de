---
title: "Compilerfehler CS0515"
ms.custom: na
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0515"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0515"
ms.assetid: 0f8c0253-218d-4c21-b22c-fa5802ba4e7f
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0515
"Funktion": Zugriffsmodifizierer sind bei statischen Konstruktoren nicht zulässig.  
  
 Ein statischer Konstruktor kann keinen [Zugriffsmodifizierer](../Topic/Modifiers%20\(C%23%20Reference\).md) enthalten.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0515 generiert:  
  
```  
// CS0515.cs public class Clx { public static void Main() { } } public class Clz { public static Clz()   // CS0515, remove public keyword { } }  
```