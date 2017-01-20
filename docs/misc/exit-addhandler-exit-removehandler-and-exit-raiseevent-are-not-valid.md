---
title: "&#39;Exit AddHandler&#39;, &#39;Exit RemoveHandler&#39; und &#39;Exit RaiseEvent&#39; sind nicht g&#252;ltig"
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
  - "vbc31111"
  - "bc31111"
helpviewer_keywords: 
  - "BC31111"
ms.assetid: e02264f3-0645-4de5-b622-8a2a74496b64
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;Exit AddHandler&#39;, &#39;Exit RemoveHandler&#39; und &#39;Exit RaiseEvent&#39; sind nicht g&#252;ltig
'Exit AddHandler', 'Exit RemoveHandler' und 'Exit RaiseEvent' sind nicht gültig. Verwenden Sie 'Return', um Ereignismember zu beenden.  
  
 Die `Exit`\-Anweisung kann nicht verwendet werden, um `AddHandler`, `RemoveHandler` oder `RaiseEvent`\-Methoden in einer `Custom Event`\-Deklaration zu beenden. Verwenden Sie stattdessen die `Return`\-Anweisung, ohne eine Rückgabeausdruck anzugeben, um die Methode zu beenden.  
  
 **Fehler\-ID:** BC31111  
  
### So beheben Sie diesen Fehler  
  
-   Ersetzen Sie die `Exit`\-Anweisung durch eine `Return`\-Anweisung.  
  
     Achten Sie darauf, dass die `Return`\-Anweisung keine Rückgabeausdruck angibt.  
  
## Siehe auch  
 [Event Statement](../Topic/Event%20Statement.md)   
 [AddHandler – löschen](assetId:///fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler – löschen](assetId:///35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [RaiseEvent – löschen](assetId:///7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [Return Statement](../Topic/Return%20Statement%20\(Visual%20Basic\).md)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)