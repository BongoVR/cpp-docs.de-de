---
title: "Compilerfehler CS0500"
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
  - "CS0500"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0500"
ms.assetid: b1a45708-702b-482c-bd71-c0c2531e29f3
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0500
'Klassenmember' kann keinen Text deklarieren, da er als abstrakt markiert ist.  
  
 Eine [abstrakte](../Topic/abstract%20\(C%23%20Reference\).md) Methode kann nicht ihre Implementierung enthalten.  
  
 Im folgenden Beispiel wird CS0500 generiert:  
  
```  
// CS0500.cs namespace x { abstract public class clx { abstract public void f(){}   // CS0500 // try the following line instead // abstract public void f(); } public class cly { public static int Main() { return 0; } } }  
```