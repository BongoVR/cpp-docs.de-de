---
title: Compilerfehler C2212 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2212
dev_langs:
- C++
helpviewer_keywords:
- C2212
ms.assetid: 3fdab304-272c-4d07-bfd4-fad75170e536
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 152b38be30b50684684bb0c2c39a035b748915b6
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2212"></a>Compilerfehler C2212
'Bezeichner': __based ist nicht verfügbar für Zeiger auf Funktionen  
  
 Zeiger auf Funktionen können nicht deklariert werden `__based`. Wenn Sie Code basierende Daten benötigen, verwenden Sie die `__declspec` Schlüsselwort oder der `data_seg` Pragma.