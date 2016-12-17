---
title: "Compilerfehler CS0522"
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
  - "CS0522"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0522"
ms.assetid: f749f21e-92ee-495c-9b53-179ce9342d05
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0522
'Konstruktor': Strukturen können keine Basisklassenkonstruktoren aufrufen.  
  
 Eine [Struktur](../Topic/struct%20\(C%23%20Reference\).md) kann keinen Basisklassenkonstruktor aufrufen. Entfernen Sie den Aufruf des Basisklassenkonstruktors.  
  
 Im folgenden Beispiel wird CS0522 generiert:  
  
```  
// CS0522.cs public class clx { public clx(int i) { } public static void Main() { } } public struct cly { public cly(int i):base(0)   // CS0522 // try the following line instead // public cly(int i) { } }  
```