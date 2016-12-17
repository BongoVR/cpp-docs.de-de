---
title: "Der Throw-Operand muss von System.Exception abgeleitet werden."
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
  - "vbc30665"
  - "bc30665"
helpviewer_keywords: 
  - "BC30665"
ms.assetid: 7c228087-39ea-4b30-a410-6ba711e67e5e
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Der Throw-Operand muss von System.Exception abgeleitet werden.
Das für `Throw` angegebene Argument muss entweder eine Instanz von `System.Exception` oder eine Instanz einer von `System.Exception` abgeleiteten Klasse sein.  
  
 **Fehler\-ID:** BC30665  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie ein Argument, das von `System.Exception` abgeleitet wird, wie im folgenden Beispiel gezeigt.  
  
    ```  
    Throw New System.Exception("This is an error.")  
    ```  
  
## Siehe auch  
 [Throw Statement](../Topic/Throw%20Statement%20\(Visual%20Basic\).md)   
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)   
 [Ausnahmeklasse in Visual Basic](assetId:///9aac396f-34ca-4afb-8e6c-e523cb690ba9)   
 [Ausnahmen\- und Fehlerbehandlung in Visual Basic](assetId:///3e351e73-cf23-40ab-8b60-05794160529e)