---
title: "Compilerfehler CS0077"
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
  - "CS0077"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0077"
ms.assetid: 55d3d290-d172-41a3-b326-ebf5a0a7e81f
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0077
Der as\-Operator muss mit einem Referenztyp oder einem Typ, der NULL\-Werte zulässt, verwendet werden. \("int" ist ein Werttyp, der keine NULL\-Werte zulässt.\)  
  
 An den [as](../Topic/as%20\(C%23%20Reference\).md)\-Operator wurde ein [Werttyp](../Topic/Value%20Types%20\(C%23%20Reference\).md) übergeben. Da `as`[null](../Topic/null%20\(C%23%20Reference\).md) zurückgeben kann, dürfen nur [Verweistypen](../Topic/Reference%20Types%20\(C%23%20Reference\).md) oder ein Typ, der NULL\-Werte zulässt, an ihn übergeben werden. Weitere Informationen über Typen, die NULL\-Werte zulassen, finden Sie unter [Typen, die NULL\-Werte zulassen](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0077 generiert:  
  
```  
// CS0077.cs using System; class C { } struct S { } class M { public static void Main() { object o1, o2; C c; S s; o1 = new C(); o2 = new S(); s = o2 as S;  // CS0077, S is not a reference type. // try the following line instead // c = o1 as C; } }  
```