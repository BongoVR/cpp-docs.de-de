---
title: hash_set::Hasher (STL/CLR) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::hash_set::hasher
dev_langs:
- C++
helpviewer_keywords:
- hasher member [STL/CLR]
ms.assetid: 0fafd645-0bdf-4d4c-8630-c536fbc4bd2c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: e8f51d37f8b35f1ff10a11f7afa4038bfe2bd8e4
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="hashsethasher-stlclr"></a>hash_set::hasher (STL/CLR)
Der Hashalgorithmus Delegat für einen Schlüssel.  
  
## <a name="syntax"></a>Syntax  
  
```  
Microsoft::VisualC::StlClr::UnaryDelegate<GKey, int>  
    hasher;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Typ beschreibt ein Delegat, der einen Schlüssel-Wert in eine ganze Zahl konvertiert.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_hash_set_hasher.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
    Myhash_set c1;   
    Myhash_set::hasher^ myhash = c1.hash_delegate();   
  
    System::Console::WriteLine("hash(L'a') = {0}", myhash(L'a'));   
    System::Console::WriteLine("hash(L'b') = {0}", myhash(L'b'));   
    return (0);   
    }  
  
```  
  
```Output  
hash(L'a') = 1616896120  
hash(L'b') = 570892832  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext Hash_set/>  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Hash_set (STL/CLR)](../dotnet/hash-set-stl-clr.md)   
 [hash_set::hash_delegate (STL/CLR)](../dotnet/hash-set-hash-delegate-stl-clr.md)