---
title: Compilerfehler C2106 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2106
dev_langs: C++
helpviewer_keywords: C2106
ms.assetid: d5c91a2e-04e4-4770-8478-788b98c52a53
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 36196b87acfd2cd7aa064c414b2e9d0f4a2f7ead
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2106"></a>Compilerfehler C2106
'Operator': linke Operand muss ein l-Wert  
  
 Der Operator muss einen l-Wert als dem linken Operanden haben.  
  
 Im folgende Beispiel wird C2106 generiert:  
  
```  
// C2106.cpp  
int main() {  
   int a;  
   1 = a;   // C2106  
   a = 1;   // OK  
}  
```