---
title: "Anonyme Typen m&#252;ssen mindestens einen Member enthalten."
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
  - "bc36574"
  - "vbc36574"
helpviewer_keywords: 
  - "BC36574"
ms.assetid: fdc8dd47-ea38-49e8-8dd5-676f726cd101
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "shoag"
manager: "wpickett"
---
# Anonyme Typen m&#252;ssen mindestens einen Member enthalten.
Die Initialisiererliste in der Deklaration eines anonymen Typs darf nicht leer sein.  
  
```  
' Not valid. ' Dim anonInstance = New With {}  
```  
  
 **Fehler\-ID:** BC36574  
  
### So beheben Sie diesen Fehler  
  
-   Deklarieren Sie einen Member innerhalb der geschweiften Klammern, wie im folgenden Code gezeigt.  
  
    ```  
    Dim anonInstance = New With {.MemberName = "value"}  
    ```  
  
## Siehe auch  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)