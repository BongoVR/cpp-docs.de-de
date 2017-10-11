---
title: Compilerfehler C3704 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3704
dev_langs:
- C++
helpviewer_keywords:
- C3704
ms.assetid: ee40ea35-a214-4dec-9489-d7f155dd0ac2
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: ae48bc886aab0211063cc7a9c2e73f3c7bbdd368
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3704"></a>Compilerfehler C3704
'Funktion': eine Vararg-Methode kann keine Ereignisse auslösen  
  
 Sie haben versucht, [__event](../../cpp/event.md) für eine Vararg-Methode. Um diesen Fehler zu beheben, ersetzen die `fireEvent(int i, ...)` rufen Sie mit der `fireEvent(int i)` aufrufen, wie im folgenden Codebeispiel gezeigt.  
  
 Im folgende Beispiel wird C3704 generiert:  
  
```  
// C3704.cpp  
[ event_source(native) ]  
class CEventSrc {  
   public:  
      __event void fireEvent(int i, ...);   // C3704  
      // try the following line instead:  
      // __event void fireEvent(int i);  
};  
  
int main() {  
}  
```
