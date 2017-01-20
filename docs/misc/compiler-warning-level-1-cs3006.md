---
title: "Compilerwarnung (Stufe 1) CS3006"
ms.custom: na
ms.date: "12/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS3006"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS3006"
ms.assetid: efbfd898-e46f-4c3d-91e2-e2da0056b016
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 1) CS3006
Die überladene Methode 'Methode' weicht nur hinsichtlich des Verweises oder der Ausgabe ab, oder des Arrayrangs, und ist nicht CLS\-kompatibel  
  
 Eine Methode kann nicht auf Basis der Parameter [ref](../Topic/ref%20\(C%23%20Reference\).md) oder [out](../Topic/out%20\(C%23%20Reference\).md) überladen werden und weiterhin der Common Language Specification \(CLS\) entsprechen. Weitere Informationen zur CLS\-Kompatibilität finden Sie unter [Schreiben von CLS\-kompatiblem Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3) und [Sprachenunabhängigkeit und sprachunabhängige Komponenten](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md).  
  
## Beispiel  
 Im folgenden Beispiel wird CS3006 generiert: Kommentieren Sie das Attribut auf Assemblyebene aus, oder entfernen Sie eine der Methodendefinitionen, um diese Warnung zu beheben.  
  
```  
// CS3006.cs using System; [assembly: CLSCompliant(true)] public class MyClass { public void f(int i) { } public void f(ref int i)   // CS3006 { } public static void Main() { } }  
```