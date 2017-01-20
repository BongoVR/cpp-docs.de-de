---
title: "Die &quot;RaiseEvent&quot;-Methode muss die gleiche Signatur wie der Delegattyp &quot;&lt;Signatur&gt;&quot; des enthaltenden Ereignisses aufweisen."
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
  - "bc31137"
  - "vbc31137"
helpviewer_keywords: 
  - "BC31137"
ms.assetid: 9db77546-9205-4fd2-baf6-6eb1b46b1f1a
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "shoag"
manager: "wpickett"
---
# Die &quot;RaiseEvent&quot;-Methode muss die gleiche Signatur wie der Delegattyp &quot;&lt;Signatur&gt;&quot; des enthaltenden Ereignisses aufweisen.
Eine `Custom Event`\-Deklaration muss eine `RaiseEvent`\-Deklaration aufweisen, die die gleiche Signatur wie der Delegattyp hat, der von der `As`\-Klausel des benutzerdefinierten Ereignisses angegeben wird.  
  
 Damit die Signaturen übereinstimmen, müssen die `RaiseEvent`\-Deklaration und der Delegat die gleiche Anzahl von Parametern aufweisen, und die Parametertypen müssen übereinstimmen.  
  
 **Fehler\-ID:** BC31137  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie die Parameter der `RaiseEvent`\-Deklaration, sodass sie mit den Parametern des Delegattyps übereinstimmen.  
  
## Beispiel  
 Dieses Beispiel zeigt ein benutzerdefiniertes Ereignis mit den korrekten Parametertypen für die `RaiseEvent`\-Deklaration.  
  
 [!CODE [VbVbalrEventError#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEventError#2)]  
  
## Siehe auch  
 [Event Statement](../Topic/Event%20Statement.md)   
 [RaiseEvent \- löschen](assetId:///7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [Delegate Statement](../Topic/Delegate%20Statement.md)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)