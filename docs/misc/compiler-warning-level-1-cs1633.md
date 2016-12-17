---
title: "Compilerwarnung (Stufe 1) CS1633"
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
  - "CS1633"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1633"
ms.assetid: f31db218-f880-4fc4-ab34-8bcdc49011da
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 1) CS1633
Unbekannte \#pragma\-Direktive.  
  
 Das verwendete Pragma gehörte nicht zu den bekannten Pragmas, die vom C\#\-Compiler unterstützt werden. Verwenden Sie zum Beheben dieses Fehlers nur unterstützte Pragmas.  
  
 Im folgenden Beispiel wird CS1633 generiert:  
  
```  
// CS1633.cs // compile with: /W:1 #pragma unknown  // CS1633 class C { public static void Main() { } }  
```