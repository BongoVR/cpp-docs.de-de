---
title: "Variablen in Modulen k&#246;nnen nicht als &#39;&lt;Spezifizierer&gt;&#39; deklariert werden."
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
  - "bc30593"
  - "vbc30593"
helpviewer_keywords: 
  - "BC30593"
ms.assetid: 2500b776-7fa4-4272-8cc7-204593706651
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Variablen in Modulen k&#246;nnen nicht als &#39;&lt;Spezifizierer&gt;&#39; deklariert werden.
Sie haben einen Spezifizierer, z. B. `MustInherit`, für eine Variable in einer `Module`\-Anweisung verwendet. Module können nie instanziiert werden, unterstützen keine Vererbung und können keine Schnittstellen implementieren.  
  
 **Fehler\-ID:** BC30593  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie den Spezifizierer.  
  
## Siehe auch  
 [Module Statement](../Topic/Module%20Statement.md)