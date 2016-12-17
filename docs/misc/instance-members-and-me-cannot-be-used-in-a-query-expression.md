---
title: "Instanzmember und &quot;Me&quot; d&#252;rfen nicht in Abfrageausdr&#252;cken verwendet werden"
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
  - "vbc36535"
  - "bc36535"
helpviewer_keywords: 
  - "BC36535"
ms.assetid: afb5281b-70a7-48c7-a46d-39522b96b1ff
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "shoag"
manager: "wpickett"
---
# Instanzmember und &quot;Me&quot; d&#252;rfen nicht in Abfrageausdr&#252;cken verwendet werden
Eine LINQ\-Abfrage in einer `Structure` enthält einen Verweis auf `Me` oder auf ein Instanzmember der Struktur. Verweise auf `Me` oder Instanzmember sind in Abfrageausdrücken innerhalb einer `Structure` nicht zulässig.  
  
 **Fehler\-ID:** BC36535  
  
### So beheben Sie diesen Fehler  
  
1.  Erstellen Sie eine Kopie des Instanzmembers oder des vom Verweis auf `Me` zurückgegebenen Werts, und verwenden Sie die Kopie im Abfrageausdruck, wie im folgenden Beispiel gezeigt.  
  
    ```vb#  
    Structure SampleStructure Public SearchValue As Integer Public Sub SetSearchValue(ByVal number As Integer) SearchValue = number End Sub Public Sub GetData() Dim sv = SearchValue Dim SampleData = New Integer() {1, 2, 3, 4} Dim query = From number In SampleData _ Where number < sv End Sub End Structure  
    ```  
  
## Siehe auch  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ](../Topic/LINQ%20in%20Visual%20Basic.md)   
 [Me](assetId:///a65973c7-cf06-4547-9b25-9fba885525c2)   
 [Struktur \(Visual Basic\)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0)