---
title: "Compilerfehler CS0080"
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
  - "CS0080"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0080"
ms.assetid: 99035371-37d1-48b2-a8b9-e8a1ebd04f0f
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0080
Einschränkungen sind für nicht generische Deklarationen nicht zulässig.  
  
 Die gefundene Syntax darf nur in einer generischen Deklaration verwendet werden, um Einschränkungen auf den Typparameter anzuwenden. Weitere Informationen finden Sie unter [Generika](../Topic/Generics%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0080 generiert, weil MyClass keine generische Klasse und Foo keine generische Methode.  
  
```  
namespace MyNamespace { public class MyClass where MyClass : System.IDisposable // CS0080    //the following line shows an example of correct syntax //public class MyClass<T> where T : System.IDisposable { public void Foo() where Foo : new() // CS0080 //the following line shows an example of correct syntax //public void Foo<U>() where U : struct { } } public class Program { public static void Main() { } } }  
```