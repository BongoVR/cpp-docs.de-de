---
title: Datentypkonstanten| Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- FLT_MIN
- SHRT_MAX
- CHAR_MIN
- MB_LEN_MAX
- DBL_EPSILON
- SHRT_MIN
- _FLT_RADIX
- FLT_DIG
- FLT_MAX_10_EXP
- FLT_MANT_DIG
- DBL_MAX_EXP
- SCHAR_MIN
- SCHAR_MAX
- DBL_MIN
- FLT_MIN_10_EXP
- _DBL_ROUNDS
- USHRT_MAX
- FLT_MAX_EXP
- LONG_MAX
- DBL_MAX
- DBL_DIG
- FLT_MIN_EXP
- INT_MIN
- DBL_MIN_10_EXP
- CHAR_BIT
- INT_MAX
- ULONG_MAX
- DBL_MIN_EXP
- LONG_MIN
- _FLT_ROUNDS
- DBL_MANT_DIG
- _DBL_RADIX
- CHAR_MAX
- FLT_MAX
- DBL_MAX_10_EXP
- UCHAR_MAX
- FLT_EPSILON
- UINT_MAX
dev_langs:
- C++
helpviewer_keywords:
- DBL_MAX_EXP constant
- _DBL_RADIX constant
- FLT_MIN_EXP constant
- DBL_EPSILON constant
- INT_MIN constant
- FLT_EPSILON constant
- DBL_MANT_DIG constant
- _FLT_RADIX constant
- DBL_MIN constant
- USHRT_MAX constant
- FLT_MAX_10_EXP constant
- _FLT_ROUNDS constant
- data type constants [C++]
- _DBL_ROUNDS constant
- CHAR_MAX constant
- FLT_MAX_EXP constant
- FLT_MIN constant
- CHAR_MIN constant
- FLT_MIN_10_EXP constant
- DBL_MIN_EXP constant
- SCHAR_MAX constant
- FLT_RADIX constant
- CHAR_BIT constant
- UCHAR_MAX constant
- DBL_RADIX constant
- FLT_ROUNDS constant
- LONG_MIN constant
- SHRT_MAX constant
- LONG_MAX constant
- DBL_MAX_10_EXP constant
- DBL_MIN_10_EXP constant
- INT_MAX constant
- constants [C++], data type
- ULONG_MAX constant
- FLT_DIG constant
- MB_LEN_MAX constant
- DBL_DIG constant
- SHRT_MIN constant
- DBL_MAX constant
- DBL_ROUNDS constant
- FLT_MAX constant
- UINT_MAX constant
- FLT_MANT_DIG constant
- SCHAR_MIN constant
ms.assetid: c0f1c405-0465-41d5-b5ff-e81cdb6f1622
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Human Translation
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: a33c5071549695c11ba4820679d5d7059b7f5a5c
ms.lasthandoff: 04/01/2017

---
# <a name="data-type-constants"></a>Datentypkonstanten
Datentypkonstanten sind von der Implementierung abhängige Wertbereiche, die für integrale Datentypen zulässig sind. Die unten aufgelisteten Konstanten geben die Bereiche für die integralen Datentypen an und sind in „limits.h“ definiert.  
  
> [!NOTE]
>  Die /J-Compileroption ändert den Standard von `char` in `unsigned`.  
  
|Konstante|Wert|Bedeutung|  
|--------------|-----------|-------------|  
|**SCHAR_MAX**|127|Der Höchstwert von `char` mit Vorzeichen|  
|**SCHAR_MIN**|-128|Der Mindestwert von `char` mit Vorzeichen|  
|**UCHAR_MAX**|255 (0xff)|Höchstwert von `unsigned char`|  
|**CHAR_BIT**|8|Die Anzahl der Bits in einem `char`|  
|**USHRT_MAX**|65535 (0xffff)|Der Höchstwert von **unsigned short**|  
|**SHRT_MAX**|32767|Der Höchstwert von **short** (mit Vorzeichen)|  
|**SHRT_MIN**|-32768|Der Mindestwert von **short** (mit Vorzeichen)|  
|**UINT_MAX**|4294967295 (0xffffffff)|Der Höchstwert von `unsigned int`|  
|**ULONG_MAX**|4294967295 (0xffffffff)|Der Höchstwert von `unsigned long`|  
|**INT_MAX**|2147483647|Der Höchstwert von `int` (mit Vorzeichen)|  
|**INT_MIN**|-2147483647-1|Der Mindestwert von `int` (mit Vorzeichen)|  
|**LONG_MAX**|2147483647|Der Höchstwert von **long** (mit Vorzeichen)|  
|**LONG_MIN**|-2147483647-1|Der Mindestwert von **long** (mit Vorzeichen)|  
|**CHAR_MAX**|127 (255 bei Verwendung der /J-Option)|Höchstwert von `char`|  
|**CHAR_MIN**|-128 (0 bei Verwendung der /J-Option)|Mindestwert von `char`|  
|**MB_LEN_MAX**|2|Die maximale Anzahl der Bytes in `char` in Multibyte|  
|**_I64_MAX**|9223372036854775807|Der Höchstwert von _**int64** (mit Vorzeichen)|  
|**_I64_MIN**|-9223372036854775807-1|Der Mindestwert von _**int64** (mit Vorzeichen)|  
|**_UI64_MAX**|0xffffffffffffffff|Der Höchstwert von _**int64** (ohne Vorzeichen)|  
  
 Folgende Konstanten geben den Bereich und andere Merkmale der Datentypen **double** und **float** an, die in „float.h“ definiert sind:  
  
|Konstante|Wert|Beschreibung|  
|--------------|-----------|-----------------|  
|**DBL_DIG**|15|# Anzahl der Dezimalstellen der Genauigkeit|  
|**DBL_EPSILON**|2.2204460492503131e-016|Am kleinsten, derart, dass 1.0+**DBL_EPSILON** !=1.0|  
|**DBL_MANT_DIG**|53|# Anzahl der Bits der Mantisse|  
|**DBL_MAX**|1.7976931348623158e+308|Maximalwert|  
|**DBL_MAX_10_EXP**|308|Der höchstmögliche dezimale Exponent|  
|**DBL_MAX_EXP**|1024|Der höchstmögliche binäre Exponent|  
|**DBL_MIN**|2.2250738585072014e-308|Der positive Mindestwert|  
|**DBL_MIN_10_EXP**|(-307)|Der dezimale Mindestwert|  
|**DBL_MIN_EXP**|(-1021)|Der binäre Mindestwert|  
|**_DBL_RADIX**|2|Die Exponentenbasis|  
|**_DBL_ROUNDS**|1|Runden der Addition: nah|  
|**FLT_DIG**|6|Anzahl der Dezimalstellen der Genauigkeit|  
|**FLT_EPSILON**|1.192092896e-07F|Am kleinsten, derart, dass 1.0+**FLT_EPSILON** !=1.0|  
|**FLT_MANT_DIG**|24|Anzahl der Bits der Mantisse|  
|**FLT_MAX**|3.402823466e+38F|Maximalwert|  
|**FLT_MAX_10_EXP**|38|Der höchstmögliche dezimale Exponent|  
|**FLT_MAX_EXP**|128|Der höchstmögliche binäre Exponent|  
|**FLT_MIN**|1.175494351e-38F|Der positive Mindestwert|  
|**FLT_MIN_10_EXP**|(-37)|Der dezimale Mindestwert|  
|**FLT_MIN_EXP**|(-125)|Der binäre Mindestwert|  
|**FLT_RADIX**|2|Die Exponentenbasis|  
|**FLT_ROUNDS**|1|Runden der Addition: nah|  
  
## <a name="see-also"></a>Siehe auch  
 [Globale Konstanten](../c-runtime-library/global-constants.md)
