---
title: "Compilerfehler CS0022"
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
  - "CS0022"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0022"
ms.assetid: 531c3ed2-0d75-4046-8d57-89f79381af8e
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0022
Falsche Indexanzahl in \[\]. \<Zahl\> wurde erwartet  
  
 In einem Vorgang, in dem auf ein Array zugegriffen wird, war innerhalb der eckigen Klammern eine falsche Anzahl von Dimensionen angegeben. Weitere Informationen finden Sie unter [Arrays](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md).  
  
## Beispiel  
 Im folgenden Beispiel wird CS0022 generiert:  
  
```  
// CS0022.cs public class MyClass { public static void Main() { int[] a = new int[10]; a[0] = 0;     // single-dimension array a[0,1] = 9;   // CS0022, the array does not have two dimensions } }  
```