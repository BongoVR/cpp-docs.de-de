---
title: 'multiset:: KEY_TYPE (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::multiset::key_type
dev_langs:
- C++
helpviewer_keywords:
- key_type member [STL/CLR]
ms.assetid: 8b243eb3-889b-405c-a2bd-2c2c5dfaafcd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 89ba7f04e0bd8101a21f13cf921c5823c246bd1f
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="multisetkeytype-stlclr"></a>multiset::key_type (STL/CLR)
Der Typ eines Sortierschlüssels.  
  
## <a name="syntax"></a>Syntax  
  
```  
typedef Key key_type;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Type stellt ein Synonym für den Vorlagenparameter `Key` dar.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_multiset_key_type.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::multiset<wchar_t> Mymultiset;   
int main()   
    {   
    Mymultiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display contents " a b c" using key_type   
    for (Mymultiset::iterator it = c1.begin(); it != c1.end(); ++it)   
        {   // store element in key_type object   
        Mymultiset::key_type val = *it;   
  
        System::Console::Write(" {0}", val);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Set >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Multiset (STL/CLR)](../dotnet/multiset-stl-clr.md)   
 [multiset:: key_compare (STL/CLR)](../dotnet/multiset-key-compare-stl-clr.md)   
 [multiset::value_type (STL/CLR)](../dotnet/multiset-value-type-stl-clr.md)