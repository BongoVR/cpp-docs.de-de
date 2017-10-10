---
title: Compilerfehler C2218 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2218
dev_langs:
- C++
helpviewer_keywords:
- C2218
ms.assetid: b0f55da4-8edb-4b45-b298-1a091981bd7b
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 3ca2e431fdfeff3c9dc957bee46f84cfd2c04162
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2218"></a>Compilerfehler C2218
"__vectorcall" kann nicht zusammen mit "/arch:IA32" verwendet werden.  
  
 Die Aufrufkonvention `__vectorcall` wird nur in systemeigenem Code auf x86- und x64-Prozessoren unterstützt, die zusätzlich SIMD-Streamingerweiterungen 2 (SSE2) und höher einschließen. Weitere Informationen finden Sie unter [__vectorcall](../../cpp/vectorcall.md).  
  
 Um diesen Fehler zu beheben, ändern Sie die Compileroptionen in die Befehlssätze Ziel SSE2, AVX oder AVX2. Weitere Informationen finden Sie unter [/arch (x86)](../../build/reference/arch-x86.md).
