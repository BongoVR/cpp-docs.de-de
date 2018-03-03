---
title: Compilerfehler Fehler C2085 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2085
dev_langs:
- C++
helpviewer_keywords:
- C2085
ms.assetid: 0a86785c-8e6f-481b-8c7b-412220c1950d
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 5834cbca32c2e3bb0c20ab39ee5d3b9d3e8e9c55
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2085"></a>Compilerfehler Fehler C2085
'Bezeichner': nicht in der Liste formaler Parameter  
  
 Der Bezeichner wurde in einer Funktionsdefinition, aber nicht in der Liste formaler Parameter deklariert. (Nur ANSI-C)  
  
 Im folgende Beispiel wird C2085 generiert:  
  
```  
// C2085.c  
void func1( void )  
int main( void ) {}   // C2085  
```  
  
 Mögliche Lösung:  
  
```  
// C2085b.c  
void func1( void );  
int main( void ) {}  
```  
  
 Das Semikolon fehlt, `func1()` einer Funktionsdefinition, nicht um einen Prototyp, deshalb sieht `main` ist definiert in `func1()`, generieren Fehler C2085 für Bezeichner `main`.