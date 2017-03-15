---
title: unorm_2-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator+=
- amp_short_vectors/Concurrency::graphics::unnorm_2::y
- amp_short_vectors/Concurrency::graphics::unnorm_2::set_y
- amp_short_vectors/Concurrency::graphics::unnorm_2::x
- amp_short_vectors/Concurrency::graphics::unnorm_2::get_yx
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator--
- amp_short_vectors/Concurrency::graphics::unnorm_2::set_xy
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator*=
- amp_short_vectors/Concurrency::graphics::unnorm_2::xy
- amp_short_vectors/Concurrency::graphics::unnorm_2::get_y
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator=
- amp_short_vectors/Concurrency::graphics::unnorm_2::set_x
- amp_short_vectors/Concurrency::graphics::unnorm_2::rg
- amp_short_vectors/Concurrency::graphics::unorm_2
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator-=
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator/=
- amp_short_vectors/Concurrency::graphics::unnorm_2::get_xy
- amp_short_vectors/Concurrency::graphics::unnorm_2::set_yx
- amp_short_vectors/Concurrency::graphics::unnorm_2::yx
- amp_short_vectors/Concurrency::graphics::unnorm_2::gr
- amp_short_vectors/Concurrency::graphics::unnorm_2::r
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator-
- amp_short_vectors/Concurrency::graphics::unnorm_2::get_x
- amp_short_vectors/Concurrency::graphics::unnorm_2::g
- amp_short_vectors/Concurrency::graphics::unnorm_2::operator++
dev_langs:
- C++
ms.assetid: 62e88ea7-e29f-4f62-95ce-61a1f39f5e34
caps.latest.revision: 11
author: mikeblome
ms.author: mblome
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
translationtype: Machine Translation
ms.sourcegitcommit: fc190feb08d9b221cd1cc21a9c91ad567c86c848
ms.openlocfilehash: 8c4e7cd3040e9d9d6d3c3a5a915118fbc815aebf
ms.lasthandoff: 02/24/2017

---
# <a name="unorm2-class"></a>unorm_2-Klasse
Stellt einen kurzen Vektor aus zwei normalen Zahlen ohne Vorzeichen dar.  
  
## <a name="syntax"></a>Syntax  
  
```  
class unorm_2;  
```  
  
## <a name="members"></a>Mitglieder  
  
### <a name="public-typedefs"></a>Öffentliche Typedefs  
  
|Name|Beschreibung|  
|----------|-----------------|  
|`value_type`||  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[unorm_2-Konstruktor](#ctor)|Überladen. Standardkonstruktor, initialisiert alle Elemente mit 0.|  
  
### <a name="public-methods"></a>Öffentliche Methoden  
  
|Name|Beschreibung|  
|----------|-----------------|  
|unorm_2::get_x-Methode||  
|unorm_2::get_xy-Methode||  
|unorm_2::get_y-Methode||  
|unorm_2::get_yx-Methode||  
|unorm_2::ref_g-Methode||  
|unorm_2::ref_r-Methode||  
|unorm_2::ref_x-Methode||  
|unorm_2::ref_y-Methode||  
|unorm_2::set_x-Methode||  
|unorm_2::set_xy-Methode||  
|unorm_2::set_y-Methode||  
|unorm_2::set_yx-Methode||  
  
### <a name="public-operators"></a>Öffentliche Operatoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|unorm_2::operator-- Operator||  
|unorm_2::operator*=-Operator||  
|unorm_2::operator/=-Operator||  
|unorm_2::operator++-Operator||  
|unorm_2::operator+=-Operator||  
|unorm_2::operator=-Operator||  
|unorm_2::operator-=-Operator||  
  
### <a name="public-constants"></a>Öffentliche Konstanten  
  
|Name|Beschreibung|  
|----------|-----------------|  
|unorm_2::size-Konstante||  
  
### <a name="public-data-members"></a>Öffentliche Datenmember  
  
|Name|Beschreibung|  
|----------|-----------------|  
|unorm_2::g-Datenmember||  
|unorm_2::gr-Datenmember||  
|unorm_2::r-Datenmember||  
|unorm_2::rg-Datenmember||  
|unorm_2::x-Datenmember||  
|unorm_2::xy-Datenmember||  
|unorm_2::y-Datenmember||  
|unorm_2::yx-Datenmember||  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 `unorm_2`  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** amp_short_vectors.h  
  
 **Namespace:** Concurrency:: Graphics  
  
##  <a name="a-namectora-unorm2"></a><a name="ctor"></a>unorm_2 

 Standardkonstruktor, initialisiert alle Elemente mit 0.  
  
```  
unorm_2() restrict(amp,
    cpu);

 
unorm_2(
    unorm _V0,  
    unorm _V1) restrict(amp,
    cpu);

 
unorm_2(
    float _V0,  
    float _V1) restrict(amp,
    cpu);

 
unorm_2(
    unorm _V) restrict(amp,
    cpu);

 
explicit unorm_2(
    float _V) restrict(amp,
    cpu);

 
unorm_2(
    const unorm_2& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_2(
    const uint_2& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_2(
    const int_2& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_2(
    const float_2& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_2(
    const norm_2& _Other) restrict(amp,
    cpu);

 
explicit inline unorm_2(
    const double_2& _Other) restrict(amp,
    cpu);
```  
  
### <a name="parameters"></a>Parameter  
 `_V0`  
 Der Wert 0-Element zu initialisieren.  
  
 `_V1`  
 Der Wert 1 Element initialisiert werden.  
  
 `_V`  
 Der Wert für die Initialisierung.  
  
 `_Other`  
 Das Objekt, das zum Initialisieren verwendet.  
  
##  <a name="a-nameunorm2sizea-size"></a><a name="unorm_2__size"></a>Größe 

```  
static const int size = 2;  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Concurrency:: Graphics-Namespace](concurrency-graphics-namespace.md)

