---
title: Compilerfehler C2530 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2530
dev_langs:
- C++
helpviewer_keywords:
- C2530
ms.assetid: b790a312-48df-4a6a-9e27-be2c5f32f16c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9b226ef5ca0e839c745e13d4118264a69ca408db
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2530"></a>Compilerfehler C2530
'Bezeichner': Verweise müssen initialisiert werden  
  
 Sie müssen einen Verweis initialisieren, wenn es deklariert wurde, es sei denn, es bereits deklariert ist:  
  
-   Mit dem Schlüsselwort ["extern"](../../cpp/using-extern-to-specify-linkage.md).  
  
-   Als Mitglied einer Klasse, Struktur oder Union (und er wird im Konstruktor initialisiert).  
  
-   Als Parameter in einer Deklaration oder Definition.  
  
-   Als Rückgabetyp einer Funktion.  
  
 Im folgende Beispiel wird C2530 generiert:  
  
```  
// C2530.cpp  
int main() {  
   int i = 0;  
   int &j;   // C2530  
   int &k = i;   // OK  
}  
```