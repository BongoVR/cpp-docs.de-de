---
title: hash_multiset::Rehash (STL/CLR) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::hash_multiset::rehash
dev_langs:
- C++
helpviewer_keywords:
- rehash member [STL/CLR]
ms.assetid: 1208cffc-acee-4c75-87b5-ce9ec641c3b6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 8707be6f21cb0c4bd6c82d7e41be3cef0141ce6d
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="hashmultisetrehash-stlclr"></a>hash_multiset::rehash (STL/CLR)
Erstellt die Hashtabelle neu.  
  
## <a name="syntax"></a>Syntax  
  
```  
void rehash();  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion erstellt die Hashtabelle, die sicherstellen, dass neu [hash_multiset::load_factor (STL/CLR)](../dotnet/hash-multiset-load-factor-stl-clr.md) `() <=` [hash_multiset::max_load_factor (STL/CLR)](../dotnet/hash-multiset-max-load-factor-stl-clr.md). Andernfalls wird die Hashtabelle vergrößert nur bei Bedarf nach einer Einfügung. (Es nimmt nie automatisch in der Größe.) Sie können damit passen Sie die Größe der Hashtabelle.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_hash_multiset_rehash.cpp   
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
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect current parameters   
    System::Console::WriteLine("bucket_count() = {0}", c1.bucket_count());   
    System::Console::WriteLine("load_factor() = {0}", c1.load_factor());   
    System::Console::WriteLine("max_load_factor() = {0}",   
        c1.max_load_factor());   
    System::Console::WriteLine();   
  
// change max_load_factor and redisplay   
    c1.max_load_factor(0.25f);   
    System::Console::WriteLine("bucket_count() = {0}", c1.bucket_count());   
    System::Console::WriteLine("load_factor() = {0}", c1.load_factor());   
    System::Console::WriteLine("max_load_factor() = {0}",   
        c1.max_load_factor());   
    System::Console::WriteLine();   
  
// rehash and redisplay   
    c1.rehash(100);   
    System::Console::WriteLine("bucket_count() = {0}", c1.bucket_count());   
    System::Console::WriteLine("load_factor() = {0}", c1.load_factor());   
    System::Console::WriteLine("max_load_factor() = {0}",   
        c1.max_load_factor());   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
bucket_count() = 16  
load_factor() = 0.1875  
max_load_factor() = 4  
  
bucket_count() = 16  
load_factor() = 0.1875  
max_load_factor() = 0.25  
  
bucket_count() = 128  
load_factor() = 0.0234375  
max_load_factor() = 0.25  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext Hash_set/>  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [hash_multiset-Element (STL/CLR)](../dotnet/hash-multiset-stl-clr.md)   
 [hash_multiset::bucket_count (STL/CLR)](../dotnet/hash-multiset-bucket-count-stl-clr.md)   
 [hash_multiset::load_factor (STL/CLR)](../dotnet/hash-multiset-load-factor-stl-clr.md)   
 [hash_multiset::max_load_factor (STL/CLR)](../dotnet/hash-multiset-max-load-factor-stl-clr.md)