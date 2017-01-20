---
title: "Compilerwarnung (Stufe 4) CS0402"
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
  - "CS0402"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0402"
ms.assetid: 5a252c95-18c7-4569-bae0-e1f7b582cf6a
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 4) CS0402
'identifier': Ein Einstiegspunkt kann nicht generisch sein oder sich in einem generischen Typ befinden.  
  
 Der Einstiegspunkt wurde in einem generischen Typ gefunden. Um diese Warnung zu entfernen, implementieren Sie 'Main' in einer nicht generischen Klasse oder Struktur.  
  
```  
// CS0402.cs // compile with: /W:4 class C<T> { public static void Main()  // CS0402 { } } class CMain { public static void Main() {} }  
```