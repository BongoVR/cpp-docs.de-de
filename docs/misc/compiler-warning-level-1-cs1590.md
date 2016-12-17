---
title: "Compilerwarnung (Stufe 1) CS1590"
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
  - "CS1590"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1590"
ms.assetid: 0d6e5594-d6a6-43bf-8aa8-a452fa5748df
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 1) CS1590
Ungültiges XML\-Include\-Element \-\- Dateiattribut fehlt  
  
 Ein path\- oder doc\-Attribut, das an das [\<include\>](../Topic/%3Cinclude%3E%20\(C%23%20Programming%20Guide\).md)\-Tag übergeben wird, fehlt oder ist unvollständig.  
  
 Im folgenden Beispiel wird CS1590 generiert:  
  
```  
// CS1590.cs // compile with: /W:1 /doc:x.xml /// <include path='MyDocs/MyMembers[@name="test"]/*' />   // CS1590 // try the following line instead // /// <include file='x.doc' path='MyDocs/MyMembers[@name="test"]/*' /> class Test { public static void Main() { } }  
```