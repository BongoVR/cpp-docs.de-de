---
title: "Compilerfehler CS0060"
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
  - "CS0060"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0060"
ms.assetid: ae6d4fb7-5ff9-4883-82c3-f55b190f439a
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0060
Inkonsistenter Zugriff: Die Basisklasse 'klasse1' ist weniger zugreifbar als die Klasse 'klasse2'  
  
 Der Klassenzugriff sollte zwischen Basisklasse und geerbter Klasse konsistent sein.  
  
 Im folgenden Beispiel wird CS0060 generiert:  
  
```  
// CS0060.cs class MyClass // try the following line instead // public class MyClass { } public class MyClass2 : MyClass   // CS0060 { public static void Main() { } }  
```  
  
## Siehe auch  
 [Zugriffsmodifizierer](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)