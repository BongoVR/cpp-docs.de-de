---
title: "Typargumente k&#246;nnen nicht auf den Ausdruck &quot;&lt;Ausdruck&gt;&quot; angewendet werden"
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
  - "bc32058"
  - "vbc32058"
helpviewer_keywords: 
  - "BC32058"
ms.assetid: c6b9b49c-6fb2-47b8-a8bb-464562d3adfd
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Typargumente k&#246;nnen nicht auf den Ausdruck &quot;&lt;Ausdruck&gt;&quot; angewendet werden
Ein Importalias wurde mit einer [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md)\-Klausel definiert, die Typargumente an den Importalias übergibt.  
  
 Typargumente werden für generische Typen verwendet, und nur Klassen, Strukturen, Schnittstellen, Prozeduren und Delegaten können generisch sein. Weder Namespaces noch Importaliase können generisch sein.  
  
 **Fehler\-ID:** BC32058  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie die `Of`\-Klausel und ihre Typargumente aus dem Importalias.  
  
## Siehe auch  
 [Imports Statement \(.NET Namespace and Type\)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md)   
 [References and the Imports Statement](../Topic/References%20and%20the%20Imports%20Statement%20\(Visual%20Basic\).md)   
 [NOTINBUILD: Auflösen eines Verweises bei mehreren Variablen mit gleichem Namen](assetId:///9601e39f-1911-44e1-ace5-3f6e090408b9)   
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)