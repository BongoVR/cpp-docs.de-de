---
title: "hash_map::value_comp (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::hash_map::value_comp"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "value_comp-Member [STL/CLR]"
ms.assetid: b11a2dee-07e8-450c-8f85-979c0a15ae64
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# hash_map::value_comp (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Kopiert den Reihenfolgendelegaten für zwei Elementwerte.  
  
## Syntax  
  
```  
value_compare^ value_comp();  
```  
  
## Hinweise  
 Die Memberfunktion gibt den Reihenfolgendelegaten zurück, der verwendet wird, um die gesteuerte Reihenfolge zu sortieren.  Sie verwenden sie, um zwei Elementwerte zu vergleichen.  
  
## Beispiel  
  
```  
// cliext_hash_map_value_comp.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
int main()   
    {   
    Myhash_map c1;   
    Myhash_map::value_compare^ kcomp = c1.value_comp();   
  
    System::Console::WriteLine("compare([L'a', 1], [L'a', 1]) = {0}",   
        kcomp(Myhash_map::make_value(L'a', 1),   
            Myhash_map::make_value(L'a', 1)));   
    System::Console::WriteLine("compare([L'a', 1], [L'b', 2]) = {0}",   
        kcomp(Myhash_map::make_value(L'a', 1),   
            Myhash_map::make_value(L'b', 2)));   
    System::Console::WriteLine("compare([L'b', 2], [L'a', 1]) = {0}",   
        kcomp(Myhash_map::make_value(L'b', 2),   
            Myhash_map::make_value(L'a', 1)));   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **Vergleichen \(\[L'a, 1\], \[L'a, 1\]\) \= True**  
**Vergleichen \(\[L'a, 1\], \[L'b, 2\]\) \= True**  
**Vergleichen \(\[L'b, 2\], \[L'a, 1\] \= False\)**   
## Anforderungen  
 **Header:** \<cliext\/hash\_map\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [hash\_map](../dotnet/hash-map-stl-clr.md)   
 [hash\_map::value\_compare](../dotnet/hash-map-value-compare-stl-clr.md)   
 [hash\_map::value\_type](../dotnet/hash-map-value-type-stl-clr.md)