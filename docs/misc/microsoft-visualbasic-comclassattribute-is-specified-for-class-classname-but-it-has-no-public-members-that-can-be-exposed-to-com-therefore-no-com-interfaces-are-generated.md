---
title: "Microsoft.VisualBasic.ComClassAttribute ist f&#252;r die Klasse &quot;&lt;Klassenname&gt;1&quot; festgelegt, hat jedoch keine &#246;ffentlichen Member, die f&#252;r COM verf&#252;gbar gemacht werden k&#246;nnen. Es wurden daher keine COM-Schnittstellen generiert"
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
  - "bc40011"
  - "vbc40011"
helpviewer_keywords: 
  - "BC40011"
ms.assetid: 39aed273-bf27-4667-8116-022c4dd8f3c5
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Microsoft.VisualBasic.ComClassAttribute ist f&#252;r die Klasse &quot;&lt;Klassenname&gt;1&quot; festgelegt, hat jedoch keine &#246;ffentlichen Member, die f&#252;r COM verf&#252;gbar gemacht werden k&#246;nnen. Es wurden daher keine COM-Schnittstellen generiert
Eine Klasse mit einem `COMClassAttribute`\-Attributblock definiert keine `Public`\-Eigenschaften oder \-Methoden. Wenn eine Klasse als COM\-Objekt verfügbar gemacht werden soll, müssen die Eigenschaften und Methoden mit `Public`\-Zugriff deklariert werden.  
  
 Standardmäßig ist diese Meldung eine Warnung. Weitere Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC40011  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie das `Public`\-Schlüsselwort mindestens einer Eigenschaft oder Methode in der Klasse hinzu, oder entfernen Sie den `COMClassAttribute`\-Attributblock.  
  
## Siehe auch  
 [NICHT IM BUILD: In Visual Basic verwendete Attribute](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NICHT IM BUILD: Anwendung von Attributen](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [Public](../Topic/Public%20\(Visual%20Basic\).md)   
 [ComClassAttribute\-Klasse](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)