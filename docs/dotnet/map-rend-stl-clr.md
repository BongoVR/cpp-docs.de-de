---
title: 'Map:: rend (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::map::rend
dev_langs:
- C++
helpviewer_keywords:
- rend member [STL/CLR]
ms.assetid: 132d9a82-f76a-4f3e-8d21-26de17e1245f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 6793d9fe5988a05856920790cbec4b702c456039
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="maprend-stlclr"></a>map::rend (STL/CLR)
Legt das Ende der umgekehrten kontrollierten Sequenz fest.  
  
## <a name="syntax"></a>Syntax  
  
```  
reverse_iterator rend();  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion gibt einem reverse-Iterator, verweist direkt hinter dem Anfang der kontrollierten Sequenz zurück. Daher kennzeichnet es die `end` der umgekehrten Sequenz. Es mit der einen Iterator abrufen, bestimmt die `current` Ende der kontrollierten Sequenz in umgekehrter Reihenfolge, aber dessen Status kann ändern, wenn die Länge der gesteuerten Sequenz geändert wird.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_map_rend.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::map<wchar_t, int> Mymap;   
int main()   
    {   
    Mymap c1;   
    c1.insert(Mymap::make_value(L'a', 1));   
    c1.insert(Mymap::make_value(L'b', 2));   
    c1.insert(Mymap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// inspect first two items in reversed sequence   
    Mymap::reverse_iterator rit = c1.rend();   
    --rit;   
    --rit;   
    System::Console::WriteLine("*-- --rend() = [{0} {1}]",   
        rit->first, rit->second);   
    ++rit;   
    System::Console::WriteLine("*--rend() = [{0} {1}]",   
        rit->first, rit->second);   
    return (0);   
    }  
  
```  
  
```Output  
 [a 1] [b 2] [c 3]  
*-- --rend() = [b 2]  
*--rend() = [a 1]  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Map >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Karte (STL/CLR)](../dotnet/map-stl-clr.md)   
 [Map:: begin (STL/CLR)](../dotnet/map-begin-stl-clr.md)   
 [Map:: End (STL/CLR)](../dotnet/map-end-stl-clr.md)   
 [map::rbegin (STL/CLR)](../dotnet/map-rbegin-stl-clr.md)