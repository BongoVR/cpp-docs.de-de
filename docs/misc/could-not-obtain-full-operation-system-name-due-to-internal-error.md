---
title: "Der Name des vollst&#228;ndigen Betriebssystems konnte aufgrund eines internen Fehlers nicht abgerufen werden."
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
  - "vbrDiagnosticInfo_FullOSName"
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Der Name des vollst&#228;ndigen Betriebssystems konnte aufgrund eines internen Fehlers nicht abgerufen werden.
Der Name des vollständigen Betriebssystems konnte aufgrund eines internen Fehlers nicht abgerufen werden. Dies kann dadurch verursacht werden, dass WMI auf dem aktuellen Computer fehlt.  
  
 Beim Aufrufen der `My.Computer.Info.OSFullName`\-Eigenschaft ist ein Fehler aufgetreten. Eine mögliche Ursache für diesen Fehler ist, wenn WMI \(Windows\-Verwaltungsinstrumentation, Windows Management Instrumentation\) auf dem aktuellen Computer nicht installiert ist.  
  
### So beheben Sie diesen Fehler  
  
1.  Fügen Sie rund um den Aufruf der `My.Computer.Info.OSFullName`\-Eigenschaft einen `Try...Catch`\-Block hinzu.  
  
2.  Weitere Informationen zu WMI und der Installation finden Sie unter , indem Sie nach „Windows Management Instrumentation Core“ suchen.  
  
## Siehe auch  
 [My.Computer.Info.OSFullName\-Eigenschaft](assetId:///b3b0fbd1-4dc5-428a-ad04-0d9fc9c2a9be)   
 [Ausnahmen\- und Fehlerbehandlung in Visual Basic](assetId:///3e351e73-cf23-40ab-8b60-05794160529e)   
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)