---
title: "Compilerfehler CS0557"
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
  - "CS0557"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0557"
ms.assetid: beca353e-4fea-4e4f-a48a-eddeebb153bb
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0557
Doppelte benutzerdefinierte Konvertierung in Typ 'Klasse'.  
  
 Doppelte Konvertierungsroutinen sind in einer Klasse nicht zulässig.  
  
 Im folgenden Beispiel wird CS0557 generiert:  
  
```  
// CS0557.cs namespace x { public class ii { public class iii { public static implicit operator int(iii aa) { return 0; } // CS0557, delete duplicate public static explicit operator int(iii aa) { return 0; } } public static void Main() { } } }  
```