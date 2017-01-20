---
title: "Die Datentypen der Typparameter in der in &quot;&lt;Typname&gt;&quot; definierten Erweiterungsmethode &quot;&lt;Methodenname&gt;&quot; k&#246;nnen nicht von diesen Argumenten abgeleitet werden, da sie nicht in denselben Typ konvertiert werden"
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
  - "vbc36658"
  - "bc36661"
  - "vbc36661"
  - "bc36658"
helpviewer_keywords: 
  - "BC36661"
  - "BC36658"
ms.assetid: 0bff97fd-cbe9-4433-8192-6498c6fb5d04
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "shoag"
manager: "wpickett"
---
# Die Datentypen der Typparameter in der in &quot;&lt;Typname&gt;&quot; definierten Erweiterungsmethode &quot;&lt;Methodenname&gt;&quot; k&#246;nnen nicht von diesen Argumenten abgeleitet werden, da sie nicht in denselben Typ konvertiert werden
Die Datentypen der Typparameter in der in "\<Typname\>" definierten Erweiterungsmethode "\<Methodenname\>" können nicht von diesen Argumenten abgeleitet werden, da sie nicht in denselben Typ konvertiert werden. Sie können diesen Fehler möglicherweise beheben, indem Sie die Datentypen explizit angeben.  
  
 Beim Auswerten eines Aufrufs einer generischen Erweiterungsmethode wurde versucht, über den Typrückschluss den Datentyp \(oder die Datentypen\) des Typparameters \(oder der Typparameter\) zu bestimmen. Der Compiler konnte keinen Datentyp finden, der die Einschränkungen aller Argumente erfüllt. Daher wurde dieser Fehler gemeldet.  
  
> [!NOTE]
>  Wenn die Angabe von Argumenten keine Option ist \(z. B. für Abfrageoperatoren in Abfrageausdrücken\), wird nur der erste Satz der Fehlermeldung angezeigt.  
  
 Im folgenden Code wird der Fehler veranschaulicht.  
  
```vb#  
Option Strict Off Module Module3 Sub Main() Dim c1 As New Class1 '' Not valid. Integer and Date do not convert to the same type. 'c1.targetMethod(19, #3/4/2007#) End Sub <System.Runtime.CompilerServices.Extension()> _ Sub targetMethod(Of T)(ByVal p0 As Class1, ByVal p1 As T, ByVal p2 As T) End Sub Class Class1 End Class End Module  
```  
  
 **Fehler\-ID:** BC36661 und BC36658  
  
### So beheben Sie diesen Fehler  
  
-   Sie können möglicherweise wie im folgenden Code gezeigt ein oder mehrere Argumente explizit in einen kompatiblen Typ konvertieren:  
  
    ```  
    c1.targetMethod(19, #3/4/2007#.ToOADate)  
    ```  
  
-   Sie können möglicherweise wie im folgenden Code gezeigt einen Datentyp für den oder die Typparameter angeben, in den die Argumente konvertiert werden sollen:  
  
    ```  
    c1.targetMethod(Of String)(19, #3/4/2007#)  
    ```  
  
## Siehe auch  
 [Erweiterungsmethoden](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Relaxed Delegate Conversion](../Topic/Relaxed%20Delegate%20Conversion%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../Topic/Generic%20Procedures%20in%20Visual%20Basic.md)   
 [Type Conversion Functions](../Topic/Type%20Conversion%20Functions%20\(Visual%20Basic\).md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Type Conversions in Visual Basic](../Topic/Type%20Conversions%20in%20Visual%20Basic.md)