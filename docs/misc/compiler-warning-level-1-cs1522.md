---
title: "Compilerwarnung (Stufe 1) CS1522"
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
  - "CS1522"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1522"
ms.assetid: afb99bbf-a1d9-441e-b392-6845bea23f27
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 1) CS1522
Leerer Schalterblock.  
  
 Der Compiler hat einen [switch](../Topic/switch%20\(C%23%20Reference\).md)\-Block ohne **case**\- oder **default**\-Anweisung erkannt. Ein `switch`\-Block muss mindestens eine **case**\- oder **default**\-Anweisung aufweisen.  
  
 Im folgenden Beispiel wird CS1522 generiert:  
  
```  
// CS1522.cs // compile with: /W:1 using System; class x { public static void Main() { int i = 6; switch(i)   // CS1522 { // add something to the switch block, for example: /* case (5): Console.WriteLine("5"); return; default: Console.WriteLine("not 5"); return; */ } } }  
```