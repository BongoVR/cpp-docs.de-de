---
title: "Compilerwarnung (Stufe 3) CS0168"
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
  - "CS0168"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0168"
ms.assetid: 6f5b7fe3-1e91-462f-8a73-b931327ab3f5
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 3) CS0168
Die Variable "Var" ist zugewiesen, ihr Wert wird aber nie verwendet  
  
 Der Compiler gibt eine Warnung aus, wenn eine Variable deklariert wurde, aber nicht verwendet wird.  
  
 Im folgenden Beispiel werden zwei CS0168\-Warnungen generiert:  
  
```  
// CS0168.cs // compile with: /W:3 public class clx { public int i; } public class clz { public static void Main() { int j = 0;   // CS0168, uncomment the following line // j++; clx a;       // CS0168, try the following line instead // clx a = new clx(); } }  
```