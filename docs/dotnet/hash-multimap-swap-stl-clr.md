---
title: 'hash_multimap:: Swap (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::hash_multimap::swap
dev_langs:
- C++
helpviewer_keywords:
- swap member [STL/CLR]
ms.assetid: 4baa60c2-865a-4e17-acd5-01b7c3c5cd44
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 1368af9af40c6fc76c7cdcd5be10835d0fd6f1e5
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="hashmultimapswap-stlclr"></a>hash_multimap::swap (STL/CLR)
Vertauscht den Inhalt von zwei Containern.  
  
## <a name="syntax"></a>Syntax  
  
```  
void swap(hash_multimap<Key, Mapped>% right);  
```  
  
#### <a name="parameters"></a>Parameter  
 Rechts  
 Container für den Tausch von Inhalten.  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion tauscht die kontrollierten Sequenzen zwischen `this` und `right`aus. Dies erfolgt in konstanter Zeit, und es löst keine Ausnahmen. Sie verwenden es als eine schnelle Möglichkeit zum Austauschen von den Inhalt von zwei Containern.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_hash_multimap_swap.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
    c1.insert(Myhash_multimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct another container with repetition of values   
    Myhash_multimap c2;   
    c2.insert(Myhash_multimap::make_value(L'd', 4));   
    c2.insert(Myhash_multimap::make_value(L'e', 5));   
    c2.insert(Myhash_multimap::make_value(L'f', 6));   
    for each (Myhash_multimap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// swap and redisplay   
    c1.swap(c2);   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
    for each (Myhash_multimap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
[a 1] [b 2] [c 3]  
[d 4] [e 5] [f 6]  
[d 4] [e 5] [f 6]  
[a 1] [b 2] [c 3]  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext Hash_map/>  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [hash_multimap-Element (STL/CLR)](../dotnet/hash-multimap-stl-clr.md)   
 [hash_multimap::operator= (STL/CLR)](../dotnet/hash-multimap-operator-assign-stl-clr.md)