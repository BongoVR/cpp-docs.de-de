---
title: Compilerwarnung (Stufe 4) C4057 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4057
dev_langs:
- C++
helpviewer_keywords:
- C4057
ms.assetid: e75d0645-84c9-4bef-a812-942ed9879aa3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3217ccb0a96fbe02e152ff82dedeb7e8e54b89ea
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4057"></a>Compilerwarnung (Stufe 4) C4057
'Operator': 'Bezeichner1' Dereferenzierung in leicht unterschiedliche Basistypen von 'Bezeichner2'  
  
 Zwei Zeigerausdrücke verweisen auf unterschiedliche Basistypen. Die Ausdrücke werden ohne Konvertierung verwendet.  
  
### <a name="to-fix-by-checking-the-following-possible-causes"></a>Dieser Fehler kann eine der folgenden Ursachen haben:  
  
1.  Typen mit und ohne Vorzeichen werden gemischt verwendet.  
  
2.  **short** - und **long** -Typen werden gemischt verwendet.