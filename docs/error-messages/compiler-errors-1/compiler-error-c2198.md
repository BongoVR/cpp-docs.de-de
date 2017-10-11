---
title: Compilerfehler C2198 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2198
dev_langs:
- C++
helpviewer_keywords:
- C2198
ms.assetid: 638a845c-9d7f-4115-a9aa-d72455605668
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 0da955515b5ad51836a82563fcfdf8d70de14470
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2198"></a>Compilerfehler C2198
"Funktion": Nicht genügend Argumente für Aufruf.  
  
 Der Compiler hat nicht genügend Parameter für einen Aufruf der Funktion oder eine falsche Funktionsdeklaration gefunden.  
  
 Im folgenden Beispiel wird C2198 generiert:  
  
```  
// C2198.c  
// compile with: /c  
void func( int, int );  
int main() {  
   func( 1 );   // C2198 only one actual parameter  
   func( 1, 1 );   // OK  
}  
```
