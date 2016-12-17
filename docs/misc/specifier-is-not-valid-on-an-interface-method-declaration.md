---
title: "&#39;&lt;spezifizierer&gt;&#39; ist in einer Schnittstellen-Methodendeklaration ung&#252;ltig."
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
  - "bc30270"
  - "vbc30270"
helpviewer_keywords: 
  - "BC30270"
ms.assetid: 598f2944-3e5d-4686-b6f7-2b4bcaf5c211
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;spezifizierer&gt;&#39; ist in einer Schnittstellen-Methodendeklaration ung&#252;ltig.
Eine `Function`\- oder `Sub`\-Anweisung innerhalb einer Schnittstelle enthält ein ungültiges Schlüsselwort, wie etwa `Implements`. Eine Schnittstelle kann Member nur definieren, nicht implementieren.  
  
 **Fehler\-ID:** BC30270  
  
### So beheben Sie diesen Fehler  
  
1.  Entfernen Sie das ungültige Schlüsselwort aus der Deklarationsanweisung.  
  
2.  Lagern Sie die Implementierung der Schnittstellenmember in eine Klasse aus, die die Schnittstelle implementiert.  
  
## Siehe auch  
 [Interface Statement](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Implements Statement](../Topic/Implements%20Statement.md)