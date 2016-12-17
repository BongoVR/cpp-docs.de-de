---
title: "Compilerfehler CS0265"
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
  - "CS0265"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0265"
ms.assetid: d43d19c2-8a66-4bb1-95a0-557b0a29bce1
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0265
Partielle Deklarationen von „type“ weisen inkonsistente Einschränkungen für den Typparameter „type parameter“ auf.  
  
 Dieser Fehler tritt auf, wenn Sie eine generische Klasse als partielle Klasse definieren, sodass die partiellen Definitionen an mehreren Orten auftreten und die Einschränkungen für den generischen Typ inkonsistent oder an mindestens zwei Orten unterschiedlich sind. Wenn Sie die Einschränkungen an mehreren Orten angeben, müssen alle identisch sein. Die einfachste Lösung besteht darin, die Einschränkungen nur an einem Ort anzugeben und an allen anderen Orten wegzulassen. Weitere Informationen finden Sie unter [Partielle Klassen und Methoden](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md) und [Einschränkungen für Typparameter](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
 Der folgende Code generiert den Fehler CS0265.  
  
## Beispiel  
 In diesem Code befinden sich die partiellen Klassendefinitionen alle in einer einzigen Datei, könnten aber auch auf mehrere Dateien verteilt sein.  
  
```  
// CS0265.cs public class GenericsErrors { interface IFace1 { } interface IFace2 { } partial class PartialBadBounds<T> where T : IFace1 { } // CS0265 partial class PartialBadBounds<T> where T : IFace2 { } }  
```