---
title: "Compilerfehler CS1007"
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
  - "CS1007"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1007"
ms.assetid: b56ee2c6-8e79-4b9b-8c59-194bdb22bc3e
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1007
Der Eigenschaftenaccessor ist bereits definiert.  
  
 Wenn Sie eine [Eigenschaft](../Topic/Using%20Properties%20\(C%23%20Programming%20Guide\).md) deklarieren, müssen Sie auch ihre Accessormethoden deklarieren. Eine Eigenschaft kann jedoch nicht mehr als eine `get`\-Accessormethode oder nicht mehr als eine `set`\-Accessormethode aufweisen.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1007 generiert:  
  
```  
// CS1007.cs public class clx { public int MyProperty { get { return 0; } get   // CS1007, this is the second get method { return 0; } } public static void Main() {} }  
```