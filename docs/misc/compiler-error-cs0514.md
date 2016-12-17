---
title: "Compilerfehler CS0514"
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
  - "CS0514"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0514"
ms.assetid: 74ce3010-f9e9-458c-8b68-cfb908a3e7a2
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0514
"constructor": Ein statischer Konstruktor kann keinen expliziten this\- oder base\-Konstruktoraufruf enthalten.  
  
 Das Aufrufen von `this` im statischen Konstruktor ist nicht zulässig, da der statische Konstruktor vor dem Erstellen einer Instanz der Klasse automatisch aufgerufen wird. Außerdem werden statische Konstruktoren nicht geerbt und können nicht direkt aufgerufen werden.  
  
 Weitere Informationen finden Sie unter [this](../Topic/this%20\(C%23%20Reference\).md) und [Basis](../Topic/base%20\(C%23%20Reference\).md).  
  
## Beispiel  
 Im folgenden Beispiel wird CS0514 generiert:  
  
```  
// CS0514.cs class A { static A() : base(0) // CS0514 { } public A(object o) { } } class B { static B() : this(null) // CS0514 { } public B(object o) { } }  
```