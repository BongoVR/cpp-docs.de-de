---
title: "Compilerfehler CS1012"
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
  - "CS1012"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1012"
ms.assetid: 4acc5fe0-da47-4882-b7d8-557767d7cf03
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1012
Zu viele Zeichen im Zeichenliteral.  
  
 Es wurde versucht, eine [Char](../Topic/char%20\(C%23%20Reference\).md)\-Konstante mit mehr als einem Zeichen zu initialisieren.  
  
 CS1012 kann auch bei der Datenbindung auftreten. Die folgende Zeile gibt z. B. ein Fehler zurück:  
  
 `<%# DataBinder.Eval(Container.DataItem, 'doctitle') %>`  
  
 Verwenden Sie stattdessen folgende Zeile:  
  
 `<%# DataBinder.Eval(Container.DataItem, "doctitle") %>`  
  
 Im folgenden Beispiel wird CS1012 generiert.  
  
```  
// CS1012.cs class Sample { static void Main() { char a = 'xx';   // CS1012 char a2 = 'x';   // OK System.Console.WriteLine(a2); } }  
```