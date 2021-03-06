---
title: 'Platform:: arrayreference-Klasse | Microsoft Docs'
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::ArrayReference::ArrayReference
dev_langs:
- C++
helpviewer_keywords:
- Platform::ArrayReference Class
ms.assetid: 9ab3b15e-8a60-4600-8fcb-7d6c86284f4b
author: ghogen
ms.author: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: c8e4183c400cf45a23f24a98292b68f6df537da1
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="platformarrayreference-class"></a>Platform::ArrayReference-Klasse
`ArrayReference` ist ein Optimierungstyp, den Sie als Ersatz für [Platform::Array^](../cppcx/platform-array-class.md) in den Eingabeparametern verwenden können, wenn Sie ein Array im C-Format mit Eingabedaten füllen möchten.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
class ArrayReference  
```
  
### <a name="members"></a>Member  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[Arrayreference:: Arrayreference](#ctor)|Initialisiert eine neue Instanz der `ArrayReference`-Klasse.|  
  
### <a name="public-operators"></a>Öffentliche Operatoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[ArrayReference::operator()-Operator](#operator-call)|Konvertiert diesen `ArrayReference` in ein `Platform::Array<T>^*`-Element.|  
|[ArrayReference::operator=-Operator](#operator-assign)|Weist dieser Instanz den Inhalt von einem anderen `ArrayReference` zu.|  
  
## <a name="exceptions"></a>Ausnahmen  
  
### <a name="remarks"></a>Hinweise  
 Mit `ArrayReference` zum Auffüllen eines Arrays im C-Format, vermeiden Sie den zusätzlichen Kopiervorgang, der dadurch aufgerufen würde, zunächst in eine `Platform::Array` -Variable zu kopieren, und dann in einem zweiten Schritt in das Array im C-Format. Bei Verwendung von `ArrayReference`, entsteht nur ein Kopiervorgang. Ein Codebeispiel finden Sie unter [Array und WriteOnlyArray](../cppcx/array-and-writeonlyarray-c-cx.md).  
  
### <a name="requirements"></a>Anforderungen  
 **Unterstützter Client:** Windows 8  
  
 **Unterstützter Server:** Windows Server 2012  
  
 **Namespace:** Platform  
  
 **Header:** vccorlib.h  
  
## <a name="ctor"></a>  Arrayreference:: Arrayreference-Konstruktor
Initialisiert eine neue Instanz der dem [arrayreference](../cppcx/platform-arrayreference-class.md) Klasse.  
  
### <a name="syntax"></a>Syntax  
  
```cpp  
ArrayReference(TArg* ataArg, unsigned int sizeArg, bool needsInitArg = false);  
ArrayReference(ArrayReference&& otherArg)  
  
```  
  
### <a name="parameters"></a>Parameter  
 `dataArg`  
 Ein Zeiger auf die Arraydaten.  
  
 `sizeArg`  
 Die Anzahl von Elementen im Quellarray.  
  
 `otherArg`  
 Ein `ArrayReference`-Objekt, dessen Daten zum Initialisieren der neuen Instanz verschoben werden.  
  
### <a name="remarks"></a>Hinweise  
  


## <a name="operator-assign"></a>  Arrayreference:: Operator =-Operator
Weist das angegebene Objekt dem aktuellen [arrayreference](../cppcx/platform-arrayreference-class.md) -Objekt unter Verwendung der Verschiebesemantik.  
  
### <a name="syntax"></a>Syntax  
  
```cpp  
  
ArrayReference& operator=(ArrayReference&& otherArg);  
  
```  
  
### <a name="parameters"></a>Parameter  
 `otherArg`  
 Das zum aktuellen `ArrayReference`-Objekt verschobene Objekt.  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Verweis auf ein Objekt des Typs `ArrayReference`.  
  
### <a name="remarks"></a>Hinweise  
 `Platform::ArrayReference` ist eine Standard-C++-Klassenvorlage, keine Verweisklasse.  
  


## <a name="operator-call"></a>  Arrayreference::Operator()-Operator
Konvertiert das aktuelle [arrayreference](../cppcx/platform-arrayreference-class.md) -Objekt an eine [Platform:: Array](../cppcx/platform-array-class.md) Klasse.  
  
### <a name="syntax"></a>Syntax  
  
```cpp  
  
Array<TArg>^ operator ();  
  
```  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Handle für das Objekt des Typs `Array<TArg>^`  
  
### <a name="remarks"></a>Hinweise  
 [Platform:: arrayreference](../cppcx/platform-arrayreference-class.md) und [Platform:: Array](../cppcx/platform-array-class.md) sind Standard-c++-Klassenvorlagen, keine Verweisklassen Klassen.  
  


  
  
## <a name="see-also"></a>Siehe auch  
 [Plattformnamespace](../cppcx/platform-namespace-c-cx.md)