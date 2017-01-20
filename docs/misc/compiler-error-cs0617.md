---
title: "Compilerfehler CS0617"
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
  - "CS0617"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0617"
ms.assetid: a4363709-9846-4cb8-8772-f5a3ea8555ca
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0617
„reference“ ist kein gültiges benanntes Attributargument, da es sich nicht um einen gültigen Attributparametertyp handelt.  
  
 Es wurde versucht, auf einen [privaten](../Topic/private%20\(C%23%20Reference\).md) Member einer Attributklasse zuzugreifen.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0617 generiert:  
  
```  
// CS0617.cs using System; [AttributeUsage(AttributeTargets.Struct | AttributeTargets.Class | AttributeTargets.Interface)] public class MyClass : Attribute { public int Name; public MyClass (int sName) { Name = sName; Bad = -1; Bad2 = -1; } public readonly int Bad; public int Bad2; } [MyClass(5, Bad=0)] class Class1 {}   // CS0617 [MyClass(5, Bad2=0)] class Class2 {}  
```