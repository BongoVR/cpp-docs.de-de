---
title: "Compilerfehler CS0236"
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
  - "CS0236"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0236"
ms.assetid: 1522c421-744f-441f-9e05-6bb31311ab2a
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0236
Ein Feldinitialisierer kann nicht auf das nicht statische Feld bzw. die nicht statische Methode oder Eigenschaft "Feld" verweisen.  
  
 Instanzfelder können nicht dazu verwendet werden, andere Instanzfelder außerhalb einer Methode zu initialisieren. Wenn Sie versuchen, eine Variable außerhalb einer Methode zu initialisieren, sollten Sie überlegen, die Initialisierung im Klassenkonstruktor vorzunehmen. Weitere Informationen finden Sie unter [Methoden](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0236 generiert:  
  
```  
// CS0236.cs public class MyClass { public int i = 5; public int j = i;  // CS0236 public int k;      // initialize in constructor MyClass() { k = i; } public static void Main() { } }  
```