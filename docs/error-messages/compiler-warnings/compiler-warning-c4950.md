---
title: Compiler-Warnung C4950 | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4950
dev_langs:
- C++
helpviewer_keywords:
- C4950
ms.assetid: 50226a5c-c664-4d09-ac59-e9e874ca244f
caps.latest.revision: 11
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 4ac033535632e94a365aa8dafd849f2ab28a3af7
ms.openlocfilehash: 937510b3fadf3dd2aff81defc08ea2c74b8b7dec
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-warning-c4950"></a>Compilerwarnung C4950
'type_or_member': als veraltet markiert.  
  
Ein Member oder Typ wurde mit als veraltet markiert die <xref:System.ObsoleteAttribute>Attribut.</xref:System.ObsoleteAttribute>  
  
C4950 wird immer als Fehler ausgegeben. Sie können diese Warnung deaktivieren, mit der [Warnung](../../preprocessor/warning.md) Pragma-Direktive oder [/WD](../../build/reference/compiler-option-warning-level.md) (Compileroption).  
  
## <a name="example"></a>Beispiel  
Im folgenden Beispiel wird C4950 generiert.  
  
```cpp  
// C4950.cpp  
// compile with: /clr  
using namespace System;  
  
// Any reference to Func3 should generate an error with message  
[System::ObsoleteAttribute("Will be removed in next version", true)]  
Int32 Func3(Int32 a, Int32 b) {  
   return (a + b);  
}  
  
int main() {  
   Int32 MyInt3 = ::Func3(2, 2);   // C4950  
}  
```
