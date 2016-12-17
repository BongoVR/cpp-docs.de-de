---
title: "Die &lt;Klassenname&gt;-Klasse muss als MustInherit deklariert werden oder folgende geerbte MustOverride-Member &#252;berschreiben: &lt;Membername(n)&gt;."
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
  - "bc30610"
  - "vbc30610"
helpviewer_keywords: 
  - "BC30610"
ms.assetid: 7fba7a3b-c918-44ba-ae85-20312615c1ce
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Die &lt;Klassenname&gt;-Klasse muss als MustInherit deklariert werden oder folgende geerbte MustOverride-Member &#252;berschreiben: &lt;Membername(n)&gt;.
Von Basisklassen abgeleitete Klassen, die `MustOverride`\-Member enthalten, müssen diese Member überschreiben oder den `MustInherit`\-Modifizierer verwenden.  
  
 **Fehler\-ID:** BC30610  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie der Klassendefinition den `MustInherit`\-Modifizierer hinzu.  
  
-   Deklarieren Sie mit dem `Overrides`\-Schlüsselwort eine Überschreibung.  
  
## Siehe auch  
 [Overrides](../Topic/Overrides%20\(Visual%20Basic\).md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [NICHT IM BUILD: Vererbung in Visual Basic](assetId:///e5e6e240-ed31-4657-820c-079b7c79313c)