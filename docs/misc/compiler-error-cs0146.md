---
title: "Compilerfehler CS0146"
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
  - "CS0146"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0146"
ms.assetid: 2be796e5-da2c-4939-af12-3145cd1828c8
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0146
Basisklassen\-Ringabhängigkeit zwischen 'Klasse1' und 'Klasse2'  
  
 Die Vererbungsliste für eine Klasse enthält einen direkten oder indirekten Verweis auf sich selbst. Eine Klasse kann nicht von sich selbst erben. Weitere Informationen finden Sie unter [Vererbung](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0146 generiert:  
  
```  
// CS0146.cs namespace MyNamespace { public interface InterfaceA { } public class MyClass : InterfaceA, MyClass2 { public void Main() { } } public class MyClass2 : MyClass   // CS0146 { } }  
```