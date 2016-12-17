---
title: "Compilerfehler CS1706"
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
  - "CS1706"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1706"
ms.assetid: 8c589a49-3959-422e-ac18-65a2eaae3da0
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1706
Der Ausdruck kann keine anonymen Methoden oder Lambdaausdrücke enthalten.  
  
 Sie können keine anonyme Methode in einen Ausdruck einfügen.  
  
### So beheben Sie diesen Fehler  
  
1.  Verwenden Sie einen regulären `delegate` im Ausdruck.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1706 generiert.  
  
```  
// CS1706.cs using System; delegate void MyDelegate(); class MyAttribute : Attribute { public MyAttribute(MyDelegate d) { } } // Anonymous Method in Attribute declaration is not allowed. [MyAttribute(delegate{/* anonymous Method in Attribute declaration */})]  // CS1706 class Program { }  
```