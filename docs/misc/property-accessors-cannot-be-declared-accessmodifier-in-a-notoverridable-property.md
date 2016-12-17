---
title: "Eigenschaftenaccessoren k&#246;nnen in einer NotOverridable-Eigenschaft nicht als &quot;&lt;Zugriffsmodifizierer&gt;&quot; deklariert werden."
ms.custom: na
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc31106"
  - "bc31106"
helpviewer_keywords: 
  - "BC31106"
ms.assetid: 84bcb157-9c33-4e4f-89a9-c5e6cb73028b
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Eigenschaftenaccessoren k&#246;nnen in einer NotOverridable-Eigenschaft nicht als &quot;&lt;Zugriffsmodifizierer&gt;&quot; deklariert werden.
Eine [Get Statement](../Topic/Get%20Statement.md) oder [Set Statement](../Topic/Set%20Statement%20\(Visual%20Basic\).md) in einer `NotOverridable`\-Eigenschaft enthält das `Private`\-Schlüsselwort.  
  
 Anhand der folgenden logischen Beschreibung wird erläutert, warum `NotOverridable` und `Private` nicht in einer [Property Statement](../Topic/Property%20Statement.md) kombiniert werden können:  
  
1.  Eine Eigenschaft oder Prozedur, die keine Basisklasseneigenschaft bzw. \-prozedur überschreibt, hat die Standardeinstellung [NotOverridable](../Topic/NotOverridable%20\(Visual%20Basic\).md).  
  
2.  Eine Eigenschaft oder Prozedur in einer abgeleiteten Klasse, die eine Basisklasseneigenschaft bzw. \-prozedur überschreibt, hat dagegen die Standardeinstellung [Overridable](../Topic/Overridable%20\(Visual%20Basic\).md). Um die Hierarchie des Überschreibens zu beenden, können Sie diese als `NotOverridable` deklarieren. Dies ist der einzige Kontext, in dem Sie `NotOverridable` verwenden können. Das heißt, Sie können `NotOverridable` nur in Verbindung mit [Overrides](../Topic/Overrides%20\(Visual%20Basic\).md) verwenden.  
  
3.  Ist eine Eigenschaft oder Prozedur einer Basisklasse als [Private](../Topic/Private%20\(Visual%20Basic\).md) deklariert ist, kann diese Eigenschaft oder Prozedur nicht von einer abgeleiteten Klasse überschrieben werden, da diese nicht auf die Eigenschaft oder Prozedur zugreifen kann. Daher können Sie `Private` nicht in Verbindung mit `Overridable` verwenden.  
  
4.  Um eine Eigenschaft oder Prozedur zu überschreiben, muss die überschreibende Eigenschaft oder Prozedur nicht nur dieselbe Signatur, sondern auch dieselbe Zugriffsebene haben. Das bedeutet, dass eine überschreibende Eigenschaft oder Prozedur `Private` nicht angeben kann, weil eine überschreibbare Eigenschaft oder Prozedur `Private` nicht angeben kann.  
  
5.  Da Sie `NotOverridable` nur für eine überschreibende Eigenschaft oder Prozedur angeben können, können Sie dieses Schlüsselwort nicht mit `Private` kombinieren.  
  
 Aufgrund derselben Logik können die einzelnen Eigenschaftenprozeduren \(`Get` und `Set`\) einer überschreibenden Eigenschaft nicht `Private` sein.  
  
 **Fehler\-ID:** BC31106  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie das `Private`\-Schlüsselwort aus der `Get`\- oder `Set`\-Anweisung, oder entfernen Sie die Schlüsselwörter `Overrides` und `NotOverridable` aus der `Property`\-Anweisung.  
  
## Siehe auch  
 [Eigenschaftenprozeduren](../Topic/Property%20Procedures%20\(Visual%20Basic\).md)   
 [Differences Between Shadowing and Overriding](../Topic/Differences%20Between%20Shadowing%20and%20Overriding%20\(Visual%20Basic\).md)   
 [How to: Declare a Property with Mixed Access Levels](../Topic/How%20to:%20Declare%20a%20Property%20with%20Mixed%20Access%20Levels%20\(Visual%20Basic\).md)