---
title: "Compilerfehler CS0670"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0670"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0670"
ms.assetid: 59379171-284f-4d55-8741-af6a97879abc
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0670
Ein Feld kann keinen void\-Typ aufweisen.  
  
 Ein Feld wurde als Typ [void](../Topic/void%20\(C%23%20Reference\).md) deklariert.  
  
 Im folgenden Beispiel wird CS0670 generiert:  
  
```  
// CS0670.cs class C { void f;   // CS0670 // try the following line instead // public int f; public static void Main() { C myc = new C(); myc.f = 0; } }  
```