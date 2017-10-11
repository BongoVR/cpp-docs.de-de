---
title: Compilerfehler C2879 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2879
dev_langs:
- C++
helpviewer_keywords:
- C2879
ms.assetid: ac92b645-2394-49de-8632-43d44e0553ed
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 4bb972ffa8bee016dd158490d123353bd6f46a8e
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2879"></a>Compilerfehler C2879
'Symbol': nur ein vorhandener Namespace mit einem Namespace Aliasdefinition ein alternativer Name gegeben werden kann  
  
 Sie können nicht erstellt werden ein [Namespacealias](../../cpp/namespaces-cpp.md#namespace_aliases) auf ein Symbol, das einen Namespace.  
  
 Im folgende Beispiel wird C2879 generiert:  
  
```  
// C2879.cpp  
int main() {  
   int i;  
   namespace A = i;   // C2879 i is not a namespace  
}  
```
