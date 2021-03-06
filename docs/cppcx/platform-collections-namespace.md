---
title: 'Platform:: Collections-Namespace | Microsoft Docs'
ms.custom: ''
ms.date: 01/18/2018
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- collection/Platform::Collections
dev_langs:
- C++
helpviewer_keywords:
- Platform::Collections Namespace
ms.assetid: b5042864-5f22-40b7-b7a5-c0691f65cc47
author: ghogen
ms.author: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 2b4e38d6a051481b2b5f642c6b4de3c837f8fbfd
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="platformcollections-namespace"></a>Platform::Collections-Namespace

Platform:: Collections-Namespace enthält die `Map`, `MapView`, `Vector`, und `VectorView` Klassen. Diese Klassen sind konkrete Implementierungen der entsprechenden Schnittstellen, die im Namespace [Windows::Foundation::Collections](http://go.microsoft.com/fwlink/p/?LinkId=262645) definiert sind. Die konkreten Auflistungstypen können nicht über die ABI hinweg portiert werden (z. B. beim Aufruf eines Javascript- oder C#-Programms in eine C++-Komponente). Sie sind allerdings implizit in ihre entsprechenden Schnittstellentypen konvertierbar. Wenn Sie z. B. eine öffentliche Methode implementieren, die eine Auflistung füllt und zurückgibt, verwenden Sie [Platform::Collections::Vector](../cppcx/platform-collections-vector-class.md) , um die Auflistung intern zu implementieren. Verwenden Sie [Windows::Foundation::Collections::IVector](http://go.microsoft.com/fwlink/p/?LinkId=262410) als Rückgabetyp. Weitere Informationen finden Sie unter [Sammlungen](../cppcx/collections-c-cx.md) und [Erstellen von Windows-Runtime-Komponenten in C++](/windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp).

Sie können Platform::Collections::Vector aus [std::vector](../standard-library/vector-class.md) und [Platform::Collections::Map](../cppcx/platform-collections-map-class.md) aus [std::map](../standard-library/map-class.md)erstellen.

Darüber hinaus bietet der Namespace Platform:: Collections Unterstützung für und eingabeiteratoren, und `Vector` und `VectorView` Iteratoren.

Sie müssen einschließen (`#include`) den Header "Collection.h", um die Typen im Namespace Platform:: Collections zu verwenden.

## <a name="syntax"></a>Syntax

```cpp
#include <collection.h>
using namespace Platform::Collections;
```

### <a name="members"></a>Member

Dieser Namespace enthält die folgenden Member.

|name|Beschreibung|
|----------|-----------------|
|[Platform::Collections::BackInsertIterator-Klasse](../cppcx/platform-collections-backinsertiterator-class.md)|Stellt einen Iterator dar, der ein Element am Ende einer Auflistung einfügt.|
|[Platform::Collections::InputIterator-Klasse](../cppcx/platform-collections-inputiterator-class.md)|Stellt einen Iterator dar, der ein Element am Anfang einer Auflistung einfügt.|
|[Platform::Collections::Map-Klasse](../cppcx/platform-collections-map-class.md)|Stellt eine änderbare Auflistung von Schlüssel-Wert-Paaren dar, auf die über einen Schlüssel zugegriffen wird. Wie bei [std::map](../standard-library/map-class.md).|
|[Platform::Collections::MapView-Klasse](../cppcx/platform-collections-mapview-class.md)|Stellt eine schreibgeschützte Auflistung von Schlüssel-Wert-Paaren dar, auf die über einen Schlüssel zugegriffen wird.|
|[Platform::Collections::Vector Class](../cppcx/platform-collections-vector-class.md)|Stellt eine änderbare Sequenz von Elementen dar. Wie bei [std::vector](../standard-library/vector-class.md).|
|[Platform::Collections::VectorIterator-Klasse](../cppcx/platform-collections-vectoriterator-class.md)|Stellt einen Iterator dar, der eine `Vector` -Auflistung durchläuft.|
|[Platform::Collections::VectorView-Klasse](../cppcx/platform-collections-vectorview-class.md)|Stellt eine schreibgeschützte Sequenz von Elementen dar.|
|[Platform::Collections::VectorViewIterator-Klasse](../cppcx/platform-collections-vectorviewiterator-class.md)|Stellt einen Iterator dar, der eine `VectorView` -Auflistung durchläuft.|

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[Plattformnamespace](../cppcx/platform-namespace-c-cx.md)

### <a name="requirements"></a>Anforderungen

**Metadaten:** platform.winmd

**Namespace:** Platform::Collections

**Compileroption:** /ZW

## <a name="see-also"></a>Siehe auch

[Platform-Namespace](../cppcx/platform-namespace-c-cx.md)  
