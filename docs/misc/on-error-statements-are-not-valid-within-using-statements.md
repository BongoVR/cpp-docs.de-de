---
title: "&#39;On Error&#39;-Anweisungen sind innerhalb von &#39;Using&#39;-Anweisungen nicht g&#252;ltig."
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
  - "vbc36013"
  - "bc36013"
helpviewer_keywords: 
  - "BC36013"
ms.assetid: 5b399bf9-6595-46e0-a808-378f6c28568b
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;On Error&#39;-Anweisungen sind innerhalb von &#39;Using&#39;-Anweisungen nicht g&#252;ltig.
Eine `On Error`\-Anweisung tritt innerhalb einer `Using`\-Anweisung auf, sie ist aber in diesem Kontext nicht gültig.  
  
 **Fehler\-ID:** BC36013  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie strukturierte Fehlerbehandlung, wie etwa einen `Try…Catch`\-Block, anstelle der `On Error`\-Anweisung.  
  
## Siehe auch  
 [Übersicht über die strukturierte Ausnahmebehandlung für Visual Basic](assetId:///bb81af80-a735-4873-9711-6151a48e418a)   
 [Verwenden der strukturierten und der unstrukturierten Ausnahmebehandlung \(Visual Basic\)](assetId:///e897d7ca-07e8-45dd-8a6d-a5b2a2fc9b9a)   
 [On Error Statement](../Topic/On%20Error%20Statement%20\(Visual%20Basic\).md)   
 [Gewusst wie: Testen von Code mit einem Try...Catch\-Block in Visual Basic](assetId:///8368e205-ed73-4185-a247-af84fb4fafa9)   
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)