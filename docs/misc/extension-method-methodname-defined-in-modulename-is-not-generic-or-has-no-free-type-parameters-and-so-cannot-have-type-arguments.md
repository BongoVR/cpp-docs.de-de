---
title: "Die in &quot;&lt;Modulname&gt;&quot; definierte Erweiterungsmethode &quot;&lt;Methodenname&gt;&quot; ist nicht generisch (oder besitzt keine Parameter mit einem freien Typ) und darf daher keine Typargumente enthalten."
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
  - "bc36907"
  - "vbc36907"
helpviewer_keywords: 
  - "BC36907"
ms.assetid: 45191e93-89d1-48ec-99a5-ff9661a2a6ee
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "shoag"
manager: "wpickett"
---
# Die in &quot;&lt;Modulname&gt;&quot; definierte Erweiterungsmethode &quot;&lt;Methodenname&gt;&quot; ist nicht generisch (oder besitzt keine Parameter mit einem freien Typ) und darf daher keine Typargumente enthalten.
Ein Typargument wurde in einem Aufruf einer Erweiterungsmethode angegeben, die weder generische Parameter noch generische Parameter, für die noch kein Typ angegeben ist, enthält. Der folgende Code verursacht beispielsweise diesen Fehler:  
  
```vb#  
' The extension method is not generic. <Extension()> _ Sub Example(ByVal str As String) ' Body of the Sub. End Sub  
```  
  
```vb#  
Dim str = "hi" '' The call to Example specifies a type argument. '' Not valid. 'str.Example(Of String)()  
```  
  
 **Fehler\-ID:** BC36907  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie der Definition der Erweiterungsmethode einen Typparameter hinzu.  
  
-   Entfernen Sie das zusätzliche Typargument aus dem Prozeduraufruf.  
  
## Siehe auch  
 [Erweiterungsmethoden](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../Topic/Generic%20Procedures%20in%20Visual%20Basic.md)