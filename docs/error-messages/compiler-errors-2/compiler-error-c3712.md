---
title: Compilerfehler C3712 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3712
dev_langs:
- C++
helpviewer_keywords:
- C3712
ms.assetid: 65b1fcaf-be89-4c55-9e40-25ec03457253
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: df27d74f276f70cb93a7e862e452b3a6d0eb4e55
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3712"></a>Compilerfehler C3712
'Methode': eine Ereignishandlermethode muss denselben Typ wie die Quelle 'Methode' zurückgeben  
  
 Sie definiert eine Ereignishandlermethode, die nicht den gleichen Typ wie die Quelle Ereignis-Methode zurückgegeben wurde. Um diesen Fehler zu beheben, geben Sie der Ereignishandlermethode denselben Rückgabetyp als die Quelle Ereignis-Methode.  
  
 Im folgende Beispiel wird C3712 generiert:  
  
```  
// C3712.cpp  
// compile with: /c  
[event_source(native)]  
class CEventSrc {  
public:  
   __event void event1();  
};  
  
[event_receiver(native)]  
class CEventRec {  
public:  
   int handler1() { return 0; }  
   // try the following line instead  
   // void handler1() {}  
  
   void HookEvents(CEventSrc* pSrc) {  
      __hook(&CEventSrc::event1, pSrc, &CEventRec::handler1);   // C3712  
   }  
   void UnhookEvents(CEventSrc* pSrc) {  
      __unhook(&CEventSrc::event1, pSrc, &CEventRec::handler1);   // C3712  
   }  
};  
```