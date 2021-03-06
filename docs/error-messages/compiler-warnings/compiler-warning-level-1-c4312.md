---
title: Compilerwarnung (Stufe 1) C4312 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4312
dev_langs:
- C++
helpviewer_keywords:
- C4312
ms.assetid: 541906ed-4f62-4bcb-947f-cf9ae7411bcb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 18039e44a5616330c66603e448bcafd6d18ff7aa
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4312"></a>Compilerwarnung (Stufe 1) C4312
'Operation': Konvertierung von 'Typ1' in größeren Typ 'Typ2'  
  
 Diese Warnung erkennt den Versuch, einen 32-Bit-Wert einem 64-Bit-Zeigertyp zuzuweisen, z. B. die Umwandlung eines 32-Bit-`int` oder `long` in einen 64-Bit-Zeiger.  
  
 Dabei kann es sich um eine unsichere Konvertierung auch für Zeigerwerte handeln, die in 32 Bits passen, wenn die Vorzeichenerweiterung vorhanden ist. Wenn eine negative 32-Bit-Ganzzahl einem 64-Bit-Zeigertyp zugeordnet wird, verweist der Zeigerwert aufgrund der Vorzeichenerweiterung auf eine Speicheradresse, die sich vom Wert der Ganzzahl unterscheidet.  
  
 Diese Warnung wird nur für 64-Bit-Kompilierungsziele ausgegeben. Weitere Informationen finden Sie unter [Regeln für die Verwendung von Zeigern](http://msdn.microsoft.com/library/windows/desktop/aa384242).  
  
 Im folgenden Codebeispiel wird C4312 generiert, wenn dies für 64-Bit-Ziele kompiliert wird:  
  
```  
// C4312.cpp  
// compile by using: cl /W1 /LD C4312.cpp  
void* f(int i) {  
   return (void*)i;   // C4312 for 64-bit targets  
}  
  
void* f2(__int64 i) {  
   return (void*)i;   // OK  
}  
```