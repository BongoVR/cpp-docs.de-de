---
title: verwaltete, unverwaltete | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- vc-pragma.unmanaged
- managed_CPP
- unmanaged_CPP
- vc-pragma.managed
dev_langs:
- C++
helpviewer_keywords:
- managed pragma
- pragmas, unmanaged
- pragmas, managed
- unmanaged pragma
ms.assetid: f072ddcc-e1ec-408a-8ce1-326ddb60e4a4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 316866ac047b607ec4c92d7c6d4f8ff233ed9a3f
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="managed-unmanaged"></a>managed, unmanaged
Aktivieren Sie die Steuerung auf Funktionsebene für Kompilierfunktionen als verwaltet oder nicht verwaltet.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      #pragma managed  
#pragma unmanaged  
#pragma managed([push,] on | off)  
#pragma managed(pop)  
```  
  
## <a name="remarks"></a>Hinweise  
 Die ["/ CLR"](../build/reference/clr-common-language-runtime-compilation.md) Compileroption bietet Steuerung auf Modulebene für kompilierfunktionen als verwaltet oder nicht verwaltet.  
  
 Eine nicht verwaltete Funktion wird für die systemeigene Plattform kompiliert, und die Ausführung dieses Teils des Programms wird von der Common Language Runtime an die systemeigene Plattform übergeben.  
  
 Funktionen werden standardmäßig als verwaltet kompiliert beim **"/ CLR"** verwendet wird.  
  
 Beim Anwenden dieser Pragmas:  
  
-   Fügen Sie das Pragma hinzu, das einer Funktion vorangeht, sich jedoch nicht innerhalb eines Funktionsrumpfs befindet.  
  
-   Fügen Sie das Pragma nach `#include`-Anweisungen hinzu. Verwenden Sie diese Pragmas nicht vor `#include`-Anweisungen.  
  
 Der Compiler ignoriert die `managed` und `unmanaged` Pragmas Wenn **"/ CLR"** nicht in der Kompilierung verwendet wird.  
  
 Wenn eine Vorlagenfunktion instanziiert wird, bestimmt der Pragmazustand zum Zeitpunkt der Definition, ob die Vorlage verwaltet oder nicht verwaltet ist.  
  
 Weitere Informationen finden Sie unter [Initialisierung gemischter Assemblys](../dotnet/initialization-of-mixed-assemblies.md).  
  
## <a name="example"></a>Beispiel  
  
```cpp  
// pragma_directives_managed_unmanaged.cpp  
// compile with: /clr  
#include <stdio.h>  
  
// func1 is managed  
void func1() {  
   System::Console::WriteLine("In managed function.");  
}  
  
// #pragma unmanaged  
// push managed state on to stack and set unmanaged state  
#pragma managed(push, off)  
  
// func2 is unmanaged  
void func2() {  
   printf("In unmanaged function.\n");  
}  
  
// #pragma managed  
#pragma managed(pop)  
  
// main is managed  
int main() {  
   func1();  
   func2();  
}  
```  
  
```Output  
In managed function.  
In unmanaged function.  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Pragma-Direktiven und das __Pragma-Schlüsselwort](../preprocessor/pragma-directives-and-the-pragma-keyword.md)