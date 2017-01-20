---
title: "NotInheritable-Klassen k&#246;nnen keine als &quot;&lt;Spezifizierername&gt;&quot; deklarierten Member enthalten"
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
  - "vbc30607"
  - "bc30607"
helpviewer_keywords: 
  - "BC30607"
ms.assetid: c800e24e-d055-402f-b378-6d2f4041ff16
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# NotInheritable-Klassen k&#246;nnen keine als &quot;&lt;Spezifizierername&gt;&quot; deklarierten Member enthalten
Überschreibungsmodifizierer können nicht mit `NotInheritable`\-Klassen verwendet werden, weil deren Member nicht überschrieben werden können.  
  
 **Fehler\-ID:** BC30607  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie Überschreibungsmodifizierer wie `Overridable`, `NotOverridable` oder `MustOverride` aus der Klassendefinition.  
  
## Siehe auch  
 [Overridable](../Topic/Overridable%20\(Visual%20Basic\).md)   
 [NotOverridable](../Topic/NotOverridable%20\(Visual%20Basic\).md)   
 [MustOverride](../Topic/MustOverride%20\(Visual%20Basic\).md)   
 [NICHT IM BUILD: Überschreiben von Eigenschaften und Methoden](assetId:///2167e8f5-1225-4b13-9ebd-02591ba90213)