---
title: "Compilerfehler CS1535"
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
  - "CS1535"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1535"
ms.assetid: 19f41e78-9aea-4575-abd0-60ddb927276f
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1535
Der überladene unäre Operator "Operator" nimmt einen Parameter an.  
  
 Die Definition eines unären [überladbaren Operators](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md) muss einen\-Parameter annehmen.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1535 generiert:  
  
```  
// CS1535.cs class MyClass { // uncomment the method parameter to resolve CS1535 public static MyClass operator ++ (/*MyClass MC1*/)   // CS1535 { return new MyClass(); } public static int Main() { return 1; } }  
```