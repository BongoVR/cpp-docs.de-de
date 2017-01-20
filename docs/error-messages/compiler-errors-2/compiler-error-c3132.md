---
title: "Compilerfehler C3132"
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
  - "C3132"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3132"
ms.assetid: d54a3d12-336a-4ed0-ad4e-43cddac33b5e
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3132
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Funktionsparameter': Parameterarrays können nur auf formale Argumente vom Typ 'eindimensionales verwaltetes Array' angewendet werden  
  
 Das [ParamArray](https://msdn.microsoft.com/en-us/library/system.paramarrayattribute.aspx)\-Attribut wurde auf einen Parameter angewendet, der kein eindimensionales Array war.  
  
 Im folgenden Beispiel wird C3132 generiert:  
  
```  
// C3132.cpp  
// compile with: /clr /c  
using namespace System;  
void f( [ParamArray] Int32[,] );   // C3132  
void g( [ParamArray] Int32[] );   // C3132  
  
void h( [ParamArray] array<Char ^> ^ MyArray );   // OK  
  
```