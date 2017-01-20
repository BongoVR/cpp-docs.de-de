---
title: "Compilerfehler CS1586"
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
  - "CS1586"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1586"
ms.assetid: 408a4495-6fe6-4e95-a49f-a4d041675fff
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1586
Für die Arrayerstellung ist eine Arraygröße oder ein Arrayinitialisierer erforderlich.  
  
 Ein Array wurde falsch deklariert.  
  
 Im folgenden Beispiel wird CS1586 generiert:  
  
```  
// CS1586.cs using System; class MyClass { public static void Main() { int[] a = new int[];   // CS1586 // try the following line instead int[] b = new int[5]; } }  
```  
  
## Siehe auch  
 [Arrays](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md)