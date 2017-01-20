---
title: "Der Typ von &quot;&lt;Variablenname&gt;&quot; ist mehrdeutig, weil die Schleifenbegrenzungen und die step-Klausel nicht in denselben Typ konvertiert werden"
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
  - "vbc30983"
  - "bc30983"
helpviewer_keywords: 
  - "BC30983"
ms.assetid: 6b97153c-dee3-4429-b92a-2e5a212c864b
caps.latest.revision: 14
caps.handback.revision: "14"
ms.author: "shoag"
manager: "wpickett"
---
# Der Typ von &quot;&lt;Variablenname&gt;&quot; ist mehrdeutig, weil die Schleifenbegrenzungen und die step-Klausel nicht in denselben Typ konvertiert werden
Der Code enthält eine `For...Next`\-Schleife, in der der Compiler aufgrund der folgenden Bedingungen keinen Datentyp für die Schleifensteuerungsvariable ableiten kann:  
  
-   Der Datentyp der Schleifensteuerungsvariablen wird nicht mit einer `As`\-Klausel angegeben.  
  
-   Die Schleifenbegrenzungen und die step\-Variable enthalten mindestens zwei Datentypen.  
  
-   Zwischen den Datentypen sind mehrere Konvertierungen möglich.  
  
-   Es gibt keinen optimalen Typ unter den Kandidaten, sodass die Auswahl des Typs für die Schleifensteuerungsvariable mehrdeutig ist.  
  
 Die folgende Schleife weist beispielsweise eine Schleifenbegrenzung vom Typ `Integer` und eine Schleifenbegrenzung vom Typ `UInteger` auf:  
  
```vb#  
Dim m As Integer = 1 Dim n As UInteger = 10 ' Not valid. ' For i = m To n ' Loop processing. ' Next  
```  
  
 Es wird eine mögliche Konvertierung zwischen `Integer` und `UInteger` sowie eine mögliche Konvertierung zwischen `UInteger` und `Integer` unterstützt, bei beiden handelt es sich jedoch um einschränkende Konvertierungen, sodass keine der beiden eine optimale Wahl darstellt.  
  
 Im nächsten Beispiel wird eine dritte Variable des Typs `Double` hinzugefügt. Sowohl `Integer` als auch `UInteger` verfügen über standardmäßige Erweiterungskonvertierungen für `Double`, wodurch die Konvertierung in `Double` die beste Wahl darstellt. Durch den Typrückschluss wird dem Datentyp `Double` die Schleifensteuerungsvariable `i` zugewiesen.  
  
```vb#  
Dim stepVar As Double = 1 ' Valid. For i = m To n Step stepVar ' Loop processing. Next  
```  
  
 **Fehler\-ID:** BC30983  
  
### So beheben Sie diesen Fehler  
  
-   Konvertieren Sie eine der Variablen explizit in einen Typ, für den die anderen über eine Erweiterungskonvertierung verfügen. Beispiel:  
  
    ```  
    For i = m To CLng(n)  
    ```  
  
-   Verwenden Sie eine `As`\-Klausel, um den Typ der Steuerelementvariablen anzugeben:  
  
    ```  
    For i As Double = m To n   
    ```  
  
## Siehe auch  
 [For...Next\-Anweisung](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Local Type Inference](../Topic/Local%20Type%20Inference%20\(Visual%20Basic\).md)   
 [Option Infer Statement](../Topic/Option%20Infer%20Statement.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)