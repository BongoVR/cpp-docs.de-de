---
title: "Compilerfehler CS2024"
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
  - "CS2023"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS2024"
ms.assetid: 65cf7419-a5a6-4128-88af-176dc8dba14f
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS2024
Ungültige Dateiabschnitt\-Ausrichtungsnummer "\#".  
  
 An die Compileroption [\/filealign](../Topic/-filealign%20\(C%23%20Compiler%20Options\).md) wurde ein ungültiger Wert übergeben.  
  
 Im folgenden Beispiel wird CS2024 generiert:  
  
```  
// CS2024.cs // compile with: /filealign:ex // CS2024 expected class MyClass { public static void Main() { } }  
```