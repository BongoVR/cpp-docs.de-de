---
title: "Funktion ohne As-Klausel. R&#252;ckgabetyp &#39;Object&#39; wird angenommen."
ms.custom: na
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "BC42021"
  - "vbc42021"
helpviewer_keywords: 
  - "BC42021"
ms.assetid: c1efadf1-fba3-437b-a311-240c4d07d894
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "shoag"
manager: "wpickett"
---
# Funktion ohne As-Klausel. R&#252;ckgabetyp &#39;Object&#39; wird angenommen.
Eine `Function`\-Prozedur gibt keine `As`\-Klausel an.  
  
 Eine `As`\-Klausel bezeichnet einen Datentyp, der einem Programmierelement zugeordnet werden soll. In einer [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md) gibt sie den Datentyp des Werts an, den die `Function`\-Prozedur an den aufrufenden Code zurückgibt. Wenn Sie keine `As`\-Klausel in die `Function`\-Anweisung einfügen, lautet der Rückgabedatentyp standardmäßig `Object`.  
  
 Standardmäßig ist diese Meldung eine Warnung. Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC42021  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie eine `As`\-Klausel in die `Function`\-Anweisung ein, um den Rückgabedatentyp anzugeben.  
  
## Siehe auch  
 [Function\-Prozeduren](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)