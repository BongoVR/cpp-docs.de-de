---
title: . PUSHREG | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- .PUSHREG
dev_langs:
- C++
helpviewer_keywords:
- .PUSHREG directive
ms.assetid: e0c83758-dfed-40ea-afe6-cb833c8d2d30
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 84cc00d51f72993e1e7673d8d4f3d01478d32041
ms.sourcegitcommit: 6002df0ac79bde5d5cab7bbeb9d8e0ef9920da4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2018
---
# <a name="pushreg"></a>.PUSHREG
Generiert eine `UWOP_PUSH_NONVOL` Entladen von Codeeintrag für die angegebene Anzahl, die mit dem aktuellen offset im Prolog registriert.  
  
## <a name="syntax"></a>Syntax  
  
```  
.PUSHREG register  
```  
  
## <a name="remarks"></a>Hinweise  
 . PUSHREG ermöglicht Benutzern das ml64.exe angeben, wie eine Funktion Frame entlädt und ist nur zulässig, innerhalb der Prolog, die aus erweitert die [PROC](../../assembler/masm/proc.md) FRAME-Deklaration, um die [. ENDPROLOG](../../assembler/masm/dot-endprolog.md) Richtlinie. Diese Direktiven generieren keine Code; Es werden nur generiert, `.xdata` und `.pdata`. . PUSHREG sollte Anweisungen vorangestellt werden, die die Aktionen, entladen werden tatsächlich implementieren. Es wird empfohlen, die Direktiven entladen und der Code, den sie in einem Makro Entladung vorgesehen sind, um sicherzustellen, dass Vereinbarung zu umschließen.  
  
 Weitere Informationen finden Sie unter [MASM für X64 (ml64.exe)](../../assembler/masm/masm-for-x64-ml64-exe.md).  
  
## <a name="sample"></a>Beispiel  
  
### <a name="description"></a>Beschreibung  
 Im folgende Beispiel wird gezeigt, wie permanenter Tegisters mithilfe von Push übertragen wird.  
  
### <a name="code"></a>Code  
  
```  
; ml64 ex1.asm /link /entry:Example1 /SUBSYSTEM:CONSOLE  
_text SEGMENT  
Example1 PROC FRAME  
   push r10  
.pushreg r10  
   push r15  
.pushreg r15  
   push rbx  
.pushreg rbx  
   push rsi  
.pushreg rsi  
.endprolog  
   ; rest of function ...  
   ret  
Example1 ENDP  
_text ENDS  
END  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Anweisungen – Referenz](../../assembler/masm/directives-reference.md)