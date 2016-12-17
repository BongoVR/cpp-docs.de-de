---
title: "Compilerfehler CS0838"
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
  - "CS0838"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0838"
ms.assetid: 22495e47-3331-42ef-921c-f76ff03ef1f7
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0838
Eine Ausdrucksbaumstruktur darf keinen Initialisierer mehrdimensionaler Arrays enthalten.  
  
 Mehrdimensionale Arrays in Ausdrucksbaumstrukturen können nicht mit einem Arrayinitialisierer initialisiert werden.  
  
### So beheben Sie diesen Fehler  
  
1.  Erstellen und initialisieren Sie das Array vor dem Erstellen der Ausdrucksbaumstruktur.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0838 generiert:  
  
```  
// cs0838.cs using System; using System.Linq; using System.Linq.Expressions; namespace TestNamespace { class Test { static int Main() { Expression<Func<int[,]>> expr = () => new int[2, 2] { { 1, 2 }, { 3, 4 } }; // CS0838 // try the following 2 lines instead int[,] nums = new int[2, 2] { { 1, 2 }, { 3, 4 } }; Expression<Func<int[,]>> expr2 = () => nums; return 1; } } }  
  
```  
  
## Siehe auch  
 [Ausdrucksbaumstrukturen](../Topic/Expression%20Trees%20\(C%23%20and%20Visual%20Basic\).md)