---
title: "Compilerfehler CS1035"
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
  - "CS1035"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1035"
ms.assetid: 99125500-62de-421a-b12b-04311c8947c3
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1035
Dateiende gefunden. "\*\/" erwartet.  
  
 Ein öffnendes Kommentartrennzeichen verfügt über kein schließendes Trennzeichen.  
  
 Im folgenden Beispiel wird CS1035 generiert:  
  
```  
// CS1035.cs public class a { public static void Main() { } } /*   // CS1035, needs closing comment  
```