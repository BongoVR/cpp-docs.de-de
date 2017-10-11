---
title: Compilerfehler C3363 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3363
dev_langs:
- C++
helpviewer_keywords:
- C3363
ms.assetid: 41aa922f-608e-4f7a-ba66-451fc1161935
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: e0601fed8638d6af814404517f495136a5d7d8d0
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3363"></a>Compilerfehler C3363
"Typ" : "Typ-ID" kann nur auf einen Typ angewendet werden.  
  
 Der [typeid](../../windows/typeid-cpp-component-extensions.md) -Operator wurde falsch verwendet.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3363 generiert:  
  
```  
// C3363.cpp  
// compile with: /clr  
int main() {  
   System::typeid;   // C3363  
}  
```
