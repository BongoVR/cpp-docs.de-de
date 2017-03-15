---
title: "operator&lt; (queue) (STL/CLR)"
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
  - "cliext::queue::operator<"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "operator<-Member [STL/CLR]"
ms.assetid: 2c981e2b-9a88-4b4a-8060-9ac24d5631f5
caps.latest.revision: 15
caps.handback.revision: "13"
ms.author: "mblome"
manager: "ghogen"
---
# operator&lt; (queue) (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Warteschlangenkleiner\-als\-vergleich.  
  
## Syntax  
  
```  
template<typename Value,  
    typename Container>  
    bool operator<(queue<Value, Container>% left,  
        queue<Value, Container>% right);  
```  
  
#### Parameter  
 left  
 Linker Container zu vergleichen.  
  
 right  
 Rechter Container zu vergleichen.  
  
## Hinweise  
 Die Operatorfunktionsrückgaben true, wenn für die niedrigste Position für die `i``!(``right``[i] <` `left``[i])` ist es auch dass `left``[i] <` `right``[i]` aus.  Andernfalls ist `left``->`[queue::size](../dotnet/queue-size-stl-clr.md)`() <` `right``->size()` zurück, das Sie es verwenden, um zu testen, ob `left` vor `right` sortiert wird, wenn die beiden verglichenes Warteschlangen Element durch Element sind.  
  
## Beispiel  
  
```  
// cliext_queue_operator_lt.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::queue<wchar_t> Myqueue;   
int main()   
    {   
    Myqueue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    Myqueue c2;   
    c2.push(L'a');   
    c2.push(L'b');   
    c2.push(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] < [a b c] is {0}",   
        c1 < c1);   
    System::Console::WriteLine("[a b c] < [a b d] is {0}",   
        c1 < c2);   
    return (0);   
    }  
  
```  
  
  **ein b c**  
 **ein b d**  
**\[ein b c\] \< \[ein b c\] ist falsch**  
**\[ein b c ein b\] \< \[d\] gilt**   
## Anforderungen  
 **Header:** \<cliext\/Warteschlange\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [queue](../dotnet/queue-stl-clr.md)   
 [operator\=\= \(queue\)](../dotnet/operator-equality-queue-stl-clr.md)   
 [operator\!\= \(queue\)](../dotnet/operator-inequality-queue-stl-clr.md)   
 [operator\>\= \(queue\)](../dotnet/operator-greater-or-equal-queue-stl-clr.md)   
 [operator\> \(queue\)](../dotnet/operator-greater-than-queue-stl-clr.md)   
 [operator\<\= \(queue\)](../dotnet/operator-less-or-equal-queue-stl-clr.md)