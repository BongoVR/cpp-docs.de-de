---
title: csin, csinf, csinl | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp
- devlang-cpp
ms.topic: reference
apiname:
- csin
- csinf
- csinl
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
- csin
- csinf
- csinl
- complex/csin
- complex/csinf
- complex/csinl
dev_langs:
- C++
helpviewer_keywords:
- csin function
- csinf function
- csinl function
ms.assetid: 3ed475e8-9aae-42ba-a25c-7ae656a0fd4d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 572220af53fe937dd0d5306f0e0e7d287b1d41b8
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="csin-csinf-csinl"></a>csin, csinf, csinl

Ruft den Kosinus einer komplexen Zahl ab

## <a name="syntax"></a>Syntax

```C
_Dcomplex csin(
   _Dcomplex z
);
_Fcomplex csin(
   _Fcomplex z
);  // C++ only
_Lcomplex csin(
   _Lcomplex z
);  // C++ only
_Fcomplex csinf(
   _Fcomplex z
);
_Lcomplex csinl(
   _Lcomplex z
);
```

### <a name="parameters"></a>Parameter

*z*<br/>
Eine komplexe Zahl, die einen Winkel als Bogenmaß darstellt

## <a name="return-value"></a>Rückgabewert

Der Sinus von *z*, im Bogenmaß.

## <a name="remarks"></a>Hinweise

Da C++ das Überladen zulässt, können Sie Überladungen von Aufrufen **Csin** verwenden und zurückgeben **_Fcomplex** und **_Lcomplex** Werte. In einem C-Programm **Csin** immer Double und gibt eine **_Dcomplex** Wert.

## <a name="requirements"></a>Anforderungen

|Routine|C-Header|C++-Header|
|-------------|--------------|------------------|
|**Csin**, **Csinf**, **Csinl**|\<complex.h>|\<ccomplex>|

Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>Siehe auch

[Alphabetische Funktionsreferenz](crt-alphabetical-function-reference.md)<br/>
[catanh, catanhf, catanhl](catanh-catanhf-catanhl.md)<br/>
[ctanh, ctanhf, ctanhl](ctanh-ctanhf-ctanhl.md)<br/>
[catan, catanf, catanl](catan-catanf-catanl.md)<br/>
[csinh, csinhf, csinhl](csinh-csinhf-csinhl.md)<br/>
[casinh, casinhf, casinhl](casinh-casinhf-casinhl.md)<br/>
[ccosh, ccoshf, ccoshl](ccosh-ccoshf-ccoshl.md)<br/>
[cacosh, cacoshf, cacoshl](cacosh-cacoshf-cacoshl.md)<br/>
[cacos, cacosf, cacosl](cacos-cacosf-cacosl.md)<br/>
[ctan, ctanf, ctanl](ctan-ctanf-ctanl.md)<br/>
[casin, casinf, casinl](casin-casinf-casinl.md)<br/>
[ccos, ccosf, ccosl](ccos-ccosf-ccosl.md)<br/>
[csqrt, csqrtf, csqrtl](csqrt-csqrtf-csqrtl.md)<br/>
