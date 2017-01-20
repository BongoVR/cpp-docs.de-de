---
title: "Das Typargument &#39;&lt;typargumentname&gt;&#39; ist als &#39;MustInherit&#39; deklariert und entspricht nicht der Einschr&#228;nkung &#39;New&#39; f&#252;r den Typparameter &#39;&lt;typparametername&gt;&#39;."
ms.custom: na
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc32082"
  - "BC32082"
helpviewer_keywords: 
  - "BC32082"
ms.assetid: 597e5944-a61b-4858-ada5-efb80b27f26b
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Das Typargument &#39;&lt;typargumentname&gt;&#39; ist als &#39;MustInherit&#39; deklariert und entspricht nicht der Einschr&#228;nkung &#39;New&#39; f&#252;r den Typparameter &#39;&lt;typparametername&gt;&#39;.
Ein generischer Typ wird mit einer `MustInherit`\-Klasse als Typargument aufgerufen, während der entsprechende Typparameter mit der `New`\-Einschränkung deklariert ist.  
  
 Für die `New`\-Einschränkung muss der im entsprechenden Typargument übergebene Typ die Erstellung von Objekten unterstützen. Eine *abstrakte* Klasse, also eine Klasse, die als `MustInherit` deklariert ist, macht jedoch keine Konstruktoren verfügbar, da keine Objekte aus ihr erstellt werden können.  
  
 **Fehler\-ID:** BC32082  
  
### So beheben Sie diesen Fehler  
  
1.  Wenn die im Typargument verwendete Klasse nicht abstrakt sein muss, entfernen Sie das Schlüsselwort `MustInherit` aus ihrer Deklaration.  
  
2.  Wenn die im Typargument verwendete Klasse abstrakt sein muss, aber nicht für die Konstruktion des generischen Typs verwendet werden muss, übergeben Sie im Typargument eine andere Klasse.  
  
3.  Wenn der entsprechende Typparameter keine Objekte des ihm übergebenen Typs erstellen muss, entfernen Sie die Einschränkung `New` aus seiner Deklaration.  
  
## Siehe auch  
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [New Operator](../Topic/New%20Operator%20\(Visual%20Basic\).md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)