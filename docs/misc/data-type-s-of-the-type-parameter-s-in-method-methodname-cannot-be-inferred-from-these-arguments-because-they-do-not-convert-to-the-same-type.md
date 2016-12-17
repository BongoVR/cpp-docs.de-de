---
title: "Die Datentypen der Typparameter in der &#39;&lt;Methodenname&gt;&#39;-Methode k&#246;nnen nicht von diesen Argumenten abgeleitet werden, da sie nicht in denselben Typ konvertiert werden."
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
  - "vbc36660"
  - "bc36660"
  - "vbc36657"
  - "bc36657"
helpviewer_keywords: 
  - "BC36660"
  - "BC36657"
ms.assetid: e80c5afd-e16d-4f03-bdf1-c79c4286114b
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "shoag"
manager: "wpickett"
---
# Die Datentypen der Typparameter in der &#39;&lt;Methodenname&gt;&#39;-Methode k&#246;nnen nicht von diesen Argumenten abgeleitet werden, da sie nicht in denselben Typ konvertiert werden.
Die Datentypen der Typparameter in der '\<Methodenname\>'\-Methode können nicht von diesen Argumenten abgeleitet werden, da sie nicht in denselben Typ konvertiert werden. Sie können diesen Fehler möglicherweise beheben, indem Sie die Datentypen explizit angeben.  
  
 Beim Auswerten eines Aufrufs einer generischen Prozedur wurde versucht, über den Typrückschluss den Datentyp \(bzw. die Datentypen\) der Typparameter zu bestimmen. Der Compiler konnte keinen Datentyp finden, der die Einschränkungen aller Argumente erfüllt. Daher wurde dieser Fehler gemeldet.  
  
> [!NOTE]
>  Wenn die Angabe von Argumenten keine Option ist \(z. B. für Abfrageoperatoren in Abfrageausdrücken\), wird nur der erste Satz der Fehlermeldung angezeigt.  
  
 Im folgenden Code wird der Fehler veranschaulicht.  
  
```vb#  
Option Strict Off Module Module1 Sub Main() '' Not valid. Integer and Date do not convert to the same type. 'targetMethod(19, #3/4/2007#) End Sub Sub targetMethod(Of T)(ByVal p1 As T, ByVal p2 As T) End Sub End Module  
```  
  
 **Fehler\-ID:** BC36660 und BC36657  
  
### So beheben Sie diesen Fehler  
  
-   Sie können möglicherweise wie im folgenden Code gezeigt ein oder mehrere Argumente explizit in einen kompatiblen Typ konvertieren:  
  
    ```  
    targetMethod(19, #3/4/2007#.ToOADate)  
    ```  
  
-   Sie können möglicherweise wie im folgenden Code gezeigt einen Datentyp für den oder die Typparameter angeben, in den die Argumente konvertiert werden sollen:  
  
    ```  
    targetMethod(Of String)(19, #3/4/2007#)  
    ```  
  
## Siehe auch  
 [Generic Procedures in Visual Basic](../Topic/Generic%20Procedures%20in%20Visual%20Basic.md)   
 [Type Conversion Functions](../Topic/Type%20Conversion%20Functions%20\(Visual%20Basic\).md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Type Conversions in Visual Basic](../Topic/Type%20Conversions%20in%20Visual%20Basic.md)