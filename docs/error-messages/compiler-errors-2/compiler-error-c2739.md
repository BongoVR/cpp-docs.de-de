---
title: Compiler-Fehler C2739 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2739
dev_langs:
- C++
helpviewer_keywords:
- C2739
ms.assetid: 5b63e435-7631-43d7-805e-f2adefb7e517
caps.latest.revision: 11
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: b6d2647fe6addc8f5c68ef70b91a244782f467a4
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2739"></a>Compiler-Fehler C2739 generiert
"Nummer" : Explizit verwaltet oder WinRT-Arraydimensionen müssen zwischen 1 und 32 liegen  
  
 Eine Arraydimension lag nicht zwischen 1 und 32.  
  
 Im folgenden Beispiel wird C2739 generiert und gezeigt, wie Sie diesen Fehler beheben:  
  
```  
// C2739.cpp  
// compile with: /clr  
int main() {  
   array<int, -1>^a;   // C2739  
   // try the following line instead  
   // array<int, 2>^a;  
}  
```
