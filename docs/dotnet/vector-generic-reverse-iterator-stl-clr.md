---
title: Vector::generic_reverse_iterator (STL/CLR) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::vector::generic_reverse_iterator
dev_langs:
- C++
helpviewer_keywords:
- generic_reverse_iterator member [STL/CLR]
ms.assetid: f769bd6e-4015-4730-b142-ab89c407d811
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: a3652f3a0afc92d665e311f8973e9be1d1fe532c
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="vectorgenericreverseiterator-stlclr"></a>vector::generic_reverse_iterator (STL/CLR)
Der Typ eines umgekehrten Iterators für die Verwendung mit der generischen Schnittstelle für den Container.  
  
## <a name="syntax"></a>Syntax  
  
```  
typedef Microsoft::VisualC::StlClr::Generic::  
    ReverseRandomAccessIterator<generic_value> generic_reverse_iterator;  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Typ beschreibt einen generischen reverse-Iterator, der für diese Vorlage Container-Klasse mit der generischen Schnittstelle verwendet werden kann.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_vector_generic_reverse_iterator.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct a generic container   
    cliext::vector<wchar_t>::generic_container^ gc1 = %c1;   
    for each (wchar_t elem in gc1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// modify generic and display original   
    cliext::vector<wchar_t>::generic_reverse_iterator gcit = gc1->rbegin();   
    cliext::vector<wchar_t>::generic_value gcval = *gcit;   
    *++gcit = gcval;   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
a b c  
a c c  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Vektor >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Vektor (STL/CLR)](../dotnet/vector-stl-clr.md)   
 [Vector::generic_container (STL/CLR)](../dotnet/vector-generic-container-stl-clr.md)   
 [vector::generic_iterator (STL/CLR)](../dotnet/vector-generic-iterator-stl-clr.md)