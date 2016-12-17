---
title: "Typzeichen sind in Imports-Aliasen nicht zul&#228;ssig"
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
  - "vbc31398"
  - "BC31398"
helpviewer_keywords: 
  - "BC31398"
ms.assetid: 0620669d-b529-49f3-9deb-aeda4dacc58a
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Typzeichen sind in Imports-Aliasen nicht zul&#228;ssig
Ein Importalias in einer `Imports`\-Anweisung enthält mindestens ein Typkennzeichen.  
  
 Ein Importalias muss ein gültiger Visual Basic\-Name sein. Die Typkennzeichen \(`%`, `&`, `@`, `!`, `#` und `$`\) sind keine zulässigen Zeichen. Siehe [Declared Element Names](../Topic/Declared%20Element%20Names%20\(Visual%20Basic\).md).  
  
 **Fehler\-ID:** BC31398  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie die Typkennzeichen aus dem Importalias.  
  
## Siehe auch  
 [Type Characters](../Topic/Type%20Characters%20\(Visual%20Basic\).md)   
 [Declared Element Names](../Topic/Declared%20Element%20Names%20\(Visual%20Basic\).md)   
 [Imports Statement \(.NET Namespace and Type\)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md)   
 [NOTINBUILD: Auflösen eines Verweises bei mehreren Variablen mit gleichem Namen](assetId:///9601e39f-1911-44e1-ace5-3f6e090408b9)