---
title: "Compilerfehler CS0559"
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
  - "CS0559"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0559"
ms.assetid: 37122001-8a55-4cf5-873b-68997e196893
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0559
Der Parametertyp für den Operator \+\+ oder \-\- muss der enthaltende Typ sein.  
  
 Bei der Methodendeklaration für eine Operatorüberladung müssen bestimmte Richtlinien beachtet werden. Für die Operatoren \+\+ und \-\- muss der Parameter vom selben Typ sein wie der Typ, in dem der Operator überladen wird.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0559 generiert:  
  
```  
// CS0559.cs // compile with: /target:library public class iii { public static implicit operator int(iii x) { return 0; } public static implicit operator iii(int x) { return null; } public static int operator ++(int aa)   // CS0559 // try the following line instead // public static iii operator ++(iii aa) { return (iii)0; } }  
```  
  
## Beispiel  
 Im folgenden Beispiel wird CS0559 generiert.  
  
```  
// CS0559_b.cs // compile with: /target:library public struct S { public static S operator ++(S? s) { return new S(); }   // CS0559 public static S operator --(S? s) { return new S(); }   // CS0559 } public struct T { // OK public static T operator --(T t) { return new T(); } public static T operator ++(T t) { return new T(); } public static T? operator --(T? t) { return new T(); } public static T? operator ++(T? t) { return new T(); } }  
```