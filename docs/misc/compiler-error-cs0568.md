---
title: "Compilerfehler CS0568"
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
  - "CS0568"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0568"
ms.assetid: dc9e1263-f58d-4c95-9165-27ba7757bc7b
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0568
Strukturen können keine expliziten parameterlosen Konstruktoren enthalten.  
  
 Jede [Struktur](../Topic/struct%20\(C%23%20Reference\).md) verfügt bereits über einen Standardkonstruktor, der das Objekt zu null initialisiert. Aus diesem Grund müssen die Konstruktoren, die Sie für eine Struktur erstellen, einen oder mehrere Parameter annehmen können.  
  
 Im folgenden Beispiel wird CS0568 generiert:  
  
```  
// CS0568.cs public struct ClassY { public int field1; public ClassY(){}   // CS0568, cannot have no param constructor // Try following instead: // public ClassY(int i) // { //    field1 = i; // } } public class ClassX { public static void Main() { } }  
```