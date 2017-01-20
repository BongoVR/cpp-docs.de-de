---
title: "R&#252;ckgabe- und Parametertypen von &#39;&lt;Operator&gt;&#39; m&#252;ssen &#39;&lt;Typname&gt;&#39; sein, damit sie in einer For-Anweisung verwendet werden k&#246;nnen."
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc33039"
  - "bc33039"
helpviewer_keywords: 
  - "BC33039"
ms.assetid: 30e8cfa8-c086-474c-a4f0-ad01d01096e2
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# R&#252;ckgabe- und Parametertypen von &#39;&lt;Operator&gt;&#39; m&#252;ssen &#39;&lt;Typname&gt;&#39; sein, damit sie in einer For-Anweisung verwendet werden k&#246;nnen.
Eine `For`\-Schleife gibt eine Indikatorvariable eines Typs an, der den `+`\- oder `-`\-Operator nicht mit Parametern und einem Rückgabewert des eigenen Typs definiert.  
  
 Die Indikatorvariable muss einen Typ aufweisen, der Operatoren für die Addition \(`+`\) und Subtraktion \(`-`\) unterstützt, die vollständig mit ihrem enthaltenden Typ ausgeführt werden. Dies bedeutet, dass beide Operanden und der Rückgabewert den Typ der Indikatorvariablen aufweisen müssen.  
  
 Wenn Sie für die Indikatorvariable einen numerischen Datentyp verwenden, werden die Operatoren `+` und `-` für den enthaltenen Typ unterstützt. Wenn Sie eine benutzerdefinierte Klasse oder Struktur verwenden, müssen Sie beide Operatoren mit Operanden und einem Rückgabewert vom Typ der Klasse oder Struktur definieren.  
  
 **Fehler\-ID:** BC33039  
  
### So beheben Sie diesen Fehler  
  
1.  Stellen Sie sicher, dass der Datentyp der Indikatorvariablen richtig geschrieben ist.  
  
2.  Wenn Sie für die Indikatorvariable eine benutzerdefinierte Klasse oder Struktur verwenden, definieren Sie die Operatoren `+` und `-`, die vollständig für diese Klasse oder Struktur ausgeführt werden.  
  
## Siehe auch  
 [For...Next\-Anweisung](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)   
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)