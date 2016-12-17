---
title: "Der Ausdruck ist vom Typ &quot;&lt;Typname&gt;&quot; und kein Auflistungstyp."
ms.custom: na
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc32023"
  - "vbc32023"
helpviewer_keywords: 
  - "BC32023"
ms.assetid: d0f151be-6b65-498b-b571-03faf24df0d8
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Der Ausdruck ist vom Typ &quot;&lt;Typname&gt;&quot; und kein Auflistungstyp.
Die in einer `For Each`\-Anweisung angegebene Gruppenvariable ist kein Auflistungsobjekt oder Array, und mit dem zugehörigen Typ wird die <xref:System.Collections.IEnumerable>\-Schnittstelle nicht implementiert. Der Typ muss entweder das [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] Auflistungsentwurfsmuster unterstützen oder <xref:System.Collections.IEnumerable> implementieren.  
  
 **Fehler\-ID:** BC32023  
  
### So beheben Sie diesen Fehler  
  
-   Deklarieren Sie die Gruppenvariable als Klassentyp, der entweder den [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] Auflistungsentwurf unterstützt oder <xref:System.Collections.IEnumerable> implementiert.  
  
## Siehe auch  
 <xref:System.Collections.IEnumerable>   
 [For Each...Next\-Anweisung](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md)   
 [Visual Basic\-Auflistungsklasse](assetId:///0cb2d1ad-c58d-42c0-8e69-d81f5a15e532)