---
title: "Compilerfehler CS1724"
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
  - "CS1724"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1724"
ms.assetid: f25ec28e-c20b-457d-afc2-284494e69dad
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1724
Der für das Argument für System.Runtime.InteropServices.DefaultCharSetAttribute angegebene Wert ist nicht gültig.  
  
 Dieser Fehler wird von einem ungültigen Argument für die <xref:System.Runtime.InteropServices.DefaultCharSetAttribute>\-Klasse generiert.  
  
## Beispiel  
 Im folgenden Beispiel wird der Fehler CS1724 generiert:  
  
```  
// CS1724.cs using System.Runtime.InteropServices; // To resolve, replace 42 with a valid CharSet value. [module:DefaultCharSetAttribute((CharSet)42)]   // CS1724 class C { [DllImport("F.Dll")] extern static void FW1Named(); static void Main() {} }  
```