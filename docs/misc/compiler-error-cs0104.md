---
title: "Compilerfehler CS0104"
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
  - "CS0104"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0104"
ms.assetid: 1a7e9ae8-308b-441b-ba85-fac974222875
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0104
"Verweis" ist ein mehrdeutiger Verweis und kann "Bezeichner" oder "Bezeichner" sein.  
  
 Das Programm enthält [using](../Topic/using%20\(C%23%20Reference\).md)\-Anweisungen für zwei Namespaces, und im Code wird auf einen Namen verwiesen, der in beiden Namespaces enthalten ist.  
  
 Im folgenden Beispiel wird CS0104 generiert:  
  
```  
// CS0104.cs using x; using y; namespace x { public class Test { } } namespace y { public class Test { } } public class a { public static void Main() { Test test = new Test();   // CS0104, is Test in x or y namespace? // try the following line instead // y.Test test = new y.Test(); } }  
```