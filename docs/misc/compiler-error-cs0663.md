---
title: "Compilerfehler CS0663"
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
  - "CS0663"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0663"
ms.assetid: 9f96c42b-dcc8-4a0f-8404-289fc88dba5e
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0663
Kann keine überladenen Methoden definieren, die sich nur in "ref" und "out" unterscheiden.  
  
 Methoden, die sich nur in ihrer Verwendung von [ref](../Topic/ref%20\(C%23%20Reference\).md) und [out](../Topic/out%20\(C%23%20Reference\).md) für einen Parameter unterscheiden, sind nicht zulässig.  
  
 Im folgenden Beispiel wird CS0663 generiert:  
  
```  
// CS0663.cs class TestClass { public static void Main() { } public void Test(ref int i) { } public void Test(out int i)   // CS0663 { } }  
```