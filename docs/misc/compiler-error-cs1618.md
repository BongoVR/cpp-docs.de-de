---
title: "Compilerfehler CS1618"
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
  - "CS1618"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1618"
ms.assetid: e046d402-208e-48fd-8ff3-bb03044036c4
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1618
Es kann kein Delegat mit 'methode' erstellt werden, da sie das Attribut 'Conditional' aufweist  
  
 Sie können keinen Delegaten mit einer bedingten Methode erstellen, da die Methode in einigen Builds möglicherweise nicht vorhanden ist.  
  
 Im folgenden Beispiel wird CS1618 generiert:  
  
```  
// CS1618.cs using System; using System.Diagnostics; delegate void del(); class MakeAnError { public static void Main() { del d = new del(ConditionalMethod);   // CS1618 // Invalid because on builds where DEBUG is not set, // there will be no "ConditionalMethod". } // To fix the error, remove the next line: [Conditional("DEBUG")] public static void ConditionalMethod() { Console.WriteLine("Do something only in debug"); } }  
```