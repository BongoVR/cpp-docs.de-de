---
title: Operator! = (Paar) (STL/CLR) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::pair::operator!=
dev_langs: C++
helpviewer_keywords: operator!= member [STL/CLR]
ms.assetid: 167005f9-727d-40af-8d6d-2793d0daa96a
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 7abfefd389d7e65b9baf7867eb850ef65819350e
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="operator-pair-stlclr"></a>operator!= (pair) (STL/CLR)
Kombinieren Sie nicht gleich Vergleich.  
  
## <a name="syntax"></a>Syntax  
  
```  
template<typename Value1,  
    typename Value2>  
    bool operator!=(pair<Value1, Value2>% left,  
        pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>Parameter  
 links  
 Linke Paar, das verglichen werden soll.  
  
 Rechts  
 Rechts-Paar, das verglichen werden soll.  
  
## <a name="remarks"></a>Hinweise  
 Gibt die Operatorfunktion `!(left == right)`. Sie zum Testen verwenden, ob `left` nicht sortiert wird, ist identisch mit `right` bei der beiden Paare verglichenen elementweise sind.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_pair_operator_ne.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
    cliext::pair<wchar_t, int> c2(L'x', 4);   
    System::Console::WriteLine("[{0}, {1}]", c2.first, c2.second);   
  
    System::Console::WriteLine("[x 3] != [x 3] is {0}",   
        c1 != c1);   
    System::Console::WriteLine("[x 3] != [x 4] is {0}",   
        c1 != c2);   
    return (0);   
    }  
  
```  
  
```Output  
[x, 3]  
[x, 4]  
[x 3] != [x 3] is False  
[x 3] != [x 4] is True  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext-Hilfsprogramm >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [Paar (STL/CLR)](../dotnet/pair-stl-clr.md)   
 [Operator == (Paar) (STL/CLR)](../dotnet/operator-equality-pair-stl-clr.md)   
 [Operator\< (Paar) (STL/CLR)](../dotnet/operator-less-than-pair-stl-clr.md)   
 [Operator > = (Paar) (STL/CLR)](../dotnet/operator-greater-or-equal-pair-stl-clr.md)   
 [Operator > (Paar) (STL/CLR)](../dotnet/operator-greater-than-pair-stl-clr.md)   
 [operator<= (pair) (STL/CLR)](../dotnet/operator-less-or-equal-pair-stl-clr.md)