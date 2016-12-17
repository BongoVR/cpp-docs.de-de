---
title: "Compilerfehler CS0539"
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
  - "CS0539"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0539"
ms.assetid: 41b8975c-abd1-4a36-98a4-8efa5fb0502a
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0539
"Member" in der expliziten Schnittstellendeklaration ist kein Member der Schnittstelle.  
  
 Es wurde versucht, explizit ein [Schnittstellen](../Topic/interface%20\(C%23%20Reference\).md)\-Member zu deklarieren, das nicht vorhanden ist. Sie sollten die Deklaration entweder löschen oder so ändern, dass sie auf einen gültigen Schnittstellenmember verweist.  
  
 Im folgenden Beispiel wird CS0539 generiert:  
  
```  
// CS0539.cs namespace x { interface I { void m(); } public class clx : I { void I.x()   // CS0539 { } public static int Main() { return 0; } } }  
```