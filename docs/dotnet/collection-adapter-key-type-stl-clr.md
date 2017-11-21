---
title: collection_adapter::KEY_TYPE (STL/CLR) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::collection_adapter::key_type
dev_langs: C++
helpviewer_keywords: key_type member [STL/CLR]
ms.assetid: 71ed32b0-af5b-4bac-ae09-2f5d08f0a79b
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 815e52fc75212128aa48293aef8630456a47f919
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="collectionadapterkeytype-stlclr"></a>collection_adapter::key_type (STL/CLR)
Der Typ eines Schlüssels Wörterbuch.  
  
## <a name="syntax"></a>Syntax  
  
```  
typedef Key key_type;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für den Vorlagenparameter `Key`, in der eine Spezialisierung für `IDictionary` oder `IDictionary<Value>`; andernfalls ist es nicht definiert.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_collection_adapter_key_type.cpp   
// compile with: /clr   
#include <cliext/adapter>   
#include <cliext/map>   
  
typedef cliext::map<wchar_t, int> Mymap;   
typedef cliext::collection_adapter<   
    System::Collections::Generic::IDictionary<wchar_t, int>> Mycoll;   
typedef System::Collections::Generic::KeyValuePair<wchar_t,int> Mypair;   
int main()   
    {   
    Mymap d1;   
    d1.insert(Mymap::make_value(L'a', 1));   
    d1.insert(Mymap::make_value(L'b', 2));   
    d1.insert(Mymap::make_value(L'c', 3));   
    Mycoll c1(%d1);   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mypair elem in c1)   
        {   
        Mycoll::key_type key = elem.Key;   
        Mycoll::mapped_type value = elem.Value;   
        System::Console::Write(" [{0} {1}]", key, value);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
[a 1] [b 2] [c 3]  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext-Adapter >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Collection_adapter (STL/CLR)](../dotnet/collection-adapter-stl-clr.md)   
 [collection_adapter::mapped_type (STL/CLR)](../dotnet/collection-adapter-mapped-type-stl-clr.md)