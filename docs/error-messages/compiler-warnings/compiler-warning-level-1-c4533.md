---
title: Compilerwarnung (Stufe 1) C4533 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4533
dev_langs:
- C++
helpviewer_keywords:
- C4533
ms.assetid: 359fecda-d540-46e5-b214-dbabe9ef50d2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a260cb27529e3ef7ec2b7b7a948578bad320d738
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4533"></a>Compilerwarnung (Stufe 1) C4533
Initialisierung von "Variable" wird von 'Anweisung' übersprungen.  
  
 Eine Anweisung im Programm geändert die ablaufsteuerung, sodass eine Anweisung, die eine Variable initialisiert wurde nicht ausgeführt. Im folgenden Beispiel wird C4533 generiert:  
  
```  
// C4533.cpp  
// compile with: /W1  
#include <stdio.h>  
  
struct A  
{  
   int m_data;  
};  
  
int main()  
{  
   if (1)  
   {  
      goto Label;  
   }  
  
   A a = { 100 };  
  
   Label:   // C4533  
      printf("\n%d", a.m_data);   // prints an uninitialized value  
}  
```