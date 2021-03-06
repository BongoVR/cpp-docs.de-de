---
title: Compilerfehler C3540 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3540
dev_langs:
- C++
helpviewer_keywords:
- C3540
ms.assetid: 3c0c959c-e3b7-40eb-b922-ccac44bd9d85
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 27bae73d387612be41d8462bf0e5e0d82516ba1a
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3540"></a>Compilerfehler C3540
"Typ": "sizeof" kann nicht angewendet werden, um ein Typ, der "auto" enthält  
  
 Die ["sizeof"](../../cpp/sizeof-operator.md) Operator kann nicht auf den angegebenen Typ angewendet werden, da sie enthält die `auto` Spezifizierer.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3540 ergeben.  
  
```  
// C3540.cpp  
// Compile with /Zc:auto  
int main() {  
    auto x = 123;  
    sizeof(x);    // OK  
    sizeof(auto); // C3540  
    return 0;  
}  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Auto-Schlüsselwort](../../cpp/auto-keyword.md)   
 [/ Zc: Auto (Variablentyp ableiten)](../../build/reference/zc-auto-deduce-variable-type.md)   
 [sizeof-Operator](../../cpp/sizeof-operator.md)