---
title: "Compilerfehler C3309 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3309"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3309"
ms.assetid: 75ee16e3-7d4e-4c41-b3cb-64e9849c3aab
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C3309
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"macro\_name": Ein Modulname kann kein Makro oder Schlüsselwort sein  
  
 Der Wert, den Sie an die name\-Eigenschaft des Modulattributs übergeben, darf kein Symbol für den zu erweiternden Präprozessor sein; es muss ein Zeichenfolgenliteral sein.  
  
 Im folgenden Beispiel wird C3309 generiert:  
  
```  
// C3309.cpp #define NAME MyModule [module(name="NAME")];   // C3309 // Try the following line instead // [module(name="MyModule")]; [coclass] class MyClass { public: void MyFunc(); }; int main() { }  
```