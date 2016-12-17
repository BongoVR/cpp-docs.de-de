---
title: "Eigenschaft &#39;&lt;Eigenschaftenname&gt;&#39; deklariert implizit &#39;&lt;Name des impliziten Members&gt;&#39;, was zu einem Konflikt mit einem Member f&#252;hrt, der implizit f&#252;r Member &#39;&lt;Membername&gt;&#39; in der Basisklasse &#39;&lt;Basisklassenname&gt;&#39; deklariert wird."
ms.custom: na
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc40024"
  - "bc40024"
helpviewer_keywords: 
  - "BC40024"
ms.assetid: fab4f290-a41f-47d6-9bdb-44eb8dd395d5
caps.latest.revision: 14
caps.handback.revision: "14"
ms.author: "shoag"
manager: "wpickett"
---
# Eigenschaft &#39;&lt;Eigenschaftenname&gt;&#39; deklariert implizit &#39;&lt;Name des impliziten Members&gt;&#39;, was zu einem Konflikt mit einem Member f&#252;hrt, der implizit f&#252;r Member &#39;&lt;Membername&gt;&#39; in der Basisklasse &#39;&lt;Basisklassenname&gt;&#39; deklariert wird.
Member '\<Membername1\>' deklariert implizit '\<Name des impliziten Members\>', was zu einem Konflikt mit einem Member führt, der implizit für Member '\<Membername2\>' in der Basisklasse '\<Basisklassenname\>' deklariert wird. Daher sollte der Member nicht als „Overloads“ deklariert werden.  
  
 Eine Eigenschaft in einer abgeleiteten Klasse generiert einen impliziten Member mit demselben Namen wie für einen impliziten Member der Basisklasse und gibt das [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)\-Schlüsselwort an.  
  
 Überladen wird verwendet, um mehrere Versionen einer Eigenschaft oder Prozedur in derselben Klasse zu definieren. Sie können keine zusätzliche Version eines Basisklassenmembers definieren, es sei denn, der Basisklassenmember gibt bereits `Overloads` an. Da implizite Member `Overloads` nicht angeben, geht der Compiler davon aus, dass diese Eigenschaft den impliziten Member der Basisklasse überschattet \([Shadows](../Topic/Shadows%20\(Visual%20Basic\).md)\).  
  
 Der [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)]\-Compiler erstellt implizite Member, die bestimmten von Ihnen deklarierten Programmierelementen entsprechen. In der folgenden Tabelle werden diese impliziten oder auch *synthetischen* Member zusammengefasst.  
  
|Deklariertes Element|Implizit erstellte Member|  
|--------------------------|-------------------------------|  
|Enumeration|`value__`\-Member|  
|Ereignis|`add_<eventname>`\-Prozedur<br /><br /> `remove_<eventname>`\-Prozedur<br /><br /> `<eventname>Event`\-Feld<br /><br /> `<eventname>EventHandler`\-Delegat|  
|Eigenschaft|`get_<propertyname>`\-Prozedur<br /><br /> `set_<propertyname>`\-Prozedur|  
|`My.Form`\-Member, `My.WebService`\-Member oder Member einer mit dem Attribut <xref:Microsoft.VisualBasic.MyGroupCollectionAttribute> gekennzeichneten Klasse|`m_<variablename>` `Static`\-Variable<br /><br /> `<variablename>`\-Eigenschaft<br /><br /> `get_<variablename>`\-Prozedur<br /><br /> `set_<variablename>`\-Prozedur|  
|`WithEvents`\-Variable|`_<variablename>`\-Variable<br /><br /> `<variablename>`\-Eigenschaft<br /><br /> `get_<variablename>`\-Prozedur<br /><br /> `set_<variablename>`\-Prozedur|  
  
 Aufgrund des Risikos von Namenskonflikten sollten Sie vermeiden, deklarierte Programmierelemente in derselben Form wie eines dieser impliziten Member zu benennen. Sie sollten z. B. Elementnamen vermeiden, die mit `get_` oder `set_` beginnen.  
  
 Standardmäßig ist diese Meldung eine Warnung. Weitere Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC40024  
  
### So beheben Sie diesen Fehler  
  
-   Wenn Sie den impliziten Basisklassenmember ausblenden oder überschatten möchten, sollten Sie das [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)\-Schlüsselwort in die Deklaration der Eigenschaft durch das [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md)\-Schlüsselwort ersetzen.  
  
-   Wenn Sie nicht beabsichtigen, den impliziten Member der Basisklasse zu überschatten, ändern Sie den Namen der Eigenschaft, um Konflikte mit den in der obigen Tabelle aufgelisteten Namen zu vermeiden.  
  
## Siehe auch  
 [Declared Element Names](../Topic/Declared%20Element%20Names%20\(Visual%20Basic\).md)