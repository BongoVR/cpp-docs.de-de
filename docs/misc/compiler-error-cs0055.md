---
title: "Compilerfehler CS0055"
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
  - "CS0055"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0055"
ms.assetid: 4d98abf3-2690-4418-8fd0-50c0e67d0a4a
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0055
Inkonsistenter Zugriff: Parametertyp „type“ ist weniger zugreifbar als Indexer „indexer“.  
  
 Ein public\-Konstrukt muss ein öffentlich zugreifbares Objekt zurückgeben. Weitere Informationen finden Sie unter [Zugriffsmodifizierer](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0055 generiert:  
  
```  
// CS0055.cs class MyClass //defaults to private accessibility // try the following line instead // public class MyClass { } public class MyClass2 { public int this[MyClass myClass]   // CS0055 { get { return 0; } } } public class MyClass3 { public static void Main() { } }  
```