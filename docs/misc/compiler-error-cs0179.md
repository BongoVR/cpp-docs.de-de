---
title: "Compilerfehler CS0179"
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
  - "CS0179"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0179"
ms.assetid: bef000ca-64d7-4809-b2a0-de6927b04b0d
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0179
'Member' kann nicht extern sein und Text deklarieren.  
  
 Wenn ein Klassenmember als [extern](../Topic/extern%20\(C%23%20Reference\).md) gekennzeichnet ist, weist dies darauf hin, dass sich die Definition des Members in einer anderen Datei befindet. Daher kann ein als **extern** gekennzeichneter Klassenmember nicht in der Klasse definiert werden. Entfernen Sie entweder das `extern`\-Schlüsselwort, oder löschen Sie die Definition. Weitere Informationen finden Sie unter [Methoden](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0179 generiert:  
  
```  
// CS0179.cs public class MyClass { public extern int ExternMethod(int aa)   // CS0179 { return 0; } // try the following line instead // public extern int ExternMethod(int aa); public static void Main() { } }  
```