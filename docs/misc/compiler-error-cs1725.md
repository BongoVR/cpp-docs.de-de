---
title: "Compilerfehler CS1725"
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
  - "cs1725"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1725"
ms.assetid: baef9ae3-b036-41d6-972c-9f3cdae1e8bd
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1725
Der Friend\-Assemblyverweis 'Verweis' ist ungültig. Für InternalsVisibleTo\-Deklarationen kann keine Version, keine Kultur, kein öffentliches Schlüsseltoken und keine Prozessorarchitektur angegeben werden.  
  
 Eine Versionskultur kann nicht zu einem Friend\-Assemblyverweis hinzugefügt werden. Teilklassen sollten für Friend\-Assemblys sichtbar sein.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1725 generiert:  
  
```  
// CS1725.cs // compile with: /target:library using System.Runtime.CompilerServices; [assembly:InternalsVisibleTo("partial01,version=1.1.0.0")]   // CS1725 // try the following line instead // [assembly:InternalsVisibleTo("partial01")] partial class TestClass { public static string strBar = "my string"; }  
```  
  
## Siehe auch  
 [Gewusst wie: Erstellen von signierten Friend\-Assemblys](../Topic/How%20to:%20Create%20Signed%20Friend%20Assemblies%20\(C%23%20and%20Visual%20Basic\).md)