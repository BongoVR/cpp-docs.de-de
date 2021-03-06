---
title: Compilerfehler Fehler C2712 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2712
dev_langs:
- C++
helpviewer_keywords:
- C2712
ms.assetid: f7d4ffcc-7ed2-459b-8067-a728ce647071
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c26c5d7a24c022cacf4c20687b2d8c58f7e9e342
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2712"></a>Compilerfehler Fehler C2712
__try kann nicht in Funktionen verwendet werden, die eine Objektentladung benötigen  
  
 Fehler C2712 kann auftreten, wenn Sie [/EHsc /](../../build/reference/eh-exception-handling-model.md), und eine Funktion mit strukturierter Ausnahmebehandlung auch Objekte besitzt, die Entladung (Zerstörung) benötigen.  
  
 Folgende Lösungen sind möglich:  
  
-   Verschieben Sie Code, der SEH benötigt, zu einer anderen Funktion.  
  
-   Schreiben Sie Funktionen, die SEH verwenden, neu, um die Verwendung von lokalen Variablen und Parameter, die über Destruktoren verfügen, zu vermeiden. Verwenden Sie SEH nicht in Konstruktoren oder Destruktoren  
  
-   Kompilieren ohne /EHsc  
  
 Fehler C2712 kann auch auftreten, wenn Sie eine Methode deklariert, indem Aufrufen der [__event](../../cpp/event.md) Schlüsselwort. Da das Ereignis möglicherweise in einer Multithreadumgebung verwendet werden, generiert der Compiler Code, der Bearbeitung des zugrunde liegenden Ereignisobjekts verhindert, und schließt den generierten Code dann in eine SEH- [Try-finally-Anweisung](../../cpp/try-finally-statement.md). Folglich wird Fehler C2712 auftreten, wenn Sie die Ereignismethode aufrufen und ein Argument, dessen Typ einen Destruktor enthält, als Wert übergeben. Eine Lösung besteht in diesem Fall darin, das Argument als konstanten Verweis zu übergeben.  
  
## <a name="example"></a>Beispiel  
 C2712 kann auch auftreten, wenn beim Kompilieren mit **/CLR: pure** , und deklarieren Sie einen statischen Array von Zeigern auf Funktionen in einer `__try` Block. Ein statischer Member benötigt den Compiler an, verwenden Sie die dynamische Initialisierung unter **/CLR: pure**, wodurch eine C++-Ausnahmebehandlung impliziert. Eine C++-Ausnahmebehandlung ist jedoch in einem `__try`-Block nicht zulässig.  
  
 Die Compileroptionen **/clr:pure** und **/clr:safe** sind in Visual Studio 2015 veraltet.  
  
 Im folgenden Beispiel wird C2712 generiert und gezeigt, wie Sie diesen Fehler beheben:  
  
```  
// C2712.cpp  
// compile with: /clr:pure /c  
struct S1 {  
   static int smf();  
   void fnc();  
};  
  
void S1::fnc() {  
   __try {  
      static int (*array_1[])() = {smf,};   // C2712  
  
      // OK  
      static int (*array_2[2])();  
      array_2[0] = smf;  
    }  
    __except(0) {}  
}  
```