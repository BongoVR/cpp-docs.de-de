---
title: systeminterne Funktionen "_interlockedbittestandreset" | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- _interlockedbittestandreset_rel
- _interlockedbittestandreset64
- _interlockedbittestandreset64_HLERelease
- _interlockedbittestandreset_HLERelease
- _interlockedbittestandreset_HLEAcquire
- _interlockedbittestandreset_acq
- _interlockedbittestandreset_cpp
- _interlockedbittestandreset_nf
- _interlockedbittestandreset64_cpp
- _interlockedbittestandreset64_HLEAcquire
- _interlockedbittestandreset
dev_langs:
- C++
helpviewer_keywords:
- lock_btr instruction
- _interlockedbittestandreset64 intrinsic
- _interlockedbittestandreset intrinsic
ms.assetid: 9bbb1442-f2e9-4dc2-b0da-97f3de3493b9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c292d344727f2cc473dc444853a2c46d94150dd0
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="interlockedbittestandreset-intrinsic-functions"></a>Intrinsische Funktionen „_interlockedbittestandreset“
**Microsoft-spezifisch**  
  
 Generiert eine Anweisung, die Bit `b` der Adresse `a` auf 0 (null) setzt und den ursprünglichen Wert zurückgibt.  
  
## <a name="syntax"></a>Syntax  
  
```  
unsigned char _interlockedbittestandreset(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_acq(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_HLEAcquire(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_HLERelease(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_nf(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_rel(  
   long *a,  
   long b  
);   
unsigned char _interlockedbittestandreset64(  
   __int64 *a,  
   __int64 b  
);   
unsigned char _interlockedbittestandreset64_HLEAcquire(  
   __int64 *a,  
   __int64 b  
);  
unsigned char _interlockedbittestandreset64_HLERelease(  
   __int64 *a,  
   __int64 b  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in] `a`  
 Ein Zeiger auf den zu untersuchenden Speicher.  
  
 [in] `b`  
 Die zu testende Bitposition.  
  
## <a name="return-value"></a>Rückgabewert  
 Der ursprüngliche Wert des Bits an der durch `b` angegebenen Position.  
  
## <a name="requirements"></a>Anforderungen  
  
|Systemintern|Architektur|Header|  
|---------------|------------------|------------|  
|`_interlockedbittestandreset`|x86, ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<intrin.h>|  
|`_interlockedbittestandreset_acq`, `_interlockedbittestandreset_nf`, `_interlockedbittestandreset_rel`|ARM|\<intrin.h>|  
|`_interlockedbittestandreset_HLEAcquire`, `_interlockedbittestandreset_HLERelease`|x86, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<immintrin.h>|  
|`_interlockedbittestandreset64`|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<intrin.h>|  
|`_interlockedbittestandreset64_HLEAcquire`, `_interlockedbittestandreset64_HLERelease`|[!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<immintrin.h>|  
  
## <a name="remarks"></a>Hinweise  
 Auf x86- und [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]-Prozessoren verwenden diese systeminternen Funktionen die `lock btr`-Anweisung, die das angegebene Bit liest und in einem atomarischen Vorgang auf 0 (null) setzt.  
  
 Verwenden Sie auf ARM-Prozessoren die systeminternen Funktionen mit den Suffixen `_acq` und `_rel`, wenn Sie Semantiken zum Abrufen bzw. Freigeben benötigen, wie am Anfang und Ende eines kritischen Abschnitts. Die systeminternen ARM-Funktionen mit dem Suffix `_nf` („no fence“) dienen nicht als Arbeitsspeicherbarriere.  
  
 Auf Intel-Prozessoren, die Hardware Lock Elision (HLE)-Anweisungen unterstützen, enthalten die systeminternen Funktionen mit den Suffixen `_HLEAcquire` und `_HLERelease` einen Hinweis auf den Prozessor, der die Leistung durch Beseitigen einer Schreibsperre in der Hardware beschleunigen kann. Wenn diese systeminternen Funktionen auf Prozessoren aufgerufen werden, die HLE nicht unterstützen, wird der Hinweis ignoriert.  
  
 Diese Routinen sind nur als systeminterne Funktionen verfügbar.  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)   
 [Konflikt mit dem x86-Compiler](../build/conflicts-with-the-x86-compiler.md)