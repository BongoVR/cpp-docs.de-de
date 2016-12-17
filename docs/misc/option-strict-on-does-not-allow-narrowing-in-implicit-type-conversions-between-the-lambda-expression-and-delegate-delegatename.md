---
title: "&quot;Option Strict On&quot; l&#228;sst keine Einschr&#228;nkungen in impliziten Typkonvertierungen zwischen dem lambda-Ausdruck und dem Delegaten &quot;&lt;Delegatname&gt;&quot; zu."
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
  - "bc36662"
  - "vbc36662"
helpviewer_keywords: 
  - "BC36662"
ms.assetid: 4504497b-56ba-4631-ad7b-59975f7fee04
caps.latest.revision: 4
caps.handback.revision: "4"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;Option Strict On&quot; l&#228;sst keine Einschr&#228;nkungen in impliziten Typkonvertierungen zwischen dem lambda-Ausdruck und dem Delegaten &quot;&lt;Delegatname&gt;&quot; zu.
Mit `Option Strict` On" können Sie keine einschränkende Konvertierung zwischen dem Datentyp eines Parameters in einem Delegaten und dem entsprechenden Parameter eines lambda\-Ausdrucks, der einer Variablen dieses Delegattyps zugewiesen ist, vornehmen. Im folgenden Code verfügt z. B. Delegat `Del` über einen Parameter vom Typ `Integer`.  
  
```vb#  
Delegate Function Del(ByVal p As Integer) As String  
```  
  
 Daher kann der entsprechende Parameter eines beliebigen lambda\-Ausdrucks, der einer Variablen vom Typ `Del` zugewiesen ist, ein `Integer` oder ein beliebiger Datentyp sein, für den eine erweiternde Konvertierung von `Integer` vorhanden ist.  
  
```vb#  
' Valid. Dim example1 As Del = Function(n As Integer) "Valid" Dim example2 As Del = Function(n As Long) "Valid" ' Not valid. Dim example3 As Del = Function(n As Short) "Not Valid"  
```  
  
 **Fehler\-ID:** BC36662  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie den Datentyp des Parameters im Delegaten oder den lambda\-Ausdrucks, sodass die erforderliche erweiternde Beziehung vorhanden ist.  
  
-   Geben Sie im lambda\-Ausdruck keine Parameterdatentypen an. Die Typen werden von den entsprechenden Parametern im Delegaten abgeleitet.  
  
    ```vb#  
    Dim example4 As Del = Function(n) "Valid"  
    ```  
  
## Siehe auch  
 [Lambda Expressions](../Topic/Lambda%20Expressions%20\(Visual%20Basic\).md)   
 [Delegates](../Topic/Delegates%20\(Visual%20Basic\).md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Relaxed Delegate Conversion](../Topic/Relaxed%20Delegate%20Conversion%20\(Visual%20Basic\).md)