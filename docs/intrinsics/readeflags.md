---
title: __readeflags | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: __readeflags
dev_langs: C++
helpviewer_keywords: __readeflags intrinsic
ms.assetid: f9d2f4d8-c428-491f-b8de-04d0566b2b6b
caps.latest.revision: "5"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 86e1497bccadf9afd6d26ec3bf4ab8b83e2a2a21
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="readeflags"></a>__readeflags
Lesevorgänge, die der Status der Anwendung und das Steuerelement (EFLAGS) zu registrieren.  
  
## <a name="syntax"></a>Syntax  
  
```  
unsigned     int __readeflags(void);  
unsigned __int64 __readeflags(void);  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Der Wert des Registers EFLAGS. Der Rückgabewert ist 32 Bits lang auf einer 32-Bit-Plattform und 64 Bit lang auf einer 64-Bit-Plattform.  
  
## <a name="remarks"></a>Hinweise  
 Diese Routinen sind nur als systeminterne Funktionen verfügbar.  
  
## <a name="requirements"></a>Anforderungen  
  
|Systemintern|Architektur|  
|---------------|------------------|  
|`__readeflags`|x86, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
  
 **Headerdatei** \<intrin.h >  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Intrinsische Compilerfunktionen](../intrinsics/compiler-intrinsics.md)   
 [__writeeflags](../intrinsics/writeeflags.md)