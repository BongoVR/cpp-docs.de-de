---
title: tan, tanf, tanl, tanh, tanhf, tanhl | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: reference
apiname:
- tanhf
- tanh
- tan
- tanhl
- tanf
- tanl
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
- tanh
- tan
- _tanl
- tanl
- _tanhl
- tanf
- tanhf
- tanhl
dev_langs:
- C++
helpviewer_keywords:
- tanl function
- tanhl function
- _tanl function
- _tanhl function
- tan function
- calculating tangents
- tangent
- tanh function
- tanhf function
- tanf function
- trigonometric functions
- hyperbolic functions
ms.assetid: 36cc0ce8-9c80-4653-b354-ddb3b378b6bd
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 0c3391d07e78ba177a3ce31abb26bd5b6ef0449c
ms.sourcegitcommit: 6002df0ac79bde5d5cab7bbeb9d8e0ef9920da4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2018
---
# <a name="tan-tanf-tanl-tanh-tanhf-tanhl"></a>tan, tanf, tanl, tanh, tanhf, tanhl
Berechnet den Tangens (`tan`, `tanf` oder `tanl`) oder den Hyperbeltangens (`tanh`, `tanhf` oder `tanhl`).  
  
## <a name="syntax"></a>Syntax  
  
```  
double tan(  
   double x   
);  
float tan(  
   float x   
);  // C++ only  
long double tan(  
   long double x  
);  // C++ only  
float tanf(  
   float x   
);  
long double tanl(  
   long double x  
);  
double tanh(  
   double x   
);  
float tanh(  
   float x   
);  // C++ only  
long double tanh(  
   long double x  
);  // C++ only  
float tanhf(  
   float x   
);  
long double tanhl(  
   long double x  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `x`  
 Winkel im Bogenmaß.  
  
## <a name="return-value"></a>Rückgabewert  
 Die `tan`-Funktionen geben den Tangens von `x` zurück. Wenn `x` ist größer als oder gleich 263 oder kleiner als oder gleich-263 einer im Ergebnis kommt.  
  
 Die `tanh`-Funktionen geben den Hyperbeltangens von `x` zurück. Es gibt keine Fehlerrückgabe.  
  
|Eingabe|SEH-Ausnahme|`Matherr`-Ausnahme|  
|-----------|-------------------|-------------------------|  
|± QNAN,IND|Keine|_DOMAIN|  
|± ∞  (`tan`, `tanf`)|`INVALID`|_DOMAIN|  
  
## <a name="remarks"></a>Hinweise  
 Da C++ das Überladen zulässt, können Sie Überladungen von `tan` und `tanh` aufrufen, die `float`- oder `long double`-Werte verwenden und zurückgeben. In einem C-Programm verwenden `tan` und `tanh` immer `double` und geben "Double" auch zurück.  
  
## <a name="requirements"></a>Anforderungen  
  
|-Routine zurückgegebener Wert|Erforderlicher Header|  
|-------------|---------------------|  
|`tan`, `tanf`, `tanl`, `tanh`, `tanhf`, `tanhl`|\<math.h>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).  
  
## <a name="example"></a>Beispiel  
  
```  
// crt_tan.c  
// This program displays the tangent of pi / 4  
// and the hyperbolic tangent of the result.  
//  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double pi = 3.1415926535;  
   double x, y;  
  
   x = tan( pi / 4 );  
   y = tanh( x );  
   printf( "tan( %f ) = %f\n", pi/4, x );  
   printf( "tanh( %f ) = %f\n", x, y );  
}  
```  
  
```Output  
tan( 0.785398 ) = 1.000000  
tanh( 1.000000 ) = 0.761594  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Floating-Point Support (Gleitkommaunterstützung)](../../c-runtime-library/floating-point-support.md)   
 [acos, acosf, acosl](../../c-runtime-library/reference/acos-acosf-acosl.md)   
 [asin, asinf, asinl](../../c-runtime-library/reference/asin-asinf-asinl.md)   
 [atan, atanf, atanl, atan2, atan2f, atan2l](../../c-runtime-library/reference/atan-atanf-atanl-atan2-atan2f-atan2l.md)   
 [cos, cosf, cosl, cosh, coshf, coshl](../../c-runtime-library/reference/cos-cosf-cosl-cosh-coshf-coshl.md)   
 [sin, sinf, sinl, sinh, sinhf, sinhl](../../c-runtime-library/reference/sin-sinf-sinl-sinh-sinhf-sinhl.md)   
 [_CItan](../../c-runtime-library/citan.md)