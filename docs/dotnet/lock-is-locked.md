---
title: Lock::is_locked | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- is_locked
- msclr::lock::is_locked
- lock::is_locked
- msclr::lock.is_locked
- lock.is_locked
dev_langs:
- C++
helpviewer_keywords:
- lock::is_locked
ms.assetid: d888827c-8052-47c6-87a2-8c42f60a688d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: de4f7a3c92ccace542a4588b0278fd4f799459c2
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="lockislocked"></a>lock::is_locked
Gibt an, ob eine Sperre gehalten wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
bool is_locked();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 `true` Wenn eine Sperre aufrechterhalten wird, `false` andernfalls.  
  
## <a name="example"></a>Beispiel  
 Dieses Beispiel verwendet eine einzelne Instanz einer Klasse über mehrere Threads hinweg.  Die Klasse verwendet eine Sperre auf sich selbst, um sicherzustellen, dass der Zugriff auf die internen Daten für jeden Thread konsistent sind.  Thread der hauptanwendung verwendet eine Sperre für dieselbe Instanz der Klasse in regelmäßigen Abständen überprüfen, um festzustellen, ob alle Arbeitsthreads noch vorhanden sind, und wartet, bis alle Arbeitsthreads aktiviert beenden ihre Aufgaben abgeschlossen haben.  
  
```  
// msl_lock_is_locked.cpp  
// compile with: /clr  
#include <msclr/lock.h>  
  
using namespace System;  
using namespace System::Threading;  
using namespace msclr;  
  
ref class CounterClass {  
private:  
   int Counter;     
  
public:  
   property int ThreadCount;  
  
   // function called by multiple threads, use lock to keep Counter consistent  
   // for each thread  
   void UseCounter() {  
      try {  
         lock l(this); // wait infinitely  
  
         Console::WriteLine("In thread {0}, Counter = {1}", Thread::CurrentThread->ManagedThreadId,   
            Counter);  
  
         for (int i = 0; i < 10; i++) {  
            Counter++;  
            Thread::Sleep(10);  
         }  
  
         Console::WriteLine("In thread {0}, Counter = {1}", Thread::CurrentThread->ManagedThreadId,   
            Counter);  
  
         Counter = 0;  
         // lock is automatically released when it goes out of scope and its destructor is called  
      }  
      catch (...) {  
         Console::WriteLine("Couldn't acquire lock!");  
      }  
  
      ThreadCount--;  
   }  
};  
  
int main() {  
   // create a few threads to contend for access to the shared data  
   CounterClass^ cc = gcnew CounterClass;  
   array<Thread^>^ tarr = gcnew array<Thread^>(5);  
   ThreadStart^ startDelegate = gcnew ThreadStart(cc, &CounterClass::UseCounter);  
   for (int i = 0; i < tarr->Length; i++) {  
      tarr[i] = gcnew Thread(startDelegate);  
      cc->ThreadCount++;  
      tarr[i]->Start();  
   }  
  
   // keep our main thread alive until all worker threads have completed  
   lock l(cc, lock_later); // don't lock now, just create the object  
   while (true) {  
      l.try_acquire(50); // try to acquire lock, don't throw an exception if can't  
      if (l.is_locked()) { // check if we got the lock  
         if (0 == cc->ThreadCount) {  
            Console::WriteLine("All threads completed.");  
            break; // all threads are gone, exit while  
         }  
         else {  
            Console::WriteLine("{0} threads exist, continue waiting...", cc->ThreadCount);  
            l.release(); // some threads exist, let them do their work  
         }  
      }  
   }  
}  
```  
  
```Output  
In thread 3, Counter = 0  
In thread 3, Counter = 10  
In thread 5, Counter = 0  
In thread 5, Counter = 10  
In thread 4, Counter = 0  
In thread 4, Counter = 10  
In thread 7, Counter = 0  
In thread 7, Counter = 10  
In thread 6, Counter = 0  
In thread 6, Counter = 10  
All threads completed.  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Headerdatei** \<msclr\lock.h >  
  
 **Namespace** Msclr  
  
## <a name="see-also"></a>Siehe auch  
 [Lock-Member](../dotnet/lock-members.md)   
 [lock::operator bool](../dotnet/lock-operator-bool.md)