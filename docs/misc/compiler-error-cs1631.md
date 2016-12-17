---
title: "Compilerfehler CS1631"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1631"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1631"
ms.assetid: bf0c5ff9-90a3-4db6-b4ee-0b93e31614e0
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1631
Mit "yield" kann im Text einer catch\-Klausel kein Wert zurückgegeben werden.  
  
 Die yield\-Anweisung ist im Text einer catch\-Klausel nicht zulässig. Verschieben Sie die yield\-Anweisung außerhalb der catch\-Klausel, um diesen Fehler zu vermeiden.  
  
 Im folgenden Beispiel wird CS1631 generiert:  
  
```  
// CS1631.cs using System; using System.Collections; public class C : IEnumerable { public IEnumerator GetEnumerator() { try { } catch(Exception e) { yield return this;  // CS1631 } } public static void Main() { } }  
```