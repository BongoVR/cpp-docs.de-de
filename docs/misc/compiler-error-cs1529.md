---
title: "Compilerfehler CS1529"
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
  - "CS1529"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1529"
ms.assetid: 672a6fd1-3a1f-422c-a29f-46f196d15211
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1529
Eine using\-Klausel muss allen anderen im Namespace definierten Elementen mit Ausnahme externer Aliasdeklarationen vorangehen.  
  
 Eine [using](../Topic/using%20\(C%23%20Reference\).md)\-Klausel muss zuerst in einem Namespace vorkommen.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1529 generiert:  
  
```  
// CS1529.cs namespace X { namespace Subspace { using Microsoft; class SomeClass { }; using Microsoft;      // CS1529, place before class definition } using System.Reflection;  // CS1529, place before namespace 'Subspace' } using System;                 // CS1529, place at the beginning of the file  
```