---
title: "Compilerfehler CS1027"
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
  - "CS1027"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1027"
ms.assetid: a6657f0f-5664-47a5-95cf-803f5a0e0c90
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1027
\#endif\-Direktive erwartet.  
  
 Für eine angegebene `#if`\-Direktive wurde keine entsprechende `#endif` [Präprozessordirektive](../Topic/C%23%20Preprocessor%20Directives.md) gefunden. Oder der Compiler hat möglicherweise eine `#endregion`\-Direktive gefunden, obwohl keine entsprechende `#region`\-Direktive innerhalb eines `#if`\-Blocks vorhanden ist.  
  
 Im folgenden Beispiel wird CS1027 generiert:  
  
```  
// CS1027.cs #if true   // CS1027, uncomment next line to resolve // #endif namespace x { public class clx { public static void Main() { } } }  
```