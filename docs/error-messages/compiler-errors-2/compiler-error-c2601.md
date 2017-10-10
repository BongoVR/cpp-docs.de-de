---
title: Compilerfehler Fehler C2601 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2601
dev_langs:
- C++
helpviewer_keywords:
- C2601
ms.assetid: 88275582-5f37-45d7-807d-05f06ba00965
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: cdffa40b751232525920d1d92affd9e3778d2f61
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2601"></a>Compilerfehler Fehler C2601
"Function": Lokale Funktionsdefinitionen sind nicht zulässig  
  
 Code versucht, eine Funktion innerhalb einer Funktion definieren.  
  
 Oder es gibt möglicherweise eine zusätzliche geschweifte Klammer in Ihrem Quellcode vor dem Auftreten des Fehlers C2601.  
  
 Im folgenden Beispiel wird C2601 generiert:  
  
```  
// C2601.cpp  
int main() {  
   int i = 0;  
  
   void funcname(int j) {   // C2601  
      j++;  
   }  
}  
```
