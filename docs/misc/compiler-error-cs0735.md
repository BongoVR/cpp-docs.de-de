---
title: "Compilerfehler CS0735"
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
  - "cs0735"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0735"
ms.assetid: c49925fb-067c-4f29-9bef-a22115ae1507
caps.latest.revision: 4
caps.handback.revision: "4"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0735
Ein ungültiger Typ wurde als Argument für das TypeForwardedTo\-Attribut angegeben.  
  
 Im folgenden Beispiel wird CS0735 generiert:  
  
```  
// CS735.cs // compile with: /target:library using System.Runtime.CompilerServices; [assembly:TypeForwardedTo(typeof(int[]))]   // CS0735 [assembly:TypeForwardedTo(typeof(string))]   // OK  
```