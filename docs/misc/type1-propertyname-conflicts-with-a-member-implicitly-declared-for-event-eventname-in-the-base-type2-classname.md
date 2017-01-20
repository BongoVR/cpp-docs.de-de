---
title: "&lt;Typ1 &quot;&lt;Eigenschaftsname&gt;&quot; steht mit einem Member in Konflikt, der implizit f&#252;r das Ereignis &quot;&lt;Ereignisname&gt;&quot; in der Basis&lt;typ2&gt; &quot;&lt;Klassenname&gt;&quot; deklariert wurde."
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
  - "vbc40014"
  - "bc40014"
helpviewer_keywords: 
  - "BC40014"
ms.assetid: 100534b9-d533-4e94-a2a7-0ed26426965b
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;Typ1 &quot;&lt;Eigenschaftsname&gt;&quot; steht mit einem Member in Konflikt, der implizit f&#252;r das Ereignis &quot;&lt;Ereignisname&gt;&quot; in der Basis&lt;typ2&gt; &quot;&lt;Klassenname&gt;&quot; deklariert wurde.
Eine Eigenschaft wird mit dem gleichen Namen deklariert wie ein impliziter Member, der von einem Ereignis in der Basisklasse gebildet wird. Wenn z. B. die Basisklasse ein Ereignis mit dem Namen `Event1` deklariert, generiert der Compiler die impliziten Prozeduren `add_Event1` und `remove_Event1`. Wenn die Eigenschaft in dieser Klasse einen dieser Namen besitzt, muss sie den Member der Basisklasse überschatten.  
  
 Diese Meldung ist eine Warnung.`Shadows` wird standardmäßig angenommen. Weitere Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC40014  
  
### So beheben Sie diesen Fehler  
  
1.  Um den Member der Basisklasse auszublenden, fügen Sie der Deklaration der Eigenschaft das `Shadows`\-Schlüsselwort hinzu.  
  
2.  Wenn Sie den Basisklassenmember nicht ausblenden möchten, ändern Sie den Namen der Eigenschaft.  
  
## Siehe auch  
 [Property Statement](../Topic/Property%20Statement.md)   
 [Event Statement](../Topic/Event%20Statement.md)   
 [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md)   
 [Shadowing in Visual Basic](../Topic/Shadowing%20in%20Visual%20Basic.md)