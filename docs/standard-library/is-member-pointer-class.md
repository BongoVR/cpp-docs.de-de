---
title: "is_member_pointer-Klasse | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "std::tr1::is_member_pointer"
  - "is_member_pointer"
  - "std.tr1.is_member_pointer"
  - "std.is_member_pointer"
  - "std::is_member_pointer"
  - "type_traits/std::is_member_pointer"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "is_member_pointer-Klasse [TR1]"
  - "is_member_pointer"
ms.assetid: da07ff4e-9ee0-4baa-ad93-1741f10913d1
caps.latest.revision: 19
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 19
---
# is_member_pointer-Klasse
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Testet, ob Typ ein Memberzeiger ist.  
  
## Syntax  
  
```  
template<class Ty>  
    struct is_member_pointer;  
```  
  
#### Parameter  
 `Ty`  
 Der Typ in Abfragen.  
  
## Hinweise  
 Eine Instanz der Typprädikatgriffe True, wenn der Typ `Ty` ein Zeiger auf eine Memberfunktion oder ein Zeiger z Memberobjekt ist oder ein `cv-qualified` Formular von einem davon; andernfalls false hält er an.  
  
## Beispiel  
  
```  
// std_tr1__type_traits__is_member_pointer.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct trivial   
    {   
    int val;   
    };   
  
struct functional   
    {   
    int f();   
    };   
  
int main()   
    {   
    std::cout << "is_member_pointer<trivial *> == "   
        << std::boolalpha   
        << std::is_member_pointer<trivial *>::value   
        << std::endl;   
    std::cout << "is_member_pointer<int trivial::*> == "   
        << std::boolalpha   
        << std::is_member_pointer<int trivial::*>::value   
        << std::endl;   
    std::cout << "is_member_pointer<int (functional::*)()> == "   
        << std::boolalpha   
        << std::is_member_pointer<int (functional::*)()>::value   
        << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **is\_member\_pointertrivial \<\*\> \=\= false**  
**is\_member\_pointerint \<trivial::\*\> \=\= true**  
**is\_member\_pointerint \<\(functional::\*\)\(\)\-\> \=\= true**   
## Anforderungen  
 **Header:** \<type\_traits\>  
  
 **Namespace:** std  
  
## Siehe auch  
 [\<type\_traits\>](../standard-library/type-traits.md)   
 [is\_member\_function\_pointer\-Klasse](../standard-library/is-member-function-pointer-class.md)   
 [is\_member\_object\_pointer\-Klasse](../standard-library/is-member-object-pointer-class.md)   
 [is\_pointer\-Klasse](../standard-library/is-pointer-class.md)