---
title: Compilerwarnung (Stufe 1) C4025 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4025
dev_langs:
- C++
helpviewer_keywords:
- C4025
ms.assetid: c4f6a651-0641-4446-973e-8290065e49ad
caps.latest.revision: 6
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
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 72fbde1b05136da89ddc69ffa3891b4fd724cd1b
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4025"></a>Compilerwarnung (Stufe 1) C4025
"Anzahl": Zeiger auf ein separates Segment an Funktion mit variablen Argumenten übergeben: Parameteranzahl  
  
 Die Übergabe eines basierten Zeigers an eine Funktion mit variablen Argumenten bewirkt, dass der Zeiger normalisiert wird. Dies kann unvorhersehbare Folgen haben. Übergeben Sie keine basierten Zeiger an Funktionen mit variablen Argumenten.
