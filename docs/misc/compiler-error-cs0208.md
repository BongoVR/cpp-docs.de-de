---
title: "Compilerfehler CS0208"
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
  - "CS0208"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0208"
ms.assetid: 03534893-1522-4dab-9822-8b9ed97b3bd0
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0208
Es ist nicht möglich, einen Zeiger auf den verwalteten Typ \("Typ"\) zu deklarieren oder dessen Adresse oder Größe abzurufen.  
  
 Selbst bei Verwendung des [unsafe](../Topic/unsafe%20\(C%23%20Reference\).md)\-Schlüsselworts ist es nicht zulässig, die Adresse und Größe eines verwalteten Objekts abzurufen oder einen Zeiger auf einen verwalteten Typ zu deklarieren. Ein verwalteter Typ ist:  
  
-   ein beliebiger Verweistyp  
  
-   jede Struktur, die einen Verweistyp als Feld oder Eigenschaft enthält  
  
 Weitere Informationen finden Sie unter [Unsicherer Code und Zeiger](../Topic/Unsafe%20Code%20and%20Pointers%20\(C%23%20Programming%20Guide\).md) und [sizeof](../Topic/sizeof%20\(C%23%20Reference\).md).  
  
## Beispiel  
 Im folgenden Beispiel wird CS0208 generiert:  
  
```  
// CS0208.cs // compile with: /unsafe class myClass { public int a = 98; } struct myProblemStruct { string s; float f; } struct myGoodStruct { int i; float f; } public class MyClass { unsafe public static void Main() { // myClass is a class, a managed type. myClass s = new myClass(); myClass* s2 = &s;    // CS0208 // The struct contains a string, a managed type. int i = sizeof(myProblemStruct); //CS0208 // The struct contains only value types. i = sizeof(myGoodStruct); //OK } }  
  
```  
  
## Siehe auch  
 [sizeof](../Topic/sizeof%20\(C%23%20Reference\).md)