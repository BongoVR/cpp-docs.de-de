---
title: "Compilerfehler CS0110"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0110"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0110"
ms.assetid: 0bfe7071-1194-4142-a1a1-6190ee92b1d4
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0110
Die Auswertung des Konstantenwerts für "const\-Deklaration" bezieht eine zirkuläre Definition ein.  
  
 Die Deklaration einer [const](../Topic/const%20\(C%23%20Reference\).md)\-Variablen \(`a`\) kann auf keine weitere const\-Variable \(`b`\) verweisen, die auch auf \(`a`\) verweist.  
  
 Im folgenden Beispiel wird CS0110 generiert:  
  
```  
// CS0110.cs namespace MyNamespace { public class A { public static void Main() { } } public class B : A { public const int i = c + 1;   // CS0110, c already references i public const int c = i + 1; // the following line would be OK // public const int c = 10; } }  
```  
  
## Siehe auch  
 [Konstanten](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)