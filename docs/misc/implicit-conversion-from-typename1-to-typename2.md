---
title: "Implizite Konvertierung von &quot;&lt;Typname1&gt;&quot; in &quot;&lt;Typname2&gt;."
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
  - "vbc42016"
  - "BC42016"
helpviewer_keywords: 
  - "BC42016"
ms.assetid: 7dabaab0-8258-4c17-927f-28e61f50bd3a
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "shoag"
manager: "wpickett"
---
# Implizite Konvertierung von &quot;&lt;Typname1&gt;&quot; in &quot;&lt;Typname2&gt;.
Ein Ausdruck oder eine Zuweisungsanweisung konvertiert den Wert eines Datentyps in einen anderen Typ. Da kein Konvertierungsschlüsselwort verwendet wird, ist die Konvertierung *implizit*.  
  
 Standardmäßig ist diese Meldung eine Warnung. Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC42016  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie nach Möglichkeit Werte desselben Datentyps, damit [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] keine Konvertierung vornehmen muss.  
  
-   Verwenden Sie `CType` oder ein anderes Konvertierungsschlüsselwort, damit die Konvertierung *explizit* ist.  
  
## Siehe auch  
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../Topic/Type%20Conversion%20Functions%20\(Visual%20Basic\).md)