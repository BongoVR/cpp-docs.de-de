---
title: "Compilerwarnung (Stufe 4) C4932"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "C4932"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4932"
ms.assetid: 0b8d88cc-21f6-45cb-a9f5-1795b7db0dfa
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "corob"
manager: "ghogen"
---
# Compilerwarnung (Stufe 4) C4932
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

\_\_identifier\(Bezeichner\) und \_\_identifier\(Bezeichner\) sind nicht differenzierbar.  
  
 Der Compiler kann bei dem an [\_\_identifier](../../windows/identifier-cpp-cli.md) übergebenen Parameter nicht zwischen **\_finally** und `__finally` oder `__try` und **\_try** unterscheiden. Sie sollten nicht beide Bezeichner im selben Programm verwenden, weil dadurch der Fehler [C2374](../../error-messages/compiler-errors-1/compiler-error-c2374.md) verursacht wird.  
  
 Im folgenden Beispiel wird C4932 generiert:  
  
```  
// C4932.cpp // compile with: /clr /W4 /WX int main() { int __identifier(_finally) = 245;   // C4932 int __identifier(__finally) = 25;   // C4932 }  
```