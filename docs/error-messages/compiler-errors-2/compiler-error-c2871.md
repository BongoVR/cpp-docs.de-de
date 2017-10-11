---
title: Compilerfehler C2871 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2871
dev_langs:
- C++
helpviewer_keywords:
- C2871
ms.assetid: 44aeb84d-61f0-45e0-8dad-22a3cd46b7f8
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 0003f04a32ff017234607a90162465549092a013
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2871"></a>Compilerfehler C2871
'Name': ein Namespace mit diesem Namen ist nicht vorhanden.  
  
Dieser Fehler tritt auf, wenn Sie einen Bezeichner übergeben, der keinem Namespace ist ein [mit](../../cpp/namespaces-cpp.md#using_directives) Richtlinie.  
  
## <a name="example"></a>Beispiel  
Im folgende Beispiel wird C2871 generiert:  
  
```cpp  
// C2871.cpp  
// compile with: /c
namespace a {
   int fn(int i) { return i; }
} 
namespace b { 
   using namespace d;   // C2871 because d is not a namespace  
   using namespace a;   // OK
}  
```
