---
title: "Der Typ &lt;Typname&gt; kann die Schnittstelle &lt;Schnittstellenname&gt; nicht implementieren, weil eine &lt;Ereignissignatur&gt; deklariert wird, die &#252;ber einen R&#252;ckgabetyp verf&#252;gt."
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
  - "bc30945"
  - "vbc30945"
helpviewer_keywords: 
  - "BC30945"
ms.assetid: 4f26e71a-949d-4103-b565-35cc8e833d29
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "shoag"
manager: "wpickett"
---
# Der Typ &lt;Typname&gt; kann die Schnittstelle &lt;Schnittstellenname&gt; nicht implementieren, weil eine &lt;Ereignissignatur&gt; deklariert wird, die &#252;ber einen R&#252;ckgabetyp verf&#252;gt.
Eine Klasse oder Struktur versucht, eine Schnittstelle zu implementieren, die ein Ereignis deklariert, das einen Wert zurückgibt.  
  
 Visual Basic unterstützt das Deklarieren von Ereignissen, die Werte zurückgeben, derzeit nicht.  
  
 **Fehler\-ID:** BC30945  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie die `Implements`\-Anweisung aus der Klassen\- oder Strukturdefinition, oder implementieren Sie eine andere Schnittstelle.  
  
## Siehe auch  
 [NICHT IM BUILD: Ereignisse und Ereignishandler](assetId:///95074a0d-1cbc-4221-a95a-964185c7f962)   
 [Implements Statement](../Topic/Implements%20Statement.md)   
 [NICHT IM BUILD: Implements\-Schlüsselwort und Implements\-Anweisung](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)