---
title: Compilerfehler Fehler C2719 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2719
dev_langs: C++
helpviewer_keywords: C2719
ms.assetid: ea6236d3-8286-45cc-9478-c84ad3dd3c8e
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: f7e6707dfd5666cb8852e3bbf59cf7a81dd24766
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2719"></a>Compilerfehler Fehler C2719
'parameter': formeller Parameter mit __declspec(align('#')) wird nicht ausgerichtet  
  
 Die [ausrichten](../../cpp/align-cpp.md) `__declspec` Modifizierer ist in Funktionsparametern nicht zulässig. Die Funktionsparameterausrichtung wird durch die verwendete Aufrufkonvention gesteuert. Weitere Informationen finden Sie unter [Aufrufkonventionen](../../cpp/calling-conventions.md).  
  
 Im folgenden Beispiel wird C2719 generiert und gezeigt, wie Sie diesen Fehler beheben:  
  
```  
// C2719.cpp  
void func(int __declspec(align(32)) i);   // C2719  
// try the following line instead  
// void func(int i);  
```