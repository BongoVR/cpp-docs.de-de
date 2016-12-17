---
title: "Compilerfehler CS1578"
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
  - "CS1578"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1578"
ms.assetid: 8356cd33-5acc-4db7-8bbd-2d25f9d7728e
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1578
Dateiname, einzeilige Anmerkung oder Zeilenende erwartet.  
  
 Nach einer [\#line](../Topic/%23line%20\(C%23%20Reference\).md)\-Direktive ist nur ein Dateiname \(in doppelten Anführungszeichen\) oder ein einzeiliger Kommentar zulässig.  
  
 Im folgenden Beispiel wird CS1578 generiert:  
  
```  
// CS1578.cs class MyClass { static void Main() { #line 101 abc.cs   // CS1578 // try the following line instead //#line 101 "abc.cs" intt i;          // error will be reported on line 101 } }  
```