---
title: Compiler-Fehler C3772 | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3772
dev_langs:
- C++
helpviewer_keywords:
- C3772
ms.assetid: 63e938d4-088d-41cc-a562-5881a05b5710
caps.latest.revision: 13
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 65e7a7bd56096fbeec61b651ab494d82edef9c90
ms.openlocfilehash: 7bf4fc0d7e80d2bd77343ee43c31dc74b93c97de
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3772"></a>Compilerfehler C3772
"Name": Ungültige Friend-Vorlagendeklaration.  
  
Es ist unzulässig, einen "Friend" einer Spezialisierung einer Klassenvorlage zu deklarieren. Sie können keine explizite oder partielle Spezialisierung einer Klassenvorlage deklarieren und in derselben Anweisung einen "Friend" dieser Spezialisierung deklarieren. Die *Name* -Platzhalter identifiziert die ungültige Deklaration.  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Sie sollten keinen "Friend" der Spezialisierung einer Klassenvorlage deklarieren.  
  
-   Deklarieren Sie einen "Friend" der Klassenvorlage oder einen "Friend" einer bestimmten partiellen oder expliziten Spezialisierung, sofern dies für Ihre Anwendung geeignet ist.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel tritt ein Fehler auf, da ein "Friend" einer partiellen Spezialisierung einer Klassenvorlage deklariert wird.  
  
```cpp  
// c3772.cpp  
// compile with: /c  
  
// A class template.  
    template<class T> class A {};  
  
// A partial specialization of the class template.  
    template<class T> class A<T*> {};  
  
// An explicit specialization.  
    template<> class A<char>;  
  
class X {  
// Invalid declaration of a friend of a partial specialization.  
    template<class T> friend class A<T*>; // C3772  
  
// Instead, if it is appropriate for your application, declare a   
// friend of the class template. Consequently, all specializations   
// of the class template are friends:  
//    template<class T> friend class A;  
// Or declare a friend of a particular partial specialization:  
//    friend class A<int*>;  
// Or declare a friend of a particular explicit specialization:  
//    friend class A<char>;  
};  
```  
  
## <a name="see-also"></a>Siehe auch  
[Vorlagen](../../cpp/templates-cpp.md)   
[Spezialisierung einer Klassenvorlage](../../cpp/template-specialization-cpp.md)   

