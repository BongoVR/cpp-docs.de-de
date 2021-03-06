---
title: __ptr32, __ptr64 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- __ptr32_cpp
- __ptr64_cpp
dev_langs:
- C++
helpviewer_keywords:
- __ptr64 keyword [C++]
- _ptr32 keyword [C++]
- ptr32 keyword [C++]
- ptr64 keyword [C++]
- _ptr64 keyword [C++]
- __ptr32 keyword [C++]
ms.assetid: afb563d8-7458-4fe7-9c30-bd4b5385a59f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 53fafb1e7be45cd4b48ce51e787b6338dd0f7324
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="ptr32-ptr64"></a>__ptr32, __ptr64
## <a name="microsoft-specific"></a>Microsoft-spezifisch  
 `__ptr32` stellt einen systemeigenen Zeiger auf einem 32-Bit-System dar, während `__ptr64` einen systemeigenen Zeiger auf einem 64-Bit-System darstellt.  
  
 Das folgende Beispiel zeigt, wie die einzelnen Zeigertypen deklariert werden:  
  
```  
int * __ptr32 p32;  
int * __ptr64 p64;  
```  
  
 Bei einem 32-Bit-System wird ein Zeiger, der mit `__ptr64` deklariert wird, auf einen 32-Bit-Zeiger gekürzt. Bei einem 64-Bit-System wird ein Zeiger, der mit `__ptr32` deklariert wird, in einen 64-Bit-Zeiger umgewandelt.  
  
> [!NOTE]
>  Sie können keine `__ptr32` oder `__ptr64` beim Kompilieren mit **/CLR: pure**. Andernfalls wird `Compiler Error C2472` generiert. Die Compileroptionen **/clr:pure** und **/clr:safe** sind in Visual Studio 2015 veraltet.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt, wie Zeiger mit den Schlüsselwörtern `__ptr32` und `__ptr64` deklariert und zugewiesen werden.  
  
```  
#include <cstdlib>  
#include <iostream>  
  
int main()  
{  
    using namespace std;  
  
    int * __ptr32 p32;  
    int * __ptr64 p64;  
  
    p32 = (int * __ptr32)malloc(4);  
    *p32 = 32;  
    cout << *p32 << endl;  
  
    p64 = (int * __ptr64)malloc(4);  
    *p64 = 64;  
    cout << *p64 << endl;  
}  
```  
  
```Output  
32  
64  
```  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Grundlegende Typen](../cpp/fundamental-types-cpp.md)