---
title: carg, cargf, cargl | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp
- devlang-cpp
ms.topic: reference
apiname:
- carg
- cargf
- cargl
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
- carg
- cargf
- cargl
- complex/carg
- complex/cargf
- complex/cargl
dev_langs:
- C++
helpviewer_keywords:
- carg function
- cargf function
- cargl function
ms.assetid: 610d6a93-b929-46ab-a966-b77db0b804be
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 34a5e55b4261c68d90c3bcb28cf2f0e7be1a2c50
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="carg-cargf-cargl"></a>carg, cargf, cargl

Ruft das Argument einer komplexen Zahl mit einem Achsenabschnitt auf der negativen reellen Achse ab.

## <a name="syntax"></a>Syntax

```C
double carg(
   _Dcomplex z
);
float carg(
   _Fcomplex z
);  // C++ only
long double carg(
   _Lcomplex z
);  // C++ only
float cargf(
   _Fcomplex z
);
long double cargl(
   _Lcomplex z
);
```

### <a name="parameters"></a>Parameter

*z*<br/>
Eine komplexe Zahl.

## <a name="return-value"></a>Rückgabewert

Das Argument (auch bekannt als die Phase) *z*. Das Ergebnis wird im Intervall [-π, + π].

## <a name="remarks"></a>Hinweise

Da C++ das Überladen zulässt, können Sie Überladungen von Aufrufen **Carg** nehmen **_Fcomplex** oder **_Lcomplex** Werte, und der Rückgabewert **"float"** oder **lange** **doppelte** Werte. In einem C-Programm **Carg** immer ein **_Dcomplex** Wert und gibt eine **doppelte** Wert.

## <a name="requirements"></a>Anforderungen

|Routine|C-Header|C++-Header|
|-------------|--------------|------------------|
|**Carg**, **Cargf**, **Cargl**|\<complex.h>|\<ccomplex>|

Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>Siehe auch

[Alphabetische Funktionsreferenz](crt-alphabetical-function-reference.md)<br/>
[norm, normf, norml](norm-normf-norml1.md)<br/>
[creal, crealf, creall](creal-crealf-creall.md)<br/>
[cproj, cprojf, cprojl](cproj-cprojf-cprojl.md)<br/>
[conj, conjf, conjl](conj-conjf-conjl.md)<br/>
[cimag, cimagf, cimagl](cimag-cimagf-cimagl.md)<br/>
[cabs, cabsf, cabsl](cabs-cabsf-cabsl.md)<br/>
