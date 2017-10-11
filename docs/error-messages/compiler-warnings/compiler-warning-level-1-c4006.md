---
title: Compilerwarnung (Stufe 1) C4006 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4006
dev_langs:
- C++
helpviewer_keywords:
- C4006
ms.assetid: f1a59819-0fd2-4361-8e3a-99e4b514b8e1
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: d7c09f256223decda7d2a2e52cd6cb8c29f21b1b
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-warning-level-1-c4006"></a>Compilerwarnung (Stufe 1) C4006
\##undef erwartet einen Bezeichner  
  
 Die `#undef` -Direktive hat keinen Bezeichner zum Aufheben der Definition angegeben. Die Direktive wird ignoriert. Stellen Sie sicher, dass Sie einen Bezeichner angeben, um diese Warnung zu beheben. Im folgenden Beispiel wird C4006 generiert:  
  
```  
// C4006.cpp  
// compile with: /W1  
#undef   // C4006  
  
// try..  
// #undef TEST  
  
int main() {  
}  
```
