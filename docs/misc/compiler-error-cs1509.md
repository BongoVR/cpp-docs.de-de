---
title: "Compilerfehler CS1509"
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
  - "CS1509"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1509"
ms.assetid: 51a475c3-f085-49cb-89b0-c6582b68653f
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1509
Die Datei "Datei", auf die verwiesen wird, ist keine Assembly; verwenden Sie stattdessen die Option \/addmodule.  
  
 Eine Ausgabedatei \(Ausgabedatei 1\), die in einer Kompilierung erstellt wurde, in der [\/target:module](../Topic/-target:module%20\(C%23%20Compiler%20Options\).md) \(hat kein Assemblymanifest\) verwendet wurde, wurde für [\/reference](../Topic/-reference%20\(C%23%20Compiler%20Options\).md) angegeben. Somit wird keine Assembly an die Assembly für das aktuelle Programm angefügt, sondern die Metadateninformationen in Ausgabedatei 1 werden der Assembly für das aktuelle Programm hinzugefügt.