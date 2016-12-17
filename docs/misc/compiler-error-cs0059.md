---
title: "Compilerfehler CS0059"
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
  - "CS0059"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0059"
ms.assetid: 25a8624b-7f7b-4487-ba80-413d57f9132b
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0059
Inkonsistenter Zugriff: Parametertyp 'Typ' ist weniger zugreifbar als Delegat 'Delegat'.  
  
 Der Rückgabetyp und alle Typen, auf die in der Liste der formalen Parameter einer Methode verwiesen wird, müssen mindestens dieselben Zugriffsmöglichkeiten bieten wie die Methode selbst. Weitere Informationen finden Sie unter [Zugriffsmodifizierer](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
## Beispiel  
 Im folgenden Beispiel wird CS0059 generiert:  
  
```  
// CS0059.cs class MyClass //defaults to private accessibility // try the following line instead // public class MyClass { } public delegate void MyClassDel( MyClass myClass);   // CS0059 public class Program { public static void Main() { } }  
```