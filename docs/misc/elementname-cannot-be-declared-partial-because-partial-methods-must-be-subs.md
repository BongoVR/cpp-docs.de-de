---
title: "&#39;&lt;Elementname&gt;&#39; kann nicht als &#39;Partial&#39; deklariert werden, da partielle Methoden untergeordnete Methoden sein m&#252;ssen."
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
  - "vbc31437"
  - "bc31437"
helpviewer_keywords: 
  - "BC31437"
ms.assetid: 31ca12ab-2c26-4907-a253-e7c57bb4f34b
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;Elementname&gt;&#39; kann nicht als &#39;Partial&#39; deklariert werden, da partielle Methoden untergeordnete Methoden sein m&#252;ssen.
Nur `Sub`\-Prozeduren können als partielle Methoden deklariert werden. Beispielsweise verursacht der folgende Code diesen Fehler, da `partialMethod` eine Funktion ist.  
  
```  
' Partial Private Function partialMethod(ByVal n As Integer) As Integer ' End Function  
```  
  
 **Fehler\-ID:** BC31437  
  
### So beheben Sie diesen Fehler  
  
-   Konvertieren Sie, was Sie als partielle Methode deklarieren, in eine `Sub`.  
  
-   Verwenden Sie in diesem Fall keine partielle Methode.  
  
## Siehe auch  
 [Partial Methods](../Topic/Partial%20Methods%20\(Visual%20Basic\).md)   
 [Sub Procedures](../Topic/Sub%20Procedures%20\(Visual%20Basic\).md)