---
title: "An dieser Stelle d&#252;rfen XML-Literale nur in runden Klammern eingeschlossen stehen."
ms.custom: na
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc31198"
  - "vbc31198"
helpviewer_keywords: 
  - "BC31198"
ms.assetid: 97b16076-39ff-430a-9c65-073d01bcb08e
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# An dieser Stelle d&#252;rfen XML-Literale nur in runden Klammern eingeschlossen stehen.
Die Deklaration eines XML\-Literals wird in einem Ausdruck an einer Stelle verwendet, die mehrdeutig für den [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)]\-Compiler ist. Der [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)]\-Compiler kann also nicht feststellen, ob das Kleiner\-als\-Zeichen \(\<\) als Vergleichsoperator oder Startzeichen eines XML\-Literals vorgesehen ist. Der folgende Code veranschaulicht dies:  
  
 \[Visual Basic\]  
  
```  
' Generates an error. Dim queryResult = From element In elements _ Where <sample>Value</sample> = "Value" _ Select element  
```  
  
 **Fehler\-ID:** BC31198  
  
### So beheben Sie diesen Fehler  
  
-   Schließen Sie die Deklaration des XML\-Literals in Klammern ein, wie im folgenden Beispiel dargestellt:  
  
    ```vb#  
    Dim queryResult = From element In elements _ Where (<sample> Value</sample>) = "Value" _ Select element  
    ```  
  
-   Ändern Sie Ihren Code, sodass er auf ein vorhandenes XML\-Literal verweist, wie im folgenden Beispiel dargestellt:  
  
    ```vb#  
    Dim queryResult = From element In elements _ Where e.<sample>.Value = "Value" _ Select element  
    ```  
  
## Siehe auch  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)   
 [XML](../Topic/XML%20in%20Visual%20Basic.md)