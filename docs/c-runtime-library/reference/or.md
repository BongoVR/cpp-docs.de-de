---
title: oder | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- std::or
- std.or
- Or
dev_langs:
- C++
helpviewer_keywords:
- or function
ms.assetid: 6523b3ac-0a18-44ec-9e9a-b9bab8525ead
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f9894d2925f4d1dba03442d5d117a5eb83abfa3a
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="or"></a>oder

Eine Alternative zum &#124;&#124;-Operator.

## <a name="syntax"></a>Syntax

```C

#define or ||

```

## <a name="remarks"></a>Hinweise

Das Makro gibt den Operator &#124;&#124; aus.

## <a name="example"></a>Beispiel

```cpp
// iso646_or.cpp
// compile with: /EHsc
#include <iostream>
#include <iso646.h>

int main( )
{
   using namespace std;
   bool a = true, b = false, result;

   boolalpha(cout);

   result= a || b;
   cout << result << endl;

   result= a or b;
   cout << result << endl;
}
```

```Output
true
true
```

## <a name="requirements"></a>Anforderungen

**Header:** \<iso646.h>