---
title: 'hash_map:: mapped_type (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::hash_map::mapped_type
dev_langs:
- C++
helpviewer_keywords:
- mapped_type member [STL/CLR]
ms.assetid: 00c8738f-7dd9-418d-9566-a2e05fd7e7f6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 96fe75ad5e3b3f45bbea40d4f3bdcf9175795f70
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="hashmapmappedtype-stlclr"></a>hash_map::mapped_type (STL/CLR)
Der Typ eines zugeordneten Werts, der jedem Schlüssel zugeordnet ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
typedef Mapped mapped_type;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Type stellt ein Synonym für den Vorlagenparameter `Mapped` dar.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_hash_map_mapped_type.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
int main()   
    {   
    Myhash_map c1;   
    c1.insert(Myhash_map::make_value(L'a', 1));   
    c1.insert(Myhash_map::make_value(L'b', 2));   
    c1.insert(Myhash_map::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]" using mapped_type   
    for (Myhash_map::iterator it = c1.begin(); it != c1.end(); ++it)   
        {   // store element in mapped_type object   
        Myhash_map::mapped_type val = it->second;   
  
        System::Console::Write(" {0}", val);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
1 2 3  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext Hash_map/>  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [hash_map-Element (STL/CLR)](../dotnet/hash-map-stl-clr.md)   
 [hash_map:: key_compare (STL/CLR)](../dotnet/hash-map-key-compare-stl-clr.md)   
 [hash_map::value_type (STL/CLR)](../dotnet/hash-map-value-type-stl-clr.md)