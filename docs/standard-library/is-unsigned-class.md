---
title: is_unsigned-Klasse | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- type_traits/std::is_unsigned
dev_langs:
- C++
helpviewer_keywords:
- is_unsigned class
- is_unsigned
ms.assetid: ba5bec3d-796b-4e54-8595-a3941ec6a8dc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 66128074d7beb52ab73f2e6b48371999d38e83a5
ms.sourcegitcommit: 96cdc2da0d8c3783cc2ce03bd280a5430e1ac01d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2018
---
# <a name="isunsigned-class"></a>is_unsigned-Klasse

Prüft, ob der Typ eine Ganzzahl ohne Vorzeichen ist.

## <a name="syntax"></a>Syntax

```cpp
template <class Ty>
struct is_unsigned;
```

### <a name="parameters"></a>Parameter

`Ty` Der abzufragende Typ.

## <a name="remarks"></a>Hinweise

Eine Instanz des Typs Prädikat ist true, wenn der Typ `Ty` ein eine Ganzzahl ohne Vorzeichen ist oder ein `cv-qualified` vorzeichenloser Ganzzahltyp ist, andernfalls enthält er false.

## <a name="example"></a>Beispiel

```cpp
// std__type_traits__is_unsigned.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

struct trivial
    {
    int val;
    };

int main()
    {
    std::cout << "is_unsigned<trivial> == " << std::boolalpha
        << std::is_unsigned<trivial>::value << std::endl;
    std::cout << "is_unsigned<int> == " << std::boolalpha
        << std::is_unsigned<int>::value << std::endl;
    std::cout << "is_unsigned<unsigned int> == " << std::boolalpha
        << std::is_unsigned<unsigned int>::value << std::endl;
    std::cout << "is_unsigned<float> == " << std::boolalpha
        << std::is_unsigned<float>::value << std::endl;

    return (0);
    }

```

```Output
is_unsigned<trivial> == false
is_unsigned<int> == false
is_unsigned<unsigned int> == true
is_unsigned<float> == false
```

## <a name="requirements"></a>Anforderungen

**Header:** \<type_traits>

**Namespace:** std

## <a name="see-also"></a>Siehe auch

[<type_traits>](../standard-library/type-traits.md)<br/>
[is_signed-Klasse](../standard-library/is-signed-class.md)<br/>
