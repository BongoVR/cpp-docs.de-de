---
title: "vector::clear (STL/CLR)"
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
  - "cliext::vector::clear"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "clear-Member [STL/CLR]"
ms.assetid: 4ed20ec8-3089-4c36-b68f-1b51c639041f
caps.latest.revision: 15
caps.handback.revision: "13"
ms.author: "mblome"
manager: "ghogen"
---
# vector::clear (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Entfernt alle Elemente.  
  
## Syntax  
  
```  
void clear();  
```  
  
## Hinweise  
 Die Memberfunktion wird effektiv [vector::erase](../dotnet/vector-erase-stl-clr.md)`(` [vector::begin](../dotnet/vector-begin-stl-clr.md)`(),` [vector::end](../dotnet/vector-end-stl-clr.md)`())` auf.  Sie verwenden sie, um sicherzustellen, dass die gesteuerte Sequenz leer ist.  
  
## Beispiel  
  
```  
// cliext_vector_clear.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// clear the container and reinspect   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
// add elements and clear again   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
  
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
  **ein b c**  
**size\(\) \= 0**  
 **ein b**  
**size\(\) \= 0**   
## Anforderungen  
 **Header:** \<cliext\/Vektor\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [Vektor](../dotnet/vector-stl-clr.md)   
 [vector::erase](../dotnet/vector-erase-stl-clr.md)