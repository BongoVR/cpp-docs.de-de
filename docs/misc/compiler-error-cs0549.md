---
title: "Compilerfehler CS0549"
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
  - "CS0549"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0549"
ms.assetid: ae965019-9dee-4f28-9e9a-6f379bd0d757
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0549
'funktion' ist ein neuer virtueller Member in einer versiegelten Klasse 'klasse'.  
  
 Eine [versiegelte](../Topic/sealed%20\(C%23%20Reference\).md) [Klasse](../Topic/class%20\(C%23%20Reference\).md) kann nicht als Basisklasse verwendet werden.  Daher haben virtuelle Methoden in versiegelten Klassen keinen Nutzen.  
  
 Im folgenden Beispiel wird CS0549 generiert:  
  
```  
// CS0549.cs // compile with: /target:library sealed public class MyClass { virtual public void TestMethod() {}   // CS0549 public void TestMethod2() {}   // OK }  
```