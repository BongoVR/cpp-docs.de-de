---
title: "Compilerfehler CS1014"
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
  - "CS1014"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1014"
ms.assetid: 60c1e9af-5a0d-4ae0-a2e6-881b0d1535e9
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1014
get\- oder set\-Accessor erwartet.  
  
 In einer Eigenschaftendeklaration wurde eine Methodendeklaration gefunden. Sie können nur `get`\- und `set`\-Methoden in einer Eigenschaft deklarieren.  
  
 Weitere Informationen zu Eigenschaften finden Sie unter [Verwenden von Eigenschaften](../Topic/Using%20Properties%20\(C%23%20Programming%20Guide\).md).  
  
## Beispiel  
 Im folgenden Beispiel wird CS1014 generiert:  
  
```  
// CS1014.cs // compile with: /target:library class Sample { public int TestProperty { get { return 0; } int z;   // CS1014  not get or set } }  
```