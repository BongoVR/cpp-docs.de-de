---
title: 'Vector:: push_back (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::vector::push_back
dev_langs:
- C++
helpviewer_keywords:
- push_back member [STL/CLR]
ms.assetid: 4a4c302b-e29f-4b68-b759-2f831814d896
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: c36668b2f2c4c61a2c4c0047b8a8fb8c9100778f
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="vectorpushback-stlclr"></a>vector::push_back (STL/CLR)
Fügt ein neues Letztes Element hinzu.  
  
## <a name="syntax"></a>Syntax  
  
```  
void push_back(value_type val);  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Memberfunktion Fügt ein Element mit dem Wert `val` am Ende der kontrollierten Sequenz. Sie verwenden es, ein anderes Element in den Vektor angefügt werden soll.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_vector_push_back.cpp   
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
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Vektor >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Vektor (STL/CLR)](../dotnet/vector-stl-clr.md)   
 [vector::pop_back (STL/CLR)](../dotnet/vector-pop-back-stl-clr.md)