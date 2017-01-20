---
title: "Compilerwarnung (Stufe 4) CS0078"
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
  - "CS0078"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0078"
ms.assetid: 8d637be6-82bc-462c-bec5-217327bc8c40
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 4) CS0078
Das l\-Suffix kann leicht mit der Zahl 1 verwechselt werden. Verwenden Sie zur deutlichen Unterscheidung das L.  
  
 Der Compiler gibt eine Warnung aus, wenn eine long\-Umwandlung unter Verwendung des Kleinbuchstabens l anstelle des Großbuchstabens L erkannt wird.  
  
 Im folgenden Beispiel wird CS0078 generiert:  
  
```  
// CS0078.cs // compile with: /W:4 class test { public static void TestL(long i) { } public static void TestL(int i) { } public static void Main() { TestL(25l);   // CS0078 // try the following line instead // TestL(25L); } }  
```