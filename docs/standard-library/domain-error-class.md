---
title: "domain_error-Klasse | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "domain_error"
  - "std::domain_error"
  - "std.domain_error"
  - "stdexcept/std::domain_error"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "domain_error-Klasse"
ms.assetid: a1d8245d-61c2-4d1e-973f-073bd5dd5fa3
caps.latest.revision: 19
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 19
---
# domain_error-Klasse
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Die Klasse fungiert als Basisklasse für alle Ausnahmen, die ausgelöst werden, um einen Domänenfehler zu melden.  
  
## <a name="syntax"></a>Syntax  
  
```  
class domain_error : public logic_error {  
public:  
    explicit domain_error(const string& message);

    explicit domain_error(const char *message);

};  
```  
  
## <a name="remarks"></a>Hinweise  
 Der Rückgabewert von [Was](../standard-library/exception-class1.md) ist eine Kopie des **Nachricht**`.`[Daten](../standard-library/basic-string-class.md#basic_string__data).  
  
## <a name="example"></a>Beispiel  
  
```  
// domain_error.cpp  
// compile with: /EHsc /GR  
#include <iostream>  
  
using namespace std;  
  
int main( )  
{  
   try   
   {  
      throw domain_error( "Your domain is in error!" );  
   }  
   catch (exception &e)   
   {  
      cerr << "Caught: " << e.what( ) << endl;  
      cerr << "Type: " << typeid(e).name( ) << endl;  
   };  
}  
\* Output:   
Caught: Your domain is in error!  
Type: class std::domain_error  
*\  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \< Stdexcept>  
  
 **Namespace:** std  
  
## <a name="see-also"></a>Siehe auch  
 [Logic_error-Klasse](../standard-library/logic-error-class.md)   
 [Threadsicherheit in der C++-Standardbibliothek](../standard-library/thread-safety-in-the-cpp-standard-library.md)

