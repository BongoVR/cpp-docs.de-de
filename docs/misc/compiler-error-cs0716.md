---
title: "Compilerfehler CS0716"
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
  - "CS0716"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0716"
ms.assetid: 806d25ef-f8a7-4c94-823e-e07904defcf4
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0716
Die Konvertierung in den statischen "Typ"\-Typ ist nicht möglich.  
  
 Dieser Fehler tritt auf, wenn der Code für die Konvertierung in einen statischen Typ eine Umwandlung verwendet. Da ein Objekt keine Instanz eines statischen Typs sein kann, kann die Umwandlung in einen statischen Typ niemals eine sinnvolle Umwandlung sein.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0716 generiert:  
  
```  
// CS0716.cs public static class SC { static void F() { } } public class Test { public static void Main() { object o = new object(); System.Console.WriteLine((SC)o);  // CS0716 } }  
```