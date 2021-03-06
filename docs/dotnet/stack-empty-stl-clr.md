---
title: 'Stack:: Empty (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::stack::empty
dev_langs:
- C++
helpviewer_keywords:
- empty member [STL/CLR]
ms.assetid: 30bb4ec6-e7a1-4137-99ba-0e0ebdf31baf
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: e6af0d89dead2a79a853a51943ffdf2778ee9c7d
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="stackempty-stlclr"></a>stack::empty (STL/CLR)
Testet, ob keine Elemente vorhanden sind.  
  
## <a name="syntax"></a>Syntax  
  
```  
bool empty();  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion gibt „true“ für eine leere gesteuerte Sequenz zurück. Dies ist äquivalent zum [Stack:: Size (STL/CLR)](../dotnet/stack-size-stl-clr.md)`() == 0`. Sie verwenden sie zum Überprüfen, ob der Stapel leer ist.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_stack_empty.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    System::Console::WriteLine("empty() = {0}", c1.empty());   
  
// clear the container and reinspect   
    c1.pop();   
    c1.pop();   
    c1.pop();   
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
 **Header:** \<Cliext/Stack >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Stack (STL/CLR)](../dotnet/stack-stl-clr.md)   
 [stack::size (STL/CLR)](../dotnet/stack-size-stl-clr.md)