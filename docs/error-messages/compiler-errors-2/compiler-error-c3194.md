---
title: Compiler-Fehler C3194 generiert | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3194
dev_langs:
- C++
helpviewer_keywords:
- C3194
ms.assetid: 49d3ffc6-eff6-4b46-865b-18811692a8bb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cd6fad304dc4e400d6ca25c7e835b2d0a6935117
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3194"></a>Compiler-Fehler C3194 generiert
'Member': ein Werttyp keinen Zuweisungsoperator  
  
 Spezielle Memberfunktionen, die automatischen Aufruf durch den Compiler, z. B. ein Kopierkonstruktor oder Kopierzuweisungsoperator erfordern werden innerhalb einer Wertklasse nicht unterstützt.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3194 generiert.  
  
```  
// C3194.cpp  
// compile with: /clr /c  
value struct MyStruct {  
   MyStruct& operator= (const MyStruct& i) { return *this; }   // C3194  
};  
  
ref struct MyStruct2 {  
   MyStruct2% operator= (const MyStruct2% i) { return *this; }   // OK  
};  
```