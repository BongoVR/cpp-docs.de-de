---
title: 'multiset:: Empty (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::multiset::empty
dev_langs:
- C++
helpviewer_keywords:
- empty member [STL/CLR]
ms.assetid: 59ec9cc4-cc72-4082-9ab2-49b49980e681
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 0f0925ba5c96f2f694123a846abbd816d807ce80
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="multisetempty-stlclr"></a>multiset::empty (STL/CLR)
Testet, ob keine Elemente vorhanden sind.  
  
## <a name="syntax"></a>Syntax  
  
```  
bool empty();  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion gibt „true“ für eine leere gesteuerte Sequenz zurück. Dies ist äquivalent zum [multiset:: Size (STL/CLR)](../dotnet/multiset-size-stl-clr.md)`() == 0`. Sie verwenden sie zum Überprüfen, ob die Multimenge leer ist.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_multiset_empty.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::multiset<wchar_t> Mymultiset;   
int main()   
    {   
    Mymultiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    System::Console::WriteLine("empty() = {0}", c1.empty());   
  
// clear the container and reinspect   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    System::Console::WriteLine("empty() = {0}", c1.empty());   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
size() = 3  
empty() = False  
size() = 0  
empty() = True  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Set >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Multiset (STL/CLR)](../dotnet/multiset-stl-clr.md)   
 [multiset::size (STL/CLR)](../dotnet/multiset-size-stl-clr.md)