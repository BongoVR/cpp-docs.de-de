---
title: "deque::pop_front (STL/CLR)"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "cliext::deque::pop_front"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "pop_front-Member [STL/CLR]"
ms.assetid: 5042df47-b226-4b16-982e-6a4543b8e00b
caps.latest.revision: 16
caps.handback.revision: "14"
ms.author: "mblome"
manager: "ghogen"
---
# deque::pop_front (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Entfernt das erste Element.  
  
## Syntax  
  
```  
void pop_front();  
```  
  
## Hinweise  
 Die Memberfunktion wird das erste Element der gesteuerten Sequenz, die nicht leer sein muss.  Sie verwenden sie, um die Doppelschlange durch ein Element am Vordergrund zu verkürzen.  
  
## Beispiel  
  
```  
// cliext_deque_pop_front.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// pop an element and redisplay   
    c1.pop_front();   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **ein b c**  
 **b c**   
## Anforderungen  
 **Header:** \<cliext\/Doppelschlange\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [deque](../dotnet/deque-stl-clr.md)   
 [deque::pop\_back](../dotnet/deque-pop-back-stl-clr.md)   
 [deque::push\_back](../dotnet/deque-push-back-stl-clr.md)   
 [deque::push\_front](../dotnet/deque-push-front-stl-clr.md)