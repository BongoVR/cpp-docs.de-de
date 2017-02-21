---
title: "Compilerfehler C3460 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3460"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3460"
ms.assetid: adbf8775-10ca-4654-acdf-58dd765351cd
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerfehler C3460
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'type': Nur ein benutzerdefinierter Typ kann weitergeleitet werden.  
  
 Weitere Informationen finden Sie unter [Type Forwarding \(C\+\+\/CLI\)](../../windows/type-forwarding-cpp-cli.md).  
  
## Beispiel  
 Im folgenden Beispiel wird eine Komponente erstellt.  
  
```  
// C3460.cpp // compile with: /LD /clr public ref class R {};  
```  
  
## Beispiel  
 Im folgenden Beispiel wird C3460 generiert:  
  
```  
// C3460_b.cpp // compile with: /clr /c #using "C3460.dll" [assembly:TypeForwardedTo(int::typeid)];   // C3460 [assembly:TypeForwardedTo(R::typeid)];  
```