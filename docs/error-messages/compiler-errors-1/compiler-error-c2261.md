---
title: Compilerfehler C2261 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2261
dev_langs:
- C++
helpviewer_keywords:
- C2261
ms.assetid: 60969482-9e83-49b5-9631-a04bc844da12
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 45050daf3149cd813fb23b5814be5fe49c375f03
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2261"></a>Compilerfehler C2261
"Zeichenfolge": Assemblyverweis ist ungültig und kann nicht aufgelöst werden  
  
 Ein Wert war ungültig.  
  
 <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> Dient zum Angeben einer Friend-Assembly. Z. B. wenn a.dll b.dll als Friend-Assembly angeben möchte, würden Sie angeben (in a.dll): InternalsVisibleTo("b"). Der Laufzeit ermöglicht dann b.dll auf alles in a.dll (mit Ausnahme der private Typen).  
  
 Weitere Informationen über die richtige Syntax beim Angeben von Friend-Assemblys finden Sie unter [Friend-Assemblys (C++)](../../dotnet/friend-assemblies-cpp.md).  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C2261 generiert.  
  
```  
// C2261.cpp  
// compile with: /clr /c  
using namespace System::Runtime::CompilerServices;  
[assembly: InternalsVisibleTo("a,a,a")];   // C2261  
[assembly: InternalsVisibleTo("a.a")];   // OK  
[assembly: InternalsVisibleTo("a")];   // OK  
```