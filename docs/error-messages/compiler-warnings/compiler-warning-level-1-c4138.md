---
title: Compilerwarnung (Stufe 1) C4138 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4138
dev_langs:
- C++
helpviewer_keywords:
- C4138
ms.assetid: 65ebf929-bba0-4237-923b-c1b66adfe17d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f0865935c30c4934684c7a12e50ab26f3e8b12c4
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4138"></a>Compilerwarnung (Stufe 1) C4138
"*/" wurde außerhalb des Kommentars gefunden  
  
 Dem schließenden Kommentartrennzeichen geht kein öffnendes Kommentartrennzeichen voran. Der Compiler nimmt an, dass zwischen dem Sternchen (**\****) und dem Schrägstrich (/) ein Leerzeichen steht.  
  
## <a name="example"></a>Beispiel  
  
```  
// C4138a.cpp  
// compile with: /W1  
int */*comment*/ptr;   // C4138 Ambiguous first delimiter causes warning  
int main()  
{  
}  
```  
  
 Diese Warnung kann auf den Versuch zurückzuführen sein, Kommentare zu schachteln.  
  
 Die Warnung kann behoben werden, wenn Sie Codeabschnitte, die Kommentare enthalten, auskommentieren, den Code in einen **#if/#endif** -Block einschließen und den steuernden Ausdruck auf 0 (null) festlegen:  
  
```  
// C4138b.cpp  
// compile with: /W1  
#if 0  
int my_variable;   /* Declaration currently not needed */  
#endif  
int main()  
{  
}  
```