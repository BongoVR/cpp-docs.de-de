---
title: "Compilerfehler CS0722"
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
  - "CS0722"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0722"
ms.assetid: 85f6854c-581d-482b-b4b0-1e665d9e3e6f
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0722
"Typ": Statische Typen können nicht als Rückgabetypen verwendet werden.  
  
 Ein statischer Typ als Rückgabetyp ist nicht sinnvoll, da keine Instanzen von statischen Typen erstellt werden können.  
  
 Im folgenden Beispiel wird CS0722 generiert:  
  
```  
// CS0722.cs public static class SC { } public class CMain { public SC F()  // CS0722 { return null; } public static void Main() { } }  
```