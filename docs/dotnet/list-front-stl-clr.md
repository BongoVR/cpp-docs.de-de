---
title: 'List:: Front (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::list::front
dev_langs:
- C++
helpviewer_keywords:
- front member [STL/CLR]
ms.assetid: ead6aaaa-b518-4a9c-af80-7189bf872cad
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: f66d8ddca0efd9e54e1b71a5ffb696fb409c8c67
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="listfront-stlclr"></a>list::front (STL/CLR)
Greift auf das erste Element zu.  
  
## <a name="syntax"></a>Syntax  
  
```  
reference front();  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion gibt einen Verweis auf das erste Element der gesteuerten Sequenz, die nicht leer sein darf. Sie verwenden ihn zum Lesen oder schreiben das erste Element, wenn Sie wissen, dass es vorhanden ist.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_list_front.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect first item   
    System::Console::WriteLine("front() = {0}", c1.front());   
  
// alter first item and reinspect   
    c1.front() = L'x';   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
front() = a  
 x b c  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/List >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Liste (STL/CLR)](../dotnet/list-stl-clr.md)   
 [List:: Back (STL/CLR)](../dotnet/list-back-stl-clr.md)   
 [List:: back_item (STL/CLR)](../dotnet/list-back-item-stl-clr.md)   
 [list::front_item (STL/CLR)](../dotnet/list-front-item-stl-clr.md)