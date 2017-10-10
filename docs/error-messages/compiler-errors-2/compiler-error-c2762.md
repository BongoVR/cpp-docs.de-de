---
title: Compiler-Fehler C2762 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2762
dev_langs:
- C++
helpviewer_keywords:
- C2762
ms.assetid: 8b81a801-fd48-40a1-8bee-0748795b12e4
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: e121ab82b8e49fb1727e626eea7d060e8def2b8c
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2762"></a>Compiler-Fehler C2762 generiert
'Klasse': Ungültiger Ausdruck als Vorlagenargument für 'Argument'  
  
 Bei Verwendung ["/ Za"](../../build/reference/za-ze-disable-language-extensions.md), konvertiert der Compiler eine ganze Zahl nicht in einen Zeiger.  
  
 Im folgende Beispiel wird C2762 generiert:  
  
```  
// C2762.cpp  
// compile with: /Za  
template<typename T, T *pT>  
class X2 {};  
  
void f2() {  
   X2<int, 0> x21;   // C2762  
   // try the following line instead  
   // X2<int, static_cast<int *>(0)> x22;  
}  
```
