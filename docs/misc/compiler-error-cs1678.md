---
title: "Compilerfehler CS1678"
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
  - "CS1678"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1678"
ms.assetid: 2be8aa17-81e2-47b0-b239-e41e0c5c0d97
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1678
Parameter 'Nummer' ist als Typ 'Typ1' deklariert, muss jedoch 'Typ2' sein.  
  
 Dieser Fehler tritt auf, wenn der Parametertyp in einer anonymen Methode nicht mit der Deklaration des Delegaten übereinstimmt, in den Sie die Methode umwandeln.  
  
 Im folgenden Beispiel wird CS1678 generiert:  
  
```  
// CS1678 delegate void D(int i); class Errors { static void Main() { D d = delegate(string s) { };   // CS1678 // To resolve, use the following line instead: // D d = delegate(int s) { }; } }  
```