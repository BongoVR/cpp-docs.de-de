---
title: "Compilerfehler CS0526"
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
  - "CS0526"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0526"
ms.assetid: befc46b4-28ea-40d3-89ac-132b92455772
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0526
Schnittstellen können keine Konstruktoren enthalten.  
  
 Für diese [Schnittstellen](../Topic/interface%20\(C%23%20Reference\).md) können keine Konstruktoren definiert werden. Eine Methode wird als Konstruktor betrachtet, wenn sie denselben Namen wie die Klasse hat und keinen Rückgabewert aufweist.  
  
 Im folgenden Beispiel wird CS0526 generiert:  
  
```  
// CS0526.cs namespace x { public interface clx { public clx()   // CS0526 { } } public class cly { public static void Main() { } } }  
```