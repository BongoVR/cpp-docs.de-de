---
title: "Die implementierende Klasse &#39;&lt;Klassenname&gt;&#39; f&#252;r die Schnittstelle &#39;&lt;Schnittstellenname&gt;&#39; konnte nicht gefunden werden."
ms.custom: na
ms.date: "12/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc31094"
  - "bc31094"
helpviewer_keywords: 
  - "BC31094"
ms.assetid: 262cb67e-2930-4a4a-a63e-bb2e201b3b93
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Die implementierende Klasse &#39;&lt;Klassenname&gt;&#39; f&#252;r die Schnittstelle &#39;&lt;Schnittstellenname&gt;&#39; konnte nicht gefunden werden.
Eine implementierende Klasse in der Interopassembly ist nicht verfügbar.  
  
 **Fehler\-ID:** BC31094  
  
### So beheben Sie diesen Fehler  
  
1.  Überprüfen Sie, ob die Typbibliothek für das COM\-Objekt gültig ist.  
  
2.  Verwenden Sie das Type Library Importer\-Tool \(„Tlbimp.exe“\), um eine Interopassembly manuell zu erstellen. Fügen Sie dann in Ihrem Projekt einen Verweis auf diese Interopassembly hinzu.  
  
## Siehe auch  
 [Implements Statement](../Topic/Implements%20Statement.md)   
 [COM Interop](../Topic/COM%20Interop%20\(Visual%20Basic\).md)   
 [Tlbimp.exe \(Type Library Importer\)](../Topic/Tlbimp.exe%20\(Type%20Library%20Importer\).md)