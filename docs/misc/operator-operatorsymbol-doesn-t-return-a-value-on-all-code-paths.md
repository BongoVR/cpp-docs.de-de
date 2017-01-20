---
title: "Der Operator &quot;&lt;Operatorsymbol&gt;&quot; gibt nicht f&#252;r alle Codepfade einen Wert zur&#252;ck"
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
  - "vbc42106"
  - "bc42106"
helpviewer_keywords: 
  - "BC42106"
ms.assetid: 175b2bc9-5233-462d-97de-9d97b003cc46
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "shoag"
manager: "wpickett"
---
# Der Operator &quot;&lt;Operatorsymbol&gt;&quot; gibt nicht f&#252;r alle Codepfade einen Wert zur&#252;ck
Der Operator "\<Operatorsymbol\>" gibt nicht für alle Codepfade einen Wert zurück. Wenn das Ergebnis verwendet wird, kann während der Laufzeit eine NULL\-Verweisausnahme auftreten.  
  
 Eine Operatorprozedur hat mindestens einen möglichen Pfad durch ihren Code, bei dem kein Wert zurückgegeben wird.  
  
 Sie können einen Wert aus einer Operatorprozedur nur zurückgeben, indem Sie diese in eine [Return Statement](../Topic/Return%20Statement%20\(Visual%20Basic\).md) einbeziehen.  
  
 Wenn die Steuerung an die `End Operator`\-Anweisung übergeben wird, gibt die Operatorprozedur den Standardwert für den Datentyp der Eigenschaft zurück. Weitere Informationen finden Sie unter „Verhalten“ in [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md).  
  
 Standardmäßig ist diese Meldung eine Warnung. Weitere Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC42106  
  
### So beheben Sie diesen Fehler  
  
-   Überprüfen Sie Ihre Ablaufsteuerungslogik, und stellen Sie sicher, dass jeder mögliche Pfad endet mit einer `Return`\-Anweisung endet. Insbesondere die letzte Anweisung vor `End Operator` sollte eine `Return`\-Anweisung sein.  
  
## Siehe auch  
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)