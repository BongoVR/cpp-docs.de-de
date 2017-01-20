---
title: "Compilerfehler CS0283"
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
  - "CS0283"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0283"
ms.assetid: f94a5b84-92c5-4602-894d-6f856d57e0e6
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0283
Der Typ 'type' kann nicht als konstant deklariert werden.  
  
 Der in einer Konstantendeklaration angegebene Typ muss `byte`, `char`, `short`, `int`, `long`, `float`, `double`, `decimal`, `bool`, `string`, ein Enumerationstyp oder ein Verweistyp sein, dem der Wert NULL zugewiesen wird. Jeder konstante Ausdruck muss einen Wert des Zieltyps oder eines Typs liefern, der durch implizite Konvertierung in den Zieltyp konvertiert werden kann.  
  
## Beispiel  
 Im folgenden Beispiel wird der Fehler CS0283 generiert.  
  
```  
// CS0283.cs struct MyTest { } class MyClass { // To resolve the error but retain the "const-ness", // change const to readonly. const MyTest test = new MyTest();   // CS0283 public static int Main() { return 1; } }  
```