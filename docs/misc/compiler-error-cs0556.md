---
title: "Compilerfehler CS0556"
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
  - "CS0556"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0556"
ms.assetid: e2430c6e-784f-4ab2-88b9-f660d956e9e8
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0556
Die benutzerdefinierte Konvertierung muss zum oder vom einschließenden Typ konvertieren.  
  
 Eine benutzerdefinierte Konvertierungsroutine muss in die oder aus der Klasse konvertieren, die die Routine enthält.  
  
 Im folgenden Beispiel wird CS0556 generiert:  
  
```  
// CS0556.cs namespace x { public class ii { public class iii { public static implicit operator int(byte aa)   // CS0556 // try the following line instead // public static implicit operator int(iii aa) { return 0; } } public static void Main() { } } }  
```