---
title: __alignof-Operator | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- alignas_cpp
- __alignof_cpp
- alignof_cpp
dev_langs:
- C++
helpviewer_keywords:
- alignas [C++]
- alignment of structures
- __alignof keyword [C++]
- alignof [C++]
- types [C++], alignment requirements
ms.assetid: acb1eed7-6398-40bd-b0c5-684ceb64afbc
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 061557b4d017254584e8ddc3da0127f02d352720
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="alignof-operator"></a>__alignof-Operator
C ++ 11 stellt die `alignof` Operator, der die Ausrichtung des angegebenen Typs in Bytes zurückgibt. Zur maximalen Portabilität sollten Sie den „alignof“ des Operators statt des Microsoft-spezifischen „__alignof“-Operators verwenden.  
  
 **Microsoft-spezifisch**  
  
 Gibt einen Wert vom Typ **Size_t** , die die ausrichtungsanforderung des Typs.  
  
## <a name="syntax"></a>Syntax  
  
```  
  __alignof( type )
```  
  
## <a name="remarks"></a>Hinweise  
 Zum Beispiel:  
  
|Ausdruck|Wert|  
|----------------|-----------|  
|**__alignof (Char)**|1|  
|**__alignof (Short)**|2|  
|**__alignof (Int)**|4|  
|**__alignof ( \__int64)**|8|  
|**__alignof( float )**|4|  
|**__alignof (Double)**|8|  
|**__alignof( char\* )**|4|  
  
 Der `__alignof`-Wert entspricht dem `sizeof`-Wert für Basistypen. Betrachten Sie jedoch das Beispiel:  
  
```  
typedef struct { int a; double b; } S;  
// __alignof(S) == 8  
```  
  
 In diesem Fall ist der `__alignof`-Wert die Ausrichtungsanforderung des größten Elements in der Struktur.  
  
 Entsprechend gilt:  
  
```  
typedef __declspec(align(32)) struct { int a; } S;  
```  
  
 `__alignof(S)` ist gleich `32`.  
  
 Eine Verwendung für `__alignof` wäre als Parameter für eine Ihrer Speicherbelegungsroutinen. Beispielsweise könnten Sie angesichts der folgenden definierten Struktur `S` eine Speicherbelegungsroutine mit dem Namen `aligned_malloc` aufrufen, um einen bestimmten Grenzwert mit Speicher zu belegen.  
  
```  
typedef __declspec(align(32)) struct { int a; double b; } S;  
int n = 50; // array size  
S* p = (S*)aligned_malloc(n * sizeof(S), __alignof(S));  
```  
  
 Weitere Informationen über das Ändern der Ausrichtung finden Sie unter:  
  
-   [pack](../preprocessor/pack.md)  
  
-   [align](../cpp/align-cpp.md)  
  
-   [__unaligned](../cpp/unaligned.md)  
  
-   [/Zp (Strukturmemberausrichtung)](../build/reference/zp-struct-member-alignment.md)  
  
-   [Beispiele für die Strukturausrichtung](../build/examples-of-structure-alignment.md) (X64 bestimmte)  
  
 Weitere Informationen zu den Unterschieden bei der Ausrichtung im Code für x86 und x64 finden Sie unter:  
  
-   [Konflikt mit dem x86-Compiler](../build/conflicts-with-the-x86-compiler.md)  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Ausdrücke mit Unäroperatoren](../cpp/expressions-with-unary-operators.md)   
 [Schlüsselwörter](../cpp/keywords-cpp.md)