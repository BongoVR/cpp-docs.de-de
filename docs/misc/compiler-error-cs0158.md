---
title: "Compilerfehler CS0158"
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
  - "CS0158"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0158"
ms.assetid: 88ac61a9-ce55-4272-9141-0873765a7034
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0158
Die Bezeichnung "Bezeichnung" führt Shadowing für eine andere Bezeichnung mit demselben Namen in einem enthaltenen Gültigkeitsbereich durch.  
  
 Eine Bezeichnung in einem inneren Gültigkeitsbereich verdeckt eine Bezeichnung mit demselben Namen in einem äußeren Gültigkeitsbereich. Weitere Informationen finden Sie unter [goto](../Topic/goto%20\(C%23%20Reference\).md).  
  
 Im folgenden Beispiel wird CS0158 generiert:  
  
```  
// CS0158.cs namespace MyNamespace { public class MyClass { public static void Main() { goto lab1; lab1: { lab1: goto lab1;   // CS0158 } } } }  
```