---
title: Compilerwarnung (Stufe 4) C4960 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4960
dev_langs:
- C++
helpviewer_keywords:
- C4960
ms.assetid: 3b4ed286-9e8d-46f1-af0c-00ba669693a9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1281bc86ad363c02df5c39ed41f616a6fff1a9b3
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4960"></a>Compilerwarnung (Stufe 4) C4960
"function" ist zu groß, um ein Profil zu erstellen  
  
 Bei Verwendung von [/LTCG:PGOPTIMIZE](../../build/reference/ltcg-link-time-code-generation.md)hat der Compiler ein Eingabemodul mit einer Funktion mit mehr als 65.535 Anweisungen erkannt. Eine so große Funktion ist für profilgesteuerte Optimierungen nicht verfügbar.  
  
 Verkleinern Sie die Funktion, um die Warnung aufzuheben.