---
title: Compilerwarnung (Stufe 4) C4268 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4268
dev_langs:
- C++
helpviewer_keywords:
- C4268
ms.assetid: d0511e80-904f-4ee1-b4d7-39b5c0bd8234
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bef62649af39df950c3966ef93dddb6c71ec2fd6
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4268"></a>Compilerwarnung (Stufe 4) C4268
'Bezeichner': 'const' statischen/globalen Daten vom Compiler generierten Standardkonstruktor initialisiert füllt das Objekt mit Nullen  
  
 Ein **const** globale oder statische Instanz einer Klasse mit nicht trivialen mit einem vom Compiler generierter Standardkonstruktor initialisiert wird.  
  
## <a name="example"></a>Beispiel  
  
```  
// C4268.cpp  
// compile with: /c /LD /W4  
class X {  
public:  
   int m_data;  
};  
  
const X x1;   // C4268  
```  
  
 Wie diese Instanz der Klasse ist **const**, den Wert des `m_data` kann nicht geändert werden.