---
title: Compiler-Fehler C3272 | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3272
dev_langs:
- C++
helpviewer_keywords:
- C3272
ms.assetid: 7cdf254d-f207-4116-a1bf-7386f3b82a6f
caps.latest.revision: 8
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
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: a5d67c0228158e13090204954d8346e6656b4065
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3272"></a>Compilerfehler C3272
"Symbol": Symbol erfordert "FieldOffset", da es ein Member des Typs "Typname" ist, der mit "StructLayout(LayoutKind::Explicit)" definiert wurde.  
  
Wenn `StructLayout(LayoutKind::Explicit)` gültig ist, Felder müssen mit `FieldOffset`.  
  
Im folgenden Beispiel wird C3272 generiert:  
  
```  
// C3272_2.cpp  
// compile with: /clr /c  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
[StructLayout(LayoutKind::Explicit)]  
ref struct X  
{  
   int data_;   // C3272  
   // try the following line instead  
   // [FieldOffset(0)] int data_;  
};  
```  

