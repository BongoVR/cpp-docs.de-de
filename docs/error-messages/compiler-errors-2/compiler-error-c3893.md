---
title: Compilerfehler C3893 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3893
dev_langs:
- C++
helpviewer_keywords:
- C3893
ms.assetid: 90d52eae-6ef2-4db1-b7ad-92f9e8b140fb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0c95d44a90b9325a492a0f179c941d46ff24030c
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3893"></a>Compilerfehler C3893
"Var": l-Wert-Verwendung von Initonly-Datenmember ist nur zulässig, in einem Instanzenkonstruktor der Klasse "Type_name"  
  
 Statische [Initonly](../../dotnet/initonly-cpp-cli.md) Datenmember dürfen nur über ihre Adresse in einem statischen Konstruktor verfügen.  
  
 Instanz (nicht statische) Initonly-Datenmember können nur in Instanzkonstruktoren (nicht statisch) ihre Adresse haben.  
  
 Im folgende Beispiel wird C3893 generiert:  
  
```  
// C3893.cpp  
// compile with: /clr  
ref struct Y1 {  
   Y1() : data_var(0) {  
      int% i = data_var;   // OK  
   }  
   initonly int data_var;  
};  
  
int main(){  
   Y1^ y= gcnew Y1;  
   int% i = y->data_var;   // C3893  
}  
```