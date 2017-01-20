---
title: "Compilerwarnung (Stufe 1) CS1574"
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
  - "CS1574"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1574"
ms.assetid: 4cd2b474-ab01-4397-aed7-63e5f0081649
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 1) CS1574
XML\-Kommentar zu „construct“ weist ein syntaktisch falsches cref\-Attribut „name“ auf.  
  
 Eine an ein cref\-Tag übergebene Zeichenfolge, z. B. in einem \<Ausnahme\>\-Tag, verwies auf einen Member, der in der aktuellen Buildumgebung nicht verfügbar ist. Die Zeichenfolge, die Sie an ein cref\-Tag übergeben, muss der syntaktisch korrekte Name eines Members oder Felds sein.  
  
 Weitere Informationen finden Sie unter [Empfohlene Tags für Dokumentationskommentare](../Topic/Recommended%20Tags%20for%20Documentation%20Comments%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS1574 generiert:  
  
```  
// CS1574.cs // compile with: /W:1 /doc:x.xml using System; /// <exception cref="System.Console.WriteLin">An exception class.</exception>   // CS1574 // instead, uncomment and try the following line // /// <exception cref="System.Console.WriteLine">An exception class.</exception> class EClass : Exception { } class TestClass { public static void Main() { try { } catch(EClass) { } } }  
```