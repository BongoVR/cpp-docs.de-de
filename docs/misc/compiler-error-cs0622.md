---
title: "Compilerfehler CS0622"
ms.custom: na
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0622"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0622"
ms.assetid: aef77a69-d8b7-41f8-9539-258deaef5cc4
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0622
Arrayinitialisiererausdrücke können nur für die Zuweisung zu Arraytypen verwendet werden. Verwenden Sie stattdessen einen neuen Ausdruck.  
  
 Die zum Initialisieren eines Arrays angemessene Syntax wurde in der Deklaration von etwas anderem als einem Array verwendet.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0622 generiert:  
  
```  
// CS0622.cs using System; public class Test { public static void Main () { Test t = { new Test() };   // CS0622 // Try the following instead: // Test[] t = { new Test() }; } }  
```