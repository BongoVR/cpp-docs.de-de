---
title: "Compilerfehler CS1553"
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
  - "CS1553"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1553"
ms.assetid: aec64251-b4ac-45c0-b143-7ebda138af6e
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1553
Ungültige Deklaration. Verwenden Sie stattdessen 'modifizierer operator \<zieltyp\> \(...'  
  
 Der Rückgabetyp für einen [Operator](../Topic/operator%20\(C%23%20Reference\)2.md) muss der Parameterliste unmittelbar voranstehen, und *modifizierer* ist entweder `implicit` oder **explizit**.  
  
 Im folgenden Beispiel wird CS1553 generiert:  
  
```  
// CS1553.cs class MyClass { public static int implicit operator (MyClass f)   // CS1553 // try the following line instead // public static implicit operator int (MyClass f) { return 6; } public static void Main() { } }  
```