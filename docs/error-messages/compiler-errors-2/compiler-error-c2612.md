---
title: Compiler-Fehler C2612 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2612
dev_langs: C++
helpviewer_keywords: C2612
ms.assetid: 6faacfd6-4455-41a2-808e-0f6799f84d6d
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 51859278f3f1651bfa183eaaeaeae25802fd8cf7
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2612"></a>Compiler-Fehler C2612 generiert
nachfolgende 'Char' in der Initialisiererliste Base bzw. dieses Element nicht zulässig  
  
 Ein Zeichen, die nach der letzten Basis oder ein Member in einer Initialisiererliste angezeigt werden.  
  
 Im folgende Beispiel wird C2612 generiert:  
  
```  
// C2612.cpp  
class A {  
public:  
   int i;  
   A( int ia ) : i( ia ) + {};   // C2612  
};  
```