---
title: expm1, expm1f, expm1l | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- expm1l
- expm1
- expm1f
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
- expm1l
- expm1
- expm1f
dev_langs:
- C++
helpviewer_keywords:
- expm1f function
- expm1l function
- expm1 function
ms.assetid: 2a4dd2d9-370c-42b0-9067-0625efa272e0
caps.latest.revision: 4
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
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
ms.sourcegitcommit: 84964b0a49b236bae056125de8155b18880eb378
ms.openlocfilehash: 0fbce9639718ca7316494b1f573a817d8ab0e6f1
ms.lasthandoff: 02/24/2017

---
# <a name="expm1-expm1f-expm1l"></a>expm1, expm1f, expm1l
Berechnet das base-e-Exponential eines Werts minus eins.  
  
## <a name="syntax"></a>Syntax  
  
```  
double expm1(   
   double x   
);  
float expm1(  
   float x  
);  // C++ only  
long double expm1(  
   long double x  
);  // C++ only  
float expm1f(  
   float x  
);  
long double expm1l(  
   long double x  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `x`  
 Das Exponential des Gleitkommawerts.  
  
## <a name="return-value"></a>Rückgabewert  
 Die `expm1`-Funktionen geben einen Gleitkommawert zurück, der im Erfolgsfall e<sup>x</sup> – 1 darstellt. Bei einem Überlauf gibt `expm1``HUGE_VAL` zurück, `expm1f` gibt `HUGE_VALF` zurück, `expm1l` gibt  `HUGE_VALL` zurück und `errno` wird auf `ERANGE` gesetzt. Weitere Informationen zu Rückgabecodes finden Sie unter [errno, _doserrno, _sys_errlist und _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).  
  
## <a name="remarks"></a>Hinweise  
 Da C++ das Überladen zulässt, können Sie Überladungen von `expm1` aufrufen, die `float`- und `long double`-Werte verwenden und zurückgeben. In einem C-Programm verwendet `expm1` immer `double` und gibt diesen Wert zurück.  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|  
|-------------|---------------------|  
|`expm1`, `expm1f`, `expm1l`|\<math.h>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).  
  
## <a name="net-framework-equivalent"></a>Entsprechung in .NET Framework  
 Nicht zutreffend. Mit `PInvoke`rufen Sie die Standard-C-Funktion auf. Weitere Informationen finden Sie unter [Beispiele für Plattformaufrufe](http://msdn.microsoft.com/Library/15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## <a name="see-also"></a>Siehe auch  
 [Gleitkommaunterstützung](../../c-runtime-library/floating-point-support.md)   
 [exp2, exp2f, exp2l](http://msdn.microsoft.com/en-us/a7974629-be1e-4196-a562-6624a0732003)   
 [pow, powf, powl](../../c-runtime-library/reference/pow-powf-powl.md)
