---
title: Compiler-Fehler C2714 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2714
dev_langs: C++
helpviewer_keywords: C2714
ms.assetid: 401a5a42-660c-4bad-9d63-1a2d092bc489
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 1f0fc4847cc6f3ab50f840b1ed5a097cc405cff8
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2714"></a>Compiler-Fehler C2714 generiert
__alignof(void) ist nicht zulässig.  
  
 Zu einem Operator wurde ein ungültiger Wert übergeben.  
  
 Finden Sie unter [__alignof-Operator](../../cpp/alignof-operator.md) für Weitere Informationen.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C2714 generiert.  
  
```  
// C2714.cpp  
int main() {  
   return __alignof(void);   // C2714  
   return __alignof(char);   // OK  
}  
```