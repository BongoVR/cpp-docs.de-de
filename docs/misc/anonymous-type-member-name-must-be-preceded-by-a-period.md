---
title: "Dem Membernamen eines anonymen Typs muss ein Punkt voranstehen."
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
  - "vbc36575"
  - "bc36575"
helpviewer_keywords: 
  - "BC36575"
ms.assetid: b87be29e-39f0-4830-9969-608d71137e3e
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "shoag"
manager: "wpickett"
---
# Dem Membernamen eines anonymen Typs muss ein Punkt voranstehen.
In der Objektinitialisiererliste für eine anonyme Typdeklaration muss einem neuen Membernamen, dem ein Wert zugewiesen wird, ein Punkt vorangestellt sein. Im folgenden Beispiel wird eine gültige sowie eine ungültige Deklaration dargestellt:  
  
```vb#  
' Valid.  
Dim instanceName1 = New With {.memberName = 10}  
' Invalid declaration that causes this error.  
' Dim instanceName2 = New With {memberName = 10}  
```  
  
 **Fehler\-ID:** BC36575  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie einen Punkt vor dem Membernamen hinzu.  
  
## Siehe auch  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)