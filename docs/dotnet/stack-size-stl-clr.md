---
title: 'Stack:: Size (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::stack::size
dev_langs:
- C++
helpviewer_keywords:
- size member [STL/CLR]
ms.assetid: 6113e649-a4f9-4021-8131-34cee4bc8ca0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 06cf49539470f5cebfad22405ccd75b6504bcbff
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="stacksize-stlclr"></a>stack::size (STL/CLR)
Ermittelt die Anzahl von Elementen.  
  
## <a name="syntax"></a>Syntax  
  
```  
size_type size();  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion gibt die Länge der gesteuerten Sequenz zurück. Sie können erkennen, die Anzahl der Elemente, die derzeit in der kontrollierten Sequenz. Wenn Sie von Interesse ist, ob die Sequenz ungleich Größe finden Sie unter hat, [Stack:: Empty (STL/CLR)](../dotnet/stack-empty-stl-clr.md)`()`.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_stack_size.cpp   
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
    System::Console::WriteLine("size() = {0} starting with 3", c1.size());   
  
// pop an item and reinspect   
    c1.pop();   
    System::Console::WriteLine("size() = {0} after popping", c1.size());   
  
// add two elements and reinspect   
    c1.push(L'a');   
    c1.push(L'b');   
    System::Console::WriteLine("size() = {0} after adding 2", c1.size());   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
size() = 3 starting with 3  
size() = 2 after popping  
size() = 4 after adding 2  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Stack >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Stack (STL/CLR)](../dotnet/stack-stl-clr.md)   
 [stack::empty (STL/CLR)](../dotnet/stack-empty-stl-clr.md)