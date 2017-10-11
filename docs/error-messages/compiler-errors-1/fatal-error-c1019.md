---
title: Schwerwiegender Fehler C1019 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C1019
dev_langs:
- C++
helpviewer_keywords:
- C1019
ms.assetid: c4f8968b-bc62-4200-b3ca-69d06c163236
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 90d826ded9ebd8fdc2b304900af523b7ffe8b395
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="fatal-error-c1019"></a>Schwerwiegender Fehler C1019
Unerwartetes #else  
  
 Die `#else` -Direktive befindet sich außerhalb eines `#if`-, `#ifdef`- oder `#ifndef` -Konstrukts. Verwenden Sie `#else` nur innerhalb eines dieser Konstrukte.  
  
 Im folgenden Beispiel wird C1019 generiert:  
  
```  
// C1019.cpp  
#else   // C1019  
#endif  
  
int main() {}  
```  
  
 Mögliche Lösung:  
  
```  
// C1019b.cpp  
#if 1  
#else  
#endif  
  
int main() {}  
```
