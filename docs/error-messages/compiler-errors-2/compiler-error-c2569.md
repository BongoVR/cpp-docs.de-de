---
title: Compilerfehler C2569 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2569
dev_langs:
- C++
helpviewer_keywords:
- C2569
ms.assetid: 092bed1e-f631-436c-9586-7750629f6fac
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4869f13d972cea80bd590633b3aae2ea0c96f392
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2569"></a>Compilerfehler C2569
'EnumOderUnion': Enumeration/Union kann nicht als Basisklasse verwendet werden  
  
 Wenn Sie einen Typ aus der angegebenen Union oder Enumeration abgeleitet werden müssen, ändern Sie die Union oder Enumeration zu einer Klasse oder Struktur an.  
  
 Im folgende Beispiel wird C2569 generiert:  
  
```  
// C2569.cpp  
// compile with: /c  
union ubase {};  
class cHasPubUBase : public ubase {};   // C2569  
// OK  
struct sbase {};  
class cHasPubUBase : public sbase {};  
```