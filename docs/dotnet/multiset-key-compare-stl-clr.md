---
title: 'multiset:: key_compare (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::multiset::key_compare
dev_langs:
- C++
helpviewer_keywords:
- key_compare member [STL/CLR]
ms.assetid: 172c1ac7-fc71-409e-898a-5521eea7201a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 34617651bfd355cc62738c1488651613372c5d85
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="multisetkeycompare-stlclr"></a>multiset::key_compare (STL/CLR)
Der Delegat für zwei Schlüssel.  
  
## <a name="syntax"></a>Syntax  
  
```  
Microsoft::VisualC::StlClr::BinaryDelegate<GKey, GKey, bool>  
    key_compare;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Typ ist ein Synonym für den Delegaten, der die Reihenfolge der Schlüssel Argumente bestimmt.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_multiset_key_compare.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::multiset<wchar_t> Mymultiset;   
int main()   
    {   
    Mymultiset c1;   
    Mymultiset::key_compare^ kcomp = c1.key_comp();   
  
    System::Console::WriteLine("compare(L'a', L'a') = {0}",   
        kcomp(L'a', L'a'));   
    System::Console::WriteLine("compare(L'a', L'b') = {0}",   
        kcomp(L'a', L'b'));   
    System::Console::WriteLine("compare(L'b', L'a') = {0}",   
        kcomp(L'b', L'a'));   
    System::Console::WriteLine();   
  
// test a different ordering rule   
    Mymultiset c2 = cliext::greater<wchar_t>();   
    kcomp = c2.key_comp();   
  
    System::Console::WriteLine("compare(L'a', L'a') = {0}",   
        kcomp(L'a', L'a'));   
    System::Console::WriteLine("compare(L'a', L'b') = {0}",   
        kcomp(L'a', L'b'));   
    System::Console::WriteLine("compare(L'b', L'a') = {0}",   
        kcomp(L'b', L'a'));   
    return (0);   
    }  
  
```  
  
```Output  
compare(L'a', L'a') = False  
compare(L'a', L'b') = True  
compare(L'b', L'a') = False  
  
compare(L'a', L'a') = False  
compare(L'a', L'b') = False  
compare(L'b', L'a') = True  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Set >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Multiset (STL/CLR)](../dotnet/multiset-stl-clr.md)   
 [multiset:: key_comp (STL/CLR)](../dotnet/multiset-key-comp-stl-clr.md)   
 [multiset:: KEY_TYPE (STL/CLR)](../dotnet/multiset-key-type-stl-clr.md)   
 [multiset::value_compare (STL/CLR)](../dotnet/multiset-value-compare-stl-clr.md)