---
title: conditional-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- type_traits/std::conditional
dev_langs:
- C++
helpviewer_keywords:
- conditional class
- conditional
ms.assetid: ece9f539-fb28-4e26-a79f-3264bc984493
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
ms.translationtype: MT
ms.sourcegitcommit: 65f4e356ad0d46333b0d443d0fd6ac0b9f2b6f58
ms.openlocfilehash: 2c764bfc42d633a3036f2e567078b9ea39feea8b
ms.contentlocale: de-de
ms.lasthandoff: 10/03/2017

---
# <a name="conditional-class"></a>conditional-Klasse
Wählt einen von zwei Typen, abhängig von der angegebenen Bedingung.  
  
## <a name="syntax"></a>Syntax  
  
```
template <bool B, class T1, class T2>  
struct conditional;

template <bool _Test, class _T1, class _T2>  
using conditional_t = typename conditional<_Test, _T1, _T2>::type;
```  
  
#### <a name="parameters"></a>Parameter  
 `B`  
 Der Wert, der den ausgewählten Typ bestimmt.  
  
 `T1`  
 Das Typergebnis, wenn B „true“ ist.  
  
 `T2`  
 Das Typergebnis, wenn B „false“ ist.  
  
## <a name="remarks"></a>Hinweise  
 Die Vorlagenmember-Typdefinition (typedef) `conditional<B, T1, T2>::type` wird mit `T1` ausgewertet, wenn `B` mit `true`ausgewertet wird, und wird mit `T2` ausgewertet, wenn `B` mit `false`ausgewertet wird.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<type_traits>  
  
 **Namespace:** std  
  
## <a name="see-also"></a>Siehe auch  
 [<type_traits>](../standard-library/type-traits.md)




