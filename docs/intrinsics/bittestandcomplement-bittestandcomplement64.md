---
title: _bittestandcomplement _bittestandcomplement64 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- _bittestandcomplement64
- _bittestandcomplement64_cpp
- _bittestandcomplement_cpp
- _bittestandcomplement
dev_langs:
- C++
helpviewer_keywords:
- btc instruction
- _bittestandcomplement intrinsic
- _bittestandcomplement64 intrinsic
ms.assetid: 53fa12dd-835e-4e5d-baec-a431c8678806
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3f1c3eb6f6447363fee7bafca33b8ea59c1c7e45
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="bittestandcomplement-bittestandcomplement64"></a>_bittestandcomplement, _bittestandcomplement64
**Microsoft-spezifisch**  
  
 Erzeugen Sie eine Anweisung, die Bit `b` der Adresse `a` untersucht, den aktuellen Wert zurückgibt und das Bit auf seiner Ergänzung setzt.  
  
## <a name="syntax"></a>Syntax  
  
```  
unsigned char _bittestandcomplement(  
   long *a,  
   long b  
);  
unsigned char _bittestandcomplement64(  
   __int64 *a,  
   __int64 b  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in, out] `a`  
 Ein Zeiger auf den zu untersuchenden Speicher.  
  
 [in] `b`  
 Die zu testende Bitposition.  
  
## <a name="return-value"></a>Rückgabewert  
 Das Bit an der angegebenen Position.  
  
## <a name="requirements"></a>Anforderungen  
  
|Systemintern|Architektur|  
|---------------|------------------|  
|`_bittestandcomplement`|x86, ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
|`_bittestandcomplement64`|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
  
 **Headerdatei** \<intrin.h >  
  
## <a name="remarks"></a>Hinweise  
 Diese Routine ist nur als systeminterne Funktion verfügbar.  
  
## <a name="example"></a>Beispiel  
  
```  
// bittestandcomplement.cpp  
// processor: x86, IPF, x64  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic(_bittestandcomplement)  
#ifdef _M_AMD64  
#pragma intrinsic(_bittestandcomplement64)  
#endif  
  
int main()  
{  
   long i = 1;  
   __int64 i64 = 0x1I64;  
   unsigned char result;  
   printf("Initial value: %d\n", i);  
   printf("Testing bit 1\n");  
   result = _bittestandcomplement(&i, 1);  
   printf("Value changed to %d, Result: %d\n", i, result);  
#ifdef _M_AMD64  
   printf("Testing bit 0\n");  
   result = _bittestandcomplement64(&i64, 0);  
   printf("Value changed to %I64d, Result: %d\n", i64, result);  
#endif  
}  
```  
  
## <a name="sample-output"></a>Beispielausgabe  
  
```  
Initial value: 1  
Testing bit 1  
Value changed to 3, Result: 0  
Testing bit 0  
Value changed to 0, Result: 1  
```  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)