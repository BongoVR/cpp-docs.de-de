---
title: Compilerfehler C2805 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2805
dev_langs: C++
helpviewer_keywords: C2805
ms.assetid: c997dc56-e199-442f-b94e-ac551ec9b015
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 6c314f93f9933fa20051aad91442a2d1ac00b9da
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2805"></a>Compilerfehler C2805
binärer 'Operator Operator' hat zu wenige Parameter  
  
 Der binäre Operator hat keine Parameter.  
  
 Im folgende Beispiel wird C2805 generiert:  
  
```  
// C2805.cpp  
// compile with: /c  
class X {  
public:  
   X operator< ( void );   // C2805 must take one parameter  
   X operator< ( X );   // OK  
};  
```