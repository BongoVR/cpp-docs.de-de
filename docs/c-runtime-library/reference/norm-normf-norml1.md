---
title: Norm, Normf, Norml | Microsoft Docs
ms.custom: ''
ms.date: 04/05/2018
ms.technology:
- cpp
- devlang-cpp
ms.topic: reference
apiname:
- norm
- normf
- norml
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
- api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- norm
- normf
- norml
- complex/norm
- complex/normf
- complex/norml
dev_langs:
- C++
helpviewer_keywords:
- norm function
- normf function
- norml function
ms.assetid: 9786ecfe-0019-4553-b378-0af6c691e15c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 272f43a7b92c069da8fc4eda64a678ff38efd6ab
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="norm-normf-norml"></a>norm, normf, norml

Ruft die quadratische Größe einer komplexen Zahl ab.

## <a name="syntax"></a>Syntax

```C
double norm( _Dcomplex z );
float normf( _Fcomplex z );
long double norml( _Lcomplex z );
```

```cpp
float norm( _Fcomplex z );  // C++ only
long double norm( _Lcomplex z );  // C++ only
```

### <a name="parameters"></a>Parameter

*z*<br/>
Eine komplexe Zahl.

## <a name="return-value"></a>Rückgabewert

Quadriert Maßeinheit *z*.

## <a name="remarks"></a>Hinweise

Da C++ das Überladen zulässt, können Sie Überladungen von Aufrufen **Norm** nehmen **_Fcomplex** oder **_Lcomplex** Werte, und der Rückgabewert **"float"** oder **long double** Werte. In einem C-Programm **Norm** immer ein **_Dcomplex** Wert und gibt eine **doppelte** Wert.

## <a name="requirements"></a>Anforderungen

|Routine|C-Header|C++-Header|
|-------------|--------------|------------------|
|**Norm**, **Normf**, **Norml**|\<complex.h>|\<complex.h>|

Die **_Fcomplex**, **_Dcomplex**, und **_Lcomplex** Typen sind Microsoft-spezifische-Entsprechungen der implementierten native C99 Typen **_Complex float** , **doppelte _Complex**, und **long double _Complex**zugeordnet.  Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>Siehe auch

[Alphabetische Funktionsreferenz](crt-alphabetical-function-reference.md)<br/>
[creal, crealf, creall](creal-crealf-creall.md)<br/>
[cproj, cprojf, cprojl](cproj-cprojf-cprojl.md)<br/>
[conj, conjf, conjl](conj-conjf-conjl.md)<br/>
[cimag, cimagf, cimagl](cimag-cimagf-cimagl.md)<br/>
[carg, cargf, cargl](carg-cargf-cargl.md)<br/>
[cabs, cabsf, cabsl](cabs-cabsf-cabsl.md)<br/>
