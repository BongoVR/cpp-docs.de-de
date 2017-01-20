---
title: "Compilerfehler CS1554"
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
  - "CS1554"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1554"
ms.assetid: 81e8d4ac-cdbf-4b75-8932-0bc271a8405c
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1554
Ungültige Deklaration. Verwenden Sie stattdessen „\<Typ\> operator op \(...“.  
  
 Der Rückgabetyp für einen benutzerdefinierten [Operator](../Topic/operator%20\(C%23%20Reference\)2.md) muss vor dem Schlüsselwort „operator“ angezeigt werden.  
  
 Im folgenden Beispiel wird CS1554 generiert:  
  
```  
// CS1554.cs class MyClass { public static operator ++ MyClass (MyClass f)    // CS1554 // try the following line instead // public static MyClass operator ++ (MyClass f) { return new MyClass (); } public static void Main() { } }  
```