---
title: Compilerfehler C2451 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2451
dev_langs:
- C++
helpviewer_keywords:
- C2451
ms.assetid: a64c93a5-ab8d-4d39-ae57-9ee7ef803036
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2344ba4629a4f35556d8fc6c2e6760cadbc6392b
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2451"></a>Compilerfehler C2451
bedingter Ausdruck des Typs 'Typ' ist nicht zulässig  
  
 Der bedingte Ausdruck wird in einen Integer-Datentyp.  
  
 Im folgende Beispiel wird C2451 generiert:  
  
```  
// C2451.cpp  
class B {};  
  
int main () {  
   B b1;  
   int i = 0;  
   if (b1)   // C2451  
   // try the following line instead  
   // if (i)  
      ;  
}  
```