---
title: "Die Parameter &quot;InterfaceId&quot; und &quot;EventsId&quot; f&#252;r Microsoft.VisualBasic.ComClassAttribute auf &quot;&lt;Typname&gt;&quot; k&#246;nnen nicht denselben Wert haben"
ms.custom: na
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc32507"
  - "vbc32507"
helpviewer_keywords: 
  - "BC32507"
ms.assetid: 762e2990-e578-492d-b8ee-11658b6069fc
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "shoag"
manager: "wpickett"
---
# Die Parameter &quot;InterfaceId&quot; und &quot;EventsId&quot; f&#252;r Microsoft.VisualBasic.ComClassAttribute auf &quot;&lt;Typname&gt;&quot; k&#246;nnen nicht denselben Wert haben
Ein `COMClassAttribute`\-Attributblock gibt denselben global eindeutigen Bezeichner \(GUID\) für die Schnittstelle wie für das Erstellungsereignis an. Wenn diese Bezeichner beide angegeben werden, muss sie verschieden sein. Sie müssen sich auch vom Klassenbezeichner unterscheiden.  
  
 Eine GUID besteht aus 16 Bytes, von denen die ersten acht numerisch und die letzten acht binär sind. Sie wird von Microsoft\-Hilfsprogrammen wie "uuidgen.exe" generiert und ist garantiert eindeutig.  
  
 **Fehler\-ID:** BC32507  
  
### So beheben Sie diesen Fehler  
  
1.  Bestimmen Sie die korrekten GUIDs, die erforderlich sind, um die Schnittstelle und das Erstellungsereignis für das COM\-Objekt zu identifizieren.  
  
2.  Stellen Sie sicher, dass die GUID\-Zeichenfolgen, die dem `COMClassAttribute`\-Attributblock angezeigt werden, ordnungsgemäß kopiert werden.  
  
## Siehe auch  
 [NICHT IM BUILD: In Visual Basic verwendete Attribute](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NICHT IM BUILD: Anwendung von Attributen](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute\-Klasse](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)