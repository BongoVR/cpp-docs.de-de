---
title: "pair::second_type (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::pair::second_type"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "second_type-Member [STL/CLR]"
ms.assetid: 555f0216-186b-4dac-babc-1499f69e5c1b
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# pair::second_type (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Der Typ des zweiten umschlossenen Werts.  
  
## Syntax  
  
```  
typedef Value2 second_type;  
```  
  
## Hinweise  
 Der Typ ist ein Synonym für den Vorlagenparameter `Value2`.  
  
## Beispiel  
  
```  
// cliext_pair_second_type.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    cliext::pair<wchar_t, int>::first_type first_val = c1.first;   
    cliext::pair<wchar_t, int>::second_type second_val = c1.second;   
    System::Console::WriteLine("[{0}, {1}]", first_val, second_val);   
    return (0);   
    }  
  
```  
  
  **\[x, 3\]**   
## Anforderungen  
 **Header:** \<cliext\/Hilfsprogramm\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [pair](../dotnet/pair-stl-clr.md)   
 [pair::first](../dotnet/pair-first-stl-clr.md)   
 [pair::first\_type](../dotnet/pair-first-type-stl-clr.md)   
 [pair::second](../dotnet/pair-second-stl-clr.md)