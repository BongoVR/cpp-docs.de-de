---
title: "Compilerwarnung (Stufe 1) C4117 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4117"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4117"
ms.assetid: c45aa281-4cc1-4dfd-bd32-bd7a60ddd577
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerwarnung (Stufe 1) C4117
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Makroname 'Name' ist reserviert. 'Befehl' wird ignoriert.  
  
### Dieser Fehler kann eine der folgenden Ursachen haben:  
  
1.  Versuchen Sie, ein vordefiniertes Makro zu definieren bzw. dessen Definition aufzuheben.  
  
2.  Versuchen Sie, den **defined**\-Präprozessoroperator zu definieren bzw. dessen Definition aufzuheben.  
  
 Im folgenden Beispiel wird C4117 generiert:  
  
```  
// C4117.cpp // compile with: /W1 #define __FILE__ test         // C4117. __FILE__ is a predefined macro #define ValidMacroName test   // ok int main() { }  
```