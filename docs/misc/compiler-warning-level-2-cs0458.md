---
title: "Compilerwarnung (Stufe 2) CS0458"
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
  - "CS0458"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0458"
ms.assetid: 0986c620-b4bc-4e4b-976f-88359cfa3a45
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 2) CS0458
Das Ergebnis des Ausdrucks ist immer "null" vom Typ "Typname".  
  
 Diese Warnung wird durch einen `nullable`\-Ausdruck verursacht, dessen Ergebnis immer `null` ist.  
  
 Durch den folgenden Code wird die Warnung CS0458 generiert.  
  
## Beispiel  
 In diesem Beispiel werden unterschiedliche Vorgänge mit `nullable`\-Typen veranschaulicht, die diesen Fehler verursachen.  
  
```  
// CS0458.cs using System; public  class Test { public static void Main() { int a = 5; int? b = a + null;    // CS0458 int? qa = 15; b = qa + null;        // CS0458 b -= null;            // CS0458 int? qa2 = null; b = qa2 + null;       // CS0458 qa2 -= null;          // CS0458 } }  
```