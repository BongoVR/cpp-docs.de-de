---
title: "Compilerfehler CS0238"
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
  - "CS0238"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0238"
ms.assetid: 9b50c6e2-2c3f-431d-bdb7-557b0ec51626
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0238
"Member" ist keine Überschreibung und kann daher nicht versiegelt werden.  
  
 [sealed](../Topic/sealed%20\(C%23%20Reference\).md) wurde auf einen Member angewendet, der nicht gleichzeitig durch [override](../Topic/override%20\(C%23%20Reference\).md) gekennzeichnet war. Weitere Informationen finden Sie unter [Vererbung](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0238 generiert:  
  
```  
// CS0238.cs abstract class MyClass { public abstract void f(); } class MyClass2 : MyClass { public static void Main() { } public sealed void f() // CS0238 // Try the following definition instead: // public override sealed void f() { } }  
```