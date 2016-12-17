---
title: "Compilerfehler CS0263"
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
  - "CS0263"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0263"
ms.assetid: 94fe3eb0-10e9-4602-a993-68fe125c8565
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0263
Partielle Deklarationen von 'typ' dürfen keine unterschiedlichen Basisklassen angeben.  
  
 Wenn ein Typ in partiellen Deklarationen definiert wird, geben Sie in jeder der partiellen Deklarationen die gleichen Basistypen an. Weitere Informationen finden Sie unter [Partielle Klassen und Methoden](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0263 generiert:  
  
```  
  
// CS0263.cs // compile with: /target:library class B1 { } class B2 { } partial class C : B1  // CS0263 – is the base class B1 or B2? { } partial class C : B2 { }  
```