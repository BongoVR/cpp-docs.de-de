---
title: is_nothrow_copy_constructible-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- is_nothrow_copy_constructible
- type_traits/std::is_nothrow_copy_constructible
dev_langs:
- C++
helpviewer_keywords:
- is_nothrow_copy_constructible
ms.assetid: f13a0bea-63b1-492a-9a45-d445df35c282
caps.latest.revision: 22
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.mt:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 51fbd09793071631985720550007dddbe16f598f
ms.openlocfilehash: c71cdf2bdc69f79884f08ede6cb1dd0c20cbd0cd
ms.lasthandoff: 02/24/2017

---
# <a name="isnothrowcopyconstructible-class"></a>is_nothrow_copy_constructible-Klasse
Testet, ob der Typ einen **nothrow**-Kopierkonstruktor aufweist.  
  
## <a name="syntax"></a>Syntax  
  
```
template <class Ty>
struct is_nothrow_copy_constructible;
```  
  
#### <a name="parameters"></a>Parameter  
 `Ty`  
 Der abzufragende Typ.  
  
## <a name="remarks"></a>Hinweise  
 Eine Instanz des Typprädikats ist "true", wenn der `Ty`-Typ einen nothrow-Kopienkonstruktor aufweist; andernfalls "false".  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<type_traits>  
  
 **Namespace:** std  
  
## <a name="see-also"></a>Siehe auch  
 [<type_traits>](../standard-library/type-traits.md)






