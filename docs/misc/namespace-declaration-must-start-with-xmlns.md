---
title: "Die Namespacedeklaration muss mit &quot;xmlns&quot; beginnen."
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
  - "bc31187"
  - "vbc31187"
helpviewer_keywords: 
  - "BC31187"
ms.assetid: 64c6a033-7cdc-48a0-bff0-bdd045cb13ad
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "shoag"
manager: "wpickett"
---
# Die Namespacedeklaration muss mit &quot;xmlns&quot; beginnen.
Ein XML\-Namespace wurde ohne den erforderlichen `xmlns`\-Bezeichner angegeben. Der `xmlns`\-Bezeichner muss nur Kleinbuchstaben enthalten.  
  
 **Fehler\-ID:** BC31187  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie den `xmlns`\-Bezeichner, wenn Sie einen XML\-Namespace deklarieren. Beachten Sie folgendes Beispiel:  
  
    ```vb#  
    Imports <xmlns:ns="http://SampleNamespace">  
    ```  
  
## Siehe auch  
 [Imports Statement \(XML Namespace\)](../Topic/Imports%20Statement%20\(XML%20Namespace\).md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML](../Topic/XML%20in%20Visual%20Basic.md)