---
title: _umul128 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- __umul128
dev_langs:
- C++
helpviewer_keywords:
- __umul128 intrinsic
ms.assetid: 13684df3-3ac7-467c-b258-a0e93bc490b5
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 64e4658fbb92a9ae693aed7bb8c940230b11d88c
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2018
---
# <a name="umul128"></a>_umul128
**Microsoft-spezifisch**  
  
 Multipliziert zwei 64-Bit-Ganzzahlen ohne Vorzeichen, die als die ersten beiden Argumente übergeben wurden, und setzt die oberen 64 Bits des Produkts in die 64-Bit-Ganzzahl ohne Vorzeichen, auf die `HighProduct` verweist, und gibt die unteren 64 Bits des Produkts zurück.  
  
## <a name="syntax"></a>Syntax  
  
```  
unsigned __int64 _umul128(   
   unsigned __int64 Multiplier,   
   unsigned __int64 Multiplicand,   
   unsigned __int64 *HighProduct   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in] `Multiplier`  
 Die erste zu multiplizierende 64-Bit-Ganzzahl.  
  
 [in] `Multiplicand`  
 Die zweite zu multiplizierende 64-Bit-Ganzzahl.  
  
 [out] `HighProduct`  
 Die oberen 64 Bits des Produkts.  
  
## <a name="return-value"></a>Rückgabewert  
 Die unteren 64 Bits des Produkts.  
  
## <a name="requirements"></a>Anforderungen  
  
|Systemintern|Architektur|Header|  
|---------------|------------------|------------|  
|`_umul128`|ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<intrin.h>|  
  
## <a name="example"></a>Beispiel  
  
```  
// umul128.c  
// processor: IPF, x64  
  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic(_umul128)  
  
int main()  
{  
    unsigned __int64 a = 0x0fffffffffffffffI64;  
    unsigned __int64 b = 0xf0000000I64;  
    unsigned __int64 c, d;  
  
    d = _umul128(a, b, &c);  
  
    printf_s("%#I64x * %#I64x = %#I64x%I64x\n", a, b, c, d);  
}  
```  
  
```Output  
0xfffffffffffffff * 0xf0000000 = 0xeffffffffffffff10000000  
```  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)