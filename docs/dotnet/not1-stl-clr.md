---
title: not1 (STL/CLR) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::not1
dev_langs:
- C++
helpviewer_keywords:
- not1 function [STL/CLR]
ms.assetid: a50cd819-10de-4d81-84da-8a34c5414a43
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 1ea947c86569a8725e372a31a9820f68984cfa27
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="not1-stlclr"></a>not1 (STL/CLR)
Generiert eine `unary_negate` für ein Funktionselement ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
template<typename Fun>  
    unary_negate<Fun> not1(Fun% functor);  
```  
  
## <a name="template-parameters"></a>Vorlagenparameter  
 Fun  
 Der Typ, der das Funktionselement.  
  
## <a name="function-parameters"></a>Funktionsparameter  
 Funktionselement  
 Das Funktionselement umschließen.  
  
## <a name="remarks"></a>Hinweise  
 Die Vorlagenfunktion gibt [Unary_negate (STL/CLR)](../dotnet/unary-negate-stl-clr.md)`<Fun>(functor)`. Sie verwenden es als eine einfache Möglichkeit, ein Funktionselement ist nur einem Argument in ein Funktionselement zu umschließen, die dessen logische NOT übermittelt.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_not1.cpp   
// compile with: /clr   
#include <cliext/algorithm>   
#include <cliext/functional>   
#include <cliext/vector>   
  
typedef cliext::vector<int> Myvector;   
int main()   
    {   
    Myvector c1;   
    c1.push_back(4);   
    c1.push_back(0);   
    Myvector c3(2, 0);   
  
// display initial contents " 4 0"   
    for each (int elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// transform and display   
    cliext::logical_not<int> not_op;   
  
    cliext::transform(c1.begin(), c1.begin() + 2, c3.begin(),   
        cliext::unary_negate<cliext::logical_not<int> >(not_op));   
    for each (int elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// transform and display with function   
    cliext::transform(c1.begin(), c1.begin() + 2, c3.begin(),   
        cliext::not1(not_op));   
    for each (int elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
4 0  
1 0  
1 0  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext/funktionale >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [unary_negate (STL/CLR)](../dotnet/unary-negate-stl-clr.md)