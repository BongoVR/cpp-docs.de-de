---
title: "Compilerfehler CS1601"
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
  - "CS1601"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1601"
ms.assetid: 5efa1d2d-c70c-446d-a51f-d23d8a3be22e
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1601
Der Methoden\- oder Delegatparameter darf nicht den Typ 'Typ' haben.  
  
 Einige Typen in der .NET Framework\-Klassenbibliothek, z. B. <xref:System.TypedReference>, <xref:System.RuntimeArgumentHandle> and <xref:System.ArgIterator> können nicht als [ref](../Topic/ref%20\(C%23%20Reference\).md)\- oder [out](../Topic/out%20\(C%23%20Reference\).md)\-Parameter verwendet werden, da mit ihnen potenziell unsichere Operationen ausgeführt werden können.  
  
 Im folgenden Beispiel wird CS1601 generiert:  
  
```  
// CS1601.cs using System; class MyClass { public void Test1 (ref TypedReference t)   // CS1601 { } public void Test2 (out ArgIterator t)   // CS1601 { } }  
```