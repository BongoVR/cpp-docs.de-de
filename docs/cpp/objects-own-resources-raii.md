---
title: Objekteigene Ressourcen (RAII) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: f86b484e-5a27-4c3b-a92a-dfaa5dd6d93a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: dfd3f1df54e5b5881ed15efeb98a6e6070f400a1
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="objects-own-resources-raii"></a>Objekteigene Ressourcen (RAII)
Stellen Sie sicher, dass die eigene Ressourcen Objekte. Dieses Prinzip ist auch bekannt als "Resource Acquisition is Initialization" oder "RAII."  
  
## <a name="example"></a>Beispiel  
 Übergeben Sie jedes Objekt "Neues" als Konstruktorargument in ein anderes benanntes Objekt, das er (fast immer Unique_ptr) besitzt.  
  
```cpp  
void f() {  
    unique_ptr<widget> p( new widget() );  
    my_class x( new widget() );  
    // ...  
} // automatic destruction and deallocation for both widget objects  
  // automatic exception safety, as if "finally { p->dispose(); x.w.dispose(); }"  
```  
  
 Übergeben Sie eine neue Ressource immer sofort in ein anderes Objekt aus, das er besitzt.  
  
```cpp  
void g() {  
    other_class y( OpenFile() );  
    // ...  
} // automatic closing and release for file resource  
  // automatic exception safety, as if "finally { y.file.dispose(); }"  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Willkommen zurück bei C++](../cpp/welcome-back-to-cpp-modern-cpp.md)   
 [C++-Sprachreferenz](../cpp/cpp-language-reference.md)   
 [C++-Standardbibliothek](../standard-library/cpp-standard-library-reference.md)