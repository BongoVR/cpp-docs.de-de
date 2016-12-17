---
title: "Compilerfehler C3669"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "error-reference"
f1_keywords: 
  - "C3669"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3669"
ms.assetid: be9c7ae4-e96f-47ab-922a-39a3537d5ca6
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3669
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Member' : Überschreibungsbezeichner 'override' ist in statischen Funktionen oder Konstruktoren nicht zulässig  
  
 Eine Override wurde falsch angegeben.  Weitere Informationen finden Sie unter [Explizite Überschreibungen](../../windows/explicit-overrides-cpp-component-extensions.md).  
  
## Beispiel  
 Im folgenden Beispiel wird C3669 generiert.  
  
```  
// C3669.cpp  
// compile with: /clr  
public ref struct R {  
   R() override {}   // C3669  
};  
```