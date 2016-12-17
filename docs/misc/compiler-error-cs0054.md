---
title: "Compilerfehler CS0054"
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
  - "CS0054"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0054"
ms.assetid: 49346f55-d887-497a-af71-be4cbbf1de24
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0054
Inkonsistenter Zugriff: Indexer\-Rückgabetyp „type“ ist weniger zugreifbar als Indexer „indexer“.  
  
 Ein public\-Konstrukt muss ein öffentlich zugreifbares Objekt zurückgeben. Weitere Informationen finden Sie unter [Zugriffsmodifizierer](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0054 generiert:  
  
```  
// CS0054.cs class MyClass // try the following line instead // public class MyClass { } public class MyClass3 { public MyClass this[int i]   // CS0054 { get { return new MyClass(); } } } public class MyClass2 { public static void Main() { } }  
```