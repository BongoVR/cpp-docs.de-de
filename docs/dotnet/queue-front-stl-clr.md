---
title: 'Queue:: Front (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::queue::front
dev_langs:
- C++
helpviewer_keywords:
- front member [STL/CLR]
ms.assetid: 9d7bb95f-5896-42f7-86fa-004a7a65cc94
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: a549af95cd13588359064fd571b5726a7490b8d9
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="queuefront-stlclr"></a>queue::front (STL/CLR)
Greift auf das erste Element zu.  
  
## <a name="syntax"></a>Syntax  
  
```  
reference front();  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion gibt einen Verweis auf das erste Element der gesteuerten Sequenz, die nicht leer sein darf. Sie verwenden es das erste Element auf, wenn Sie wissen, dass es vorhanden ist.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_queue_front.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::queue<wchar_t> Myqueue;   
int main()   
    {   
    Myqueue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect first item   
    System::Console::WriteLine("front() = {0}", c1.front());   
  
// alter first item and reinspect   
    c1.front() = L'x';   
    for each (wchar_t elem in c1.get_container())   
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
 **Header:** \<Cliext bzw. einer neuen Warteschlange >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Warteschlange (STL/CLR)](../dotnet/queue-stl-clr.md)   
 [Queue:: Back (STL/CLR)](../dotnet/queue-back-stl-clr.md)   
 [Queue::back_item (STL/CLR)](../dotnet/queue-back-item-stl-clr.md)   
 [queue::front_item (STL/CLR)](../dotnet/queue-front-item-stl-clr.md)