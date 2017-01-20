---
title: "Compilerfehler CS0242"
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
  - "CS0242"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0242"
ms.assetid: bc86a5a4-89c1-4de4-a874-4dd4cbf592c2
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0242
Der Vorgang ist für void\-Zeiger nicht definiert.  
  
 Das Inkrementieren von void\-Zeigern ist nicht zulässig. Weitere Informationen finden Sie unter [Unsicherer Code und Zeiger](../Topic/Unsafe%20Code%20and%20Pointers%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0242 generiert:  
  
```  
// CS0242.cs // compile with: /unsafe class TestClass { public unsafe void Test() { void * p = null; p++;   // CS0242, incrementing a void pointer not allowed } public static void Main() { } }  
```