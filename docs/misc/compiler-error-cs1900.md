---
title: "Compilerfehler CS1900"
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
  - "CS1900"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1900"
ms.assetid: 08141138-bfea-4af3-a9a0-ec54cf2caa13
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1900
Die Warnstufe muss zwischen 0 und 4 liegen.  
  
 Die Compileroption [\/warn](../Topic/-warn%20\(C%23%20Compiler%20Options\).md) kann nur einen der fünf möglichen Werte \(0, 1, 2, 3 oder 4\) annehmen. Jeder andere an **\/warn** übergebene Wert verursacht den Fehler CS1900.  
  
 Im folgenden Beispiel wird CS1900 generiert:  
  
```  
// CS1900.cs // compile with: /W:5 // CS1900 expected class x { public static void Main() { } }  
```