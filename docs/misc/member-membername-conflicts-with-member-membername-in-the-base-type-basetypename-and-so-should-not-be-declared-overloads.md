---
title: "Member &lt;Membername&gt; steht mit dem Member &#39;&lt;Membername&gt;&#39; im Basistyp &#39;&lt;Basistypname&gt;&#39; in Konflikt und sollte daher nicht als „Overloads“ deklariert werden."
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
  - "bc40021"
  - "vbc40021"
helpviewer_keywords: 
  - "BC40021"
ms.assetid: 2ec72726-ab0e-4545-9c1e-2409eb54482e
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "shoag"
manager: "wpickett"
---
# Member &lt;Membername&gt; steht mit dem Member &#39;&lt;Membername&gt;&#39; im Basistyp &#39;&lt;Basistypname&gt;&#39; in Konflikt und sollte daher nicht als „Overloads“ deklariert werden.
Eine Eigenschaft oder Prozedur verwendet das [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)\-Schlüsselwort, um eine vorhandene Eigenschaft oder Prozedur mit demselben Namen neu zu deklarieren, aber die vorhandene Eigenschaft oder Prozedur befindet sich in der Basisklasse.  
  
 Das Überladen wird verwendet, um mehrere Versionen einer Eigenschaft oder Prozedur in derselben Klasse zu definieren. Sie können keine zusätzliche Version eines Basisklassenmembers definieren, es sei denn, der Basisklassenmember gibt bereits [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md) an.  
  
 Standardmäßig ist diese Meldung eine Warnung. Weitere Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC40021  
  
### So beheben Sie diesen Fehler  
  
-   Wenn Sie beabsichtigen, eine zusätzliche Version der Basisklassenmember zu definieren und auf den Quellcode der Basisklasse zuzugreifen, fügen Sie das [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)\-Schlüsselwort zur Basisklassendefinition hinzu.  
  
-   Der Member in einer abgeleiteten Klasse kann nicht überladen werden, wenn Sie keinen Zugriff auf den Quellcode der Basisklasse haben. Entfernen Sie das `Overloads`\-Schlüsselwort.  
  
-   Wenn Sie den Basisklassenmember ersetzen möchten, anstatt eine zusätzliche Version zu definieren, verwenden Sie das [Overrides](../Topic/Overrides%20\(Visual%20Basic\).md)\-Schlüsselwort anstelle von `Overloads`.  
  
-   Wenn Sie den Basisklassenmember durch einen neuen Member in der abgeleiteten Klasse ausblenden möchten, verwenden Sie das [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md)\-Schlüsselwort anstelle von `Overloads`.  
  
## Siehe auch  
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)