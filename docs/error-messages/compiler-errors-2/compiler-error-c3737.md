---
title: Compilerfehler C3737 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3737
dev_langs:
- C++
helpviewer_keywords:
- C3737
ms.assetid: ca2aeb23-2491-4ccb-8838-884abf7065c8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 29d31597e9581d03f97c2b07856ce81c5de50bd3
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3737"></a>Compilerfehler C3737
'Delegat': ein Delegat kann keine explizite Aufrufkonvention  
  
 Sie können nicht angeben, die [Aufrufkonvention](../../cpp/calling-conventions.md) für eine `delegate`.  
  
## <a name="example"></a>Beispiel  
Im folgende Beispiel wird C3737 generiert:  
  
```  
// C3737a.cpp  
// compile with: /clr  
delegate void __stdcall MyFunc();   // C3737  
// Try the following line instead.  
// delegate void MyFunc();  
  
int main() {  
}  
```  
