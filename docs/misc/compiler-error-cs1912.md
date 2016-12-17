---
title: "Compilerfehler CS1912"
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
  - "CS1912"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1912"
ms.assetid: 6205420e-01b9-4470-89f9-5924f1e49108
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1912
Doppelte Initialisierung des Members 'Name'.  
  
 Ein Objektinitialisierer kann einzelne Member nur einmal initialisieren.  
  
### So beheben Sie diesen Fehler  
  
1.  Entfernen Sie die zweite Initialisierung des Members aus dem Objektinitialisierer.  
  
## Beispiel  
 Der folgende Code generiert CS1912 da `memberA` zweimal initialisiert wird:  
  
```  
// cs1912.cs using System.Linq; public class TestClass { public int memberA { get; set; } public int memberB { get; set; } } public class Test { static void Main() { TestClass tc = new TestClass() { memberA = 5, memberA = 6, memberB = 2}; // CS1912 } }  
```  
  
## Siehe auch  
 [Objekt\- und Auflistungsinitialisierer](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)