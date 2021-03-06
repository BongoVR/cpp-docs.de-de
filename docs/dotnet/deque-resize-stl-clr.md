---
title: 'deque:: Resize (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::deque::resize
dev_langs:
- C++
helpviewer_keywords:
- resize member [STL/CLR]
ms.assetid: c83f3c57-38b3-4706-a124-59bafbf88484
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 0d7e68fa1a58e70d4b414f81ca826e632c8706bd
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="dequeresize-stlclr"></a>deque::resize (STL/CLR)
Ändert die Anzahl der Elemente an.  
  
## <a name="syntax"></a>Syntax  
  
```  
void resize(size_type new_size);  
void resize(size_type new_size, value_type val);  
```  
  
#### <a name="parameters"></a>Parameter  
 new_size  
 Neue Größe der gesteuerten Sequenz.  
  
 Val  
 Der Wert des Elements Auffüllung.  
  
## <a name="remarks"></a>Hinweise  
 Die beiden Memberfunktionen sicher, dass [deque:: Size (STL/CLR)](../dotnet/deque-size-stl-clr.md) `()` künftig gibt `new_size`. Wenn die gesteuerte Sequenz verlängert werden muss, fügt die erste Memberfunktion Elemente mit dem Wert `value_type()` an, während die zweite Memberfunktion Elemente mit dem Wert `val` anfügt. Um die gesteuerte Sequenz kürzere zu machen, beide Memberfunktionen effektiv das letzte Element löschen [deque:: Size (STL/CLR)](../dotnet/deque-size-stl-clr.md) `() -` `new_size` Zeiten. Sie können damit stellen Sie sicher, dass die kontrollierte Sequenz Größe hat `new_size`, indem Sie verkürzen oder Auffüllen von der aktuellen gesteuerten Sequenz.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_deque_resize.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
// construct an empty container and pad with default values   
    cliext::deque<wchar_t> c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
    c1.resize(4);   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", (int)elem);   
    System::Console::WriteLine();   
  
// resize to empty   
    c1.resize(0);   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
// resize and pad   
    c1.resize(5, L'x');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
size() = 0  
 0 0 0 0  
size() = 0  
 x x x x x  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/doppelschlange >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Deque (STL/CLR)](../dotnet/deque-stl-clr.md)   
 [deque:: Clear (STL/CLR)](../dotnet/deque-clear-stl-clr.md)   
 [deque:: Erase (STL/CLR)](../dotnet/deque-erase-stl-clr.md)   
 [deque::insert (STL/CLR)](../dotnet/deque-insert-stl-clr.md)