---
title: "Compilerfehler CS1044"
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
  - "CS1044"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1044"
ms.assetid: 18fc1ff5-8b97-4c31-99a1-5985b8e58024
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1044
In einer for\-, using\-, fixed\- oder declaration\-Anweisung kann nur ein Typ verwendet werden.  
  
 Der Compiler hat eine ungültige Anweisung gefunden.  
  
 Im folgenden Beispiel wird CS1044 generiert:  
  
```  
// CS1044.cs using System; public class MyClass : IDisposable { public void Dispose() { Console.WriteLine("Res1.Dispose()"); } public static void Main() { using (MyClass mc1 = new MyClass(), MyClass mc2 = new MyClass())   // CS1044, remove an instantiation { } } }  
```