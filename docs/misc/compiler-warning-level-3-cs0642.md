---
title: "Compilerwarnung (Stufe 3) CS0642"
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
  - "CS0642"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0642"
ms.assetid: e2df58c0-9b7e-4e50-8e31-e0134955f62c
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 3) CS0642
Möglicherweise falsche leere Anweisung  
  
 Ein Semikolon nach einer bedingten Anweisung kann dazu führen, dass Ihr Code anders als beabsichtigt ausgeführt wird.  
  
 Sie können die Compileroption **\/nowarn** oder `#pragmas warning` verwenden, um diese Warnung zu deaktivieren; weitere Informationen finden Sie unter [\/nowarn \(Suppress Specified Warnings\)](../Topic/-nowarn%20\(C%23%20Compiler%20Options\).md) oder [\#pragma warning](../Topic/%23pragma%20warning%20\(C%23%20Reference\).md).  
  
 Im folgenden Beispiel wird CS0642 generiert:  
  
```  
// CS0642.cs // compile with: /W:3 class MyClass { public static void Main() { int i; for (i = 0; i < 10; i += 1);   // CS0642 semicolon intentional? { System.Console.WriteLine (i); } } }  
```