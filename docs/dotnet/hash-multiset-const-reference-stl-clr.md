---
title: 'hash_multiset:: const_reference (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::hash_multiset::const_reference
dev_langs:
- C++
helpviewer_keywords:
- const_reference member [STL/CLR]
ms.assetid: 86d01c6b-0540-4ff9-bee6-cdf37bfc693e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 0910b3409cd6469340ef237597ce3d67302183ae
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="hashmultisetconstreference-stlclr"></a>hash_multiset::const_reference (STL/CLR)
Der Typ eines konstanten Verweises auf ein Element.  
  
## <a name="syntax"></a>Syntax  
  
```  
typedef value_type% const_reference;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Typ beschreibt einen konstanten Verweis auf ein Element.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_hash_multiset_const_reference.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_multiset<wchar_t> Myhash_multiset;   
int main()   
    {   
    Myhash_multiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    Myhash_multiset::const_iterator cit = c1.begin();   
    for (; cit != c1.end(); ++cit)   
        {   // get a const reference to an element   
        Myhash_multiset::const_reference cref = *cit;   
        System::Console::Write(" {0}", cref);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext Hash_set/>  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [hash_multiset-Element (STL/CLR)](../dotnet/hash-multiset-stl-clr.md)   
 [hash_multiset:: Reference (STL/CLR)](../dotnet/hash-multiset-reference-stl-clr.md)   
 [hash_multiset::value_type (STL/CLR)](../dotnet/hash-multiset-value-type-stl-clr.md)