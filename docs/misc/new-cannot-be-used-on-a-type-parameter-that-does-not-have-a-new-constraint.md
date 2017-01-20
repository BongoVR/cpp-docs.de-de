---
title: "&quot;New&quot; kann nicht f&#252;r einen Typparameter verwendet werden, der keine New-Einschr&#228;nkung aufweist."
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
  - "bc32046"
  - "vbc32046"
helpviewer_keywords: 
  - "BC32046"
ms.assetid: 7ec6b52d-6fd5-47a0-b4a2-163bfd3dae35
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;New&quot; kann nicht f&#252;r einen Typparameter verwendet werden, der keine New-Einschr&#228;nkung aufweist.
Eine Deklarationsanweisung verwendet eine [New Operator](../Topic/New%20Operator%20\(Visual%20Basic\).md)\-Klausel, in der als zu erstellender Typ ein Typparameter angegeben wird, der ohne eine `New`\-Einschränkung deklariert ist.  
  
 Eine *Einschränkung* für einen Typparameter ist eine Anforderung an jedes Typargument, das beim Erstellen des generischen Typs an diesen Typparameter übergeben wird. Die `New`\-Einschränkung gibt an, dass das Typargument einen parameterlosen Konstruktor verfügbar machen muss, auf den der erstellende Code zugreifen kann. Dadurch wird eine `New`\-Klausel in einer Deklarationsanweisung und das Erstellen einer Instanz dieses Typs ermöglicht.  
  
 **Fehler\-ID:** BC32046  
  
### So beheben Sie diesen Fehler  
  
-   Wenn Sie für das Typargument das Verfügbarmachen eines parameterlosen Konstruktors, auf den der Code zugreifen kann, verbindlich festlegen können, fügen Sie der Deklaration des Typparameters die `New`\-Einschränkung hinzu.  
  
-   Wenn Sie für das Typargument das Verfügbarmachen eines parameterlosen Konstruktors, auf den der Code zugreifen kann, nicht verbindlich festlegen können, entfernen Sie die `New`\-Klausel aus der Deklarationsanweisung. Sie können nicht gewährleisten, dass alle an den Typparameter übergebenen Typargumente die Erstellung einer Instanz zugelassen.  
  
## Siehe auch  
 [Generische Typen in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)