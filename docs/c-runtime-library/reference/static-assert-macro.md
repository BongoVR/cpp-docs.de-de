---
title: _STATIC_ASSERT-Makro | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- _STATIC_ASSERT
dev_langs:
- C++
helpviewer_keywords:
- _STATIC_ASSERT macro
ms.assetid: 89b0350c-2c2f-4be6-9786-8b1f0780a5da
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bbbab8314a038d796ebd1a13342f3054e59f3e68
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="staticassert-macro"></a>_STATIC_ASSERT-Makro

Auswerten eines Ausdrucks zum Zeitpunkt der Kompilierung und ein Fehler generiert, wenn das Ergebnis ist **"false"**.

## <a name="syntax"></a>Syntax

```C
_STATIC_ASSERT(
    booleanExpression
);
```

### <a name="parameters"></a>Parameter

*boolescher Ausdruck* Ausdruck (einschließlich Zeiger), der zu ungleich null ergibt (**"true"**) oder 0 (**"false"**).

## <a name="remarks"></a>Hinweise

Dieses Makro ähnelt der [_ASSERT- und _ASSERTE-Makros](assert-asserte-assert-expr-macros.md), außer dass *boolescher* wird zur Kompilierzeit statt zur Laufzeit ausgewertet. Wenn *boolescher* ergibt **"false"** (0), [Compilerfehler C2466](../../error-messages/compiler-errors-1/compiler-error-c2466.md) wird generiert.

## <a name="example"></a>Beispiel

In diesem Beispiel überprüfen wir, ob die ["sizeof"](../../c-language/sizeof-operator-c.md) ein **Int** ist größer als oder gleich 2 Byte und gibt an, ob die ["sizeof"](../../c-language/sizeof-operator-c.md) eine **lange** 1 Byte. Das Programm nicht kompiliert, und es wird generiert, [Compilerfehler C2466](../../error-messages/compiler-errors-1/compiler-error-c2466.md) da eine **lange** ist größer als 1 Byte.

```C
// crt__static_assert.c

#include <crtdbg.h>
#include <stdio.h>

_STATIC_ASSERT(sizeof(int) >= 2);
_STATIC_ASSERT(sizeof(long) == 1);  // C2466

int main()
{
    printf("I am sure that sizeof(int) will be >= 2: %d\n",
        sizeof(int));
    printf("I am not so sure that sizeof(long) == 1: %d\n",
        sizeof(long));
}
```

## <a name="requirements"></a>Anforderungen

|Makro|Erforderlicher Header|
|-----------|---------------------|
|**_STATIC_ASSERT**|\<crtdbg.h>|

## <a name="see-also"></a>Siehe auch

[Alphabetische Funktionsreferenz](crt-alphabetical-function-reference.md)<br/>
[_ASSERT, _ASSERTE, _ASSERT_EXPR Macros](assert-asserte-assert-expr-macros.md)<br/>
