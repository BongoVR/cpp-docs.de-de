---
title: Operator&gt;= (Vektor) (STL/CLR) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::vector::operator>=
dev_langs:
- C++
helpviewer_keywords:
- operator>= member [STL/CLR]
ms.assetid: c06f4489-f65a-4bd6-944f-9b23a2bb4e35
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 9aaaaa27b4009a6abc05fcfe8f56d345cc844d64
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="operatorgt-vector-stlclr"></a>Operator&gt;= (Vektor) (STL/CLR)
Vektor größer oder gleich Vergleich.  
  
## <a name="syntax"></a>Syntax  
  
```  
template<typename Value>  
    bool operator>=(vector<Value>% left,  
        vector<Value>% right);  
```  
  
#### <a name="parameters"></a>Parameter  
 links  
 Linker zu vergleichender Container.  
  
 Rechts  
 Rechter zu vergleichender Container.  
  
## <a name="remarks"></a>Hinweise  
 Gibt die Operatorfunktion `!(left < right)`. Sie verwenden es, um zu testen, ob `left` nicht sortiert ist `right` Wenn die beiden Vektoren verglichenen elementweise sind.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_vector_operator_ge.cpp   
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
  
// assign to a new container   
    cliext::vector<wchar_t> c2;   
    c2.push_back(L'a');   
    c2.push_back(L'b');   
    c2.push_back(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] >= [a b c] is {0}",   
        c1 >= c1);   
    System::Console::WriteLine("[a b c] >= [a b d] is {0}",   
        c1 >= c2);   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
 a b d  
[a b c] >= [a b c] is True  
[a b c] >= [a b d] is False  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/Vektor >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Vektor (STL/CLR)](../dotnet/vector-stl-clr.md)   
 [Operator == (Vektor) (STL/CLR)](../dotnet/operator-equality-vector-stl-clr.md)   
 [Operator! = (Vektor) (STL/CLR)](../dotnet/operator-inequality-vector-stl-clr.md)   
 [Operator\< (Vektor) (STL/CLR)](../dotnet/operator-less-than-vector-stl-clr.md)   
 [Operator > (Vektor) (STL/CLR)](../dotnet/operator-greater-than-vector-stl-clr.md)   
 [operator<= (vector) (STL/CLR)](../dotnet/operator-less-or-equal-vector-stl-clr.md)