---
title: "Compilerfehler CS1902"
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
  - "CS1902"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1902"
ms.assetid: 120c5978-9ebc-4ec1-bcec-f840af6fdf5d
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1902
Ungültige Option "Option" für \/debug. Muss entweder "full" oder "pdbonly" sein.  
  
 Eine ungültige Option wurde an die [\/debug](../Topic/-debug%20\(C%23%20Compiler%20Options\).md)\-Compileroption übergeben.  
  
 Im folgenden Beispiel wird CS1902 generiert:  
  
```  
// CS1902.cs // compile with: /debug:x // CS1902 expected class x { public static void Main() { } }  
```