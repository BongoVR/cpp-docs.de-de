---
title: "Compilerfehler CS0407"
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
  - "CS0407"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0407"
ms.assetid: 59112fb9-4641-466e-b738-b3228539a09e
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0407
'return\-type method' hat den falschen Rückgabetyp.  
  
 Die Methode war nicht mit dem Delegattyp kompatibel. Die Argumenttypen stimmten überein, der Rückgabetyp war jedoch nicht der richtige Rückgabetyp für den betreffenden Delegaten. Um diesen Fehler zu vermeiden, verwenden Sie eine andere Methode, ändern Sie den Rückgabetyp der Methode, oder ändern Sie den Rückgabetyp des Delegaten.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0407 generiert:  
  
```  
// CS0407.cs public delegate int MyDelegate(); class C { MyDelegate d; public C() { d = new MyDelegate(F);  // OK: F returns int d = new MyDelegate(G);  // CS0407 – G doesn't return int } public int F() { return 1; } public void G() { } public static void Main() { C c1 = new C(); } }  
```