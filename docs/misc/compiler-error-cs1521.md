---
title: "Compilerfehler CS1521"
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
  - "CS1521"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1521"
ms.assetid: 9a482b33-24f2-4654-81b4-be40bf56d624
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1521
Ungültiger Basistyp.  
  
 Eine [Basis](../Topic/base%20\(C%23%20Reference\).md)klassenspezifikation ist nicht ordnungsgemäß formatiert.  
  
 Im folgenden Beispiel wird CS1521 generiert:  
  
```  
// CS1521.cs class CMyClass { public static void Main() { } } class CMyClass1 : CMyClass     // OK { } class CMyClass2 : CMyClass[]   // CS1521 { } class CMyClass3 : CMyClass*    // CS1521 { }  
```