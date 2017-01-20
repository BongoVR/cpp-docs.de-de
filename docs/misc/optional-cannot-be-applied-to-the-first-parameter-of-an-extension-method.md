---
title: "&#39;Optional&#39; kann nicht auf den ersten Parameter einer Extensionmethode angewendet werden"
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
  - "bc36553"
  - "vbc36553"
helpviewer_keywords: 
  - "BC36553"
ms.assetid: 8ea0b90c-f155-47a9-988b-5b8009b510af
caps.latest.revision: 19
caps.handback.revision: "19"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;Optional&#39; kann nicht auf den ersten Parameter einer Extensionmethode angewendet werden
'Optional' kann nicht auf den ersten Parameter einer Extensionmethode angewendet werden. Der erste Parameter gibt den zu erweiternden Typ an.  
  
 Der erste Parameter einer Extensionmethode gibt den Datentyp an, der von der Methode erweitert wird. Beim Ausführen der Methode wird der erste Parameter an die Instanz des Datentyps gebunden, der die Methode aufruft. Daher ist der erste Parameter erforderlich und nicht optional.  
  
 Diese Einschränkung gilt nur für den ersten Parameter. Andere Parameter können nach den gleichen Regeln wie in jeder anderen Methode optional oder nicht optional sein. Weitere Informationen finden Sie unter [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md).  
  
 **Fehler\-ID:** BC36553  
  
### So beheben Sie diesen Fehler  
  
-   Wenn Sie möchten, dass der aktuelle erste Parameter den Datentyp angibt, der erweitert wird, entfernen Sie das Schlüsselwort `Optional`.  
  
-   Wenn der aktuelle erste Parameter ein Standardparameter für die Methode ist und Sie nicht wünschen, dass er den Datentyp darstellt, der erweitert werden soll, fügen Sie einen neuen ersten Parameter hinzu.  
  
## Beispiel  
 Der erste Parameter im folgenden Beispiel ist die einzige Anzeige dafür, dass die `Print`\-Methode den `String`\-Datentyp erweitert. Aus diesem Grund kann er nicht optional sein.  
  
```  
<Extension()> Public Sub Print (ByVal str As String) Console.WriteLine(str) End Sub  
```  
  
 Wenn die Extensionmethode wie folgt aufgerufen wird, wird der Parameter `str` in der Methode an `greeting` gebunden – die Instanz von `String`, die `Print` aufruft. Der Compiler verwendet `greeting` als das Argument für die Extensionmethode `Print`.  
  
```  
Dim greeting As String = "Hello" greeting.Print()  
```  
  
## Siehe auch  
 [Erweiterungsmethoden](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Gewusst wie: Definieren optionaler Parameter für eine Prozedur \(Visual Basic\)](assetId:///0b32b312-0da0-489b-96ad-7dcb1f1f8f88)   
 [Optional Parameters](../Topic/Optional%20Parameters%20\(Visual%20Basic\).md)