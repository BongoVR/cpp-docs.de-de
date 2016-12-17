---
title: "Argument is missing in &#39;\&#39; escape sequence."
ms.custom: na
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.message.VS_E_RE_ESCAPEMISSINGARG"
  - "vs.message.0x800A00BD"
ms.assetid: 5bd6559b-8cd9-450f-91c8-335ff1b1ef86
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "mblome"
manager: "douge"
---
# Argument is missing in &#39;\&#39; escape sequence.
Im Allgemeinen tritt dieser Fehler beim Suchen oder Ersetzen auf, wenn in einer Suchzeichenfolge reguläre Ausdrücke oder Platzhalter verwendet werden.  Hervorgerufen wird er durch einen einzelnen umgekehrten Schrägstrich \(`\`\) am Ende eines Musters oder durch `\x` oder `\u`, die ohne gültiges Unicode\-Hexadezimalzeichen eingegeben werden.  
  
### So beheben Sie diesen Fehler  
  
1.  Wenn Sie unter Verwendung des Escapezeichens für einen regulären Ausdruck suchen möchten, geben Sie `\` ein.  
  
2.  Wenn Sie nach einem Unicode\-Zeichen suchen möchten, geben Sie `\x` oder `\u` ein, gefolgt von einem gültigen Unicode\-Wert.  
  
3.  Wenn Sie tatsächlich nach dem umgekehrten Schrägstrich suchen möchten, verwenden Sie `\\`.  
  
## Siehe auch  
 [Verwenden von regulären Ausdrücken in Visual Studio](../Topic/Using%20Regular%20Expressions%20in%20Visual%20Studio.md)   
 [NIB: Find and Replace, Quick Find](assetId:///dad03582-4931-4893-83ba-84b37f5b1600)   
 [Suchen in Dateien](../Topic/Find%20in%20Files.md)