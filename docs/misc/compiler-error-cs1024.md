---
title: "Compilerfehler CS1024"
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
  - "CS1024"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1024"
ms.assetid: 41f587cb-1958-4eb6-9f8d-c03500e55e21
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1024
Präprozessordirektive erwartet.  
  
 Eine Zeile beginnt mit dem Nummernzeichen \(\#\), aber die nachfolgende Zeichenfolge war keine gültige [Präprozessordirektive](../Topic/C%23%20Preprocessor%20Directives.md).  
  
 Im folgenden Beispiel wird CS1024 generiert:  
  
```  
// CS1024.cs #import System   // CS1024  
```