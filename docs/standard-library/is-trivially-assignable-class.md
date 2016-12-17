---
title: "Is_trivially_assignable-Klasse"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "cpp"
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "language-reference"
f1_keywords: 
  - "is_trivially_assignable"
  - "std.is_trivially_assignable"
  - "std::is_trivially_assignable"
  - "type_traits/std::is_trivially_assignable"
dev_langs: 
  - "C++"
  - "c++"
helpviewer_keywords: 
  - "is_trivially_assignable"
ms.assetid: 1284a8f7-4093-426d-9c9a-dabb46f90d6d
caps.latest.revision: 13
caps.handback.revision: "3"
ms.author: "corob"
manager: "ghogen"
---
# Is_trivially_assignable-Klasse
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Testet, ob der Wert `From` Typ zugewiesen werden kann im Grunde `To` Typ  
  
## Syntax  
  
```  
template <class To, class From>  
    struct is_trivially_assignable;  
```  
  
#### Parameter  
 Beschreibung  
 Der Typ des Objekts, das die Zuweisung empfängt.  
  
 Von  
 Der Typ des Objekts, das den Wert bereitstellt.  
  
## Hinweise  
 Der Ausdruck `declval<To>() = declval<From>()` muss wohlgeformt sein und muss keine nicht trivialen Vorgänge erfordern für den Compiler bekannt sein. Beide `From` und `To` muss vollständige Typen `void`, oder Arrays von unbekannten gebunden.  
  
## Anforderungen  
 **Header:** \<type\_traits\>  
  
 **Namespace:** std  
  
## Siehe auch  
 [\<type\_traits\>](../standard-library/type-traits.md)