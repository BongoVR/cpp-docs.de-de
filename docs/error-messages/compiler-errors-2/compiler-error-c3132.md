---
title: Compiler-Fehler C3132 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3132
dev_langs:
- C++
helpviewer_keywords:
- C3132
ms.assetid: d54a3d12-336a-4ed0-ad4e-43cddac33b5e
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 4922c6095381b42c0b01052421e19f841932be5b
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3132"></a>Compiler-Fehler C3132 generiert
'Funktion-Parameter': Parameterarrays können nur auf einem formalen Argument vom Typ "eindimensionalem verwalteten Arrays" angewendet werden  
  
 Die [ParamArray](https://msdn.microsoft.com/en-us/library/system.paramarrayattribute.aspx) Attribut auf einen Parameter, die keine eindimensionale Arrays angewendet wurde.  
  
 Im folgende Beispiel wird C3132 generiert:  
  
```  
// C3132.cpp  
// compile with: /clr /c  
using namespace System;  
void f( [ParamArray] Int32[,] );   // C3132  
void g( [ParamArray] Int32[] );   // C3132  
  
void h( [ParamArray] array<Char ^> ^ MyArray );   // OK  
  
```
