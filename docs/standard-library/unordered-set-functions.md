---
title: '&lt;unordered_set&gt;-Funktionen | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- unordered_set/std::swap (set)
- unordered_set/std::swap (unordered_multiset)
ms.assetid: 66b35671-4023-4411-ad50-83786580d8ee
ms.openlocfilehash: 515d16cf8b9f11f5e9eb0b9699a0f72a19a64053
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="ltunorderedsetgt-functions"></a>&lt;unordered_set&gt;-Funktionen

|||
|-|-|
|[swap (set)](#swap)|[swap (unordered_multiset)](#swap_unordered_multiset)|

## <a name="swap"></a> swap (unordered_set)

Vertauscht den Inhalt von zwei Containern.

```

template <class Key, class Hash, class Pred, class Alloc>
void swap(
   unordered_set <Key, Hash, Pred, Alloc>& left,
   unordered_set <Key, Hash, Pred, Alloc>& right);
```

### <a name="parameters"></a>Parameter

`Key` Der Schlüsseltyp.

`Hash` Der hashfunktionsobjekttyp.

`Pred` Die Gleichheit-funktionsobjekttyp.

`Alloc` Die Allocator-Klasse.

`left` Der erste zu tauschende Container.

`right` Der zweite zu tauschende Container.

### <a name="remarks"></a>Hinweise

Die Vorlagenfunktion führt `left.`[unordered_set::swap](../standard-library/unordered-set-class.md#swap)`(right)` aus.

### <a name="example"></a>Beispiel

```cpp
#include <unordered_set>
#include <iostream>

typedef std::unordered_set<char> Myset;
int main()
{
Myset c1;

c1.insert('a');
c1.insert('b');
c1.insert('c');

// display contents " [c] [b] [a]"
for (Myset::const_iterator it = c1.begin();
it != c1.end(); ++it)
std::cout << " [" << *it << "]";
std::cout << std::endl;

Myset c2;

c2.insert('d');
c2.insert('e');
c2.insert('f');

c1.swap(c2);

// display contents " [f] [e] [d]"
for (Myset::const_iterator it = c1.begin();
it != c1.end(); ++it)
std::cout << " [" << *it << "]";
std::cout << std::endl;

swap(c1, c2);

// display contents " [c] [b] [a]"
for (Myset::const_iterator it = c1.begin();
it != c1.end(); ++it)
std::cout << " [" << *it << "]";
std::cout << std::endl;

return (0);
}

```

```Output

[c] [b] [a]
[f] [e] [d]
[c] [b] [a]

```

## <a name="swap_unordered_multiset"></a> swap (unordered_multiset)

Vertauscht den Inhalt von zwei Containern.

```

template <class Key, class Hash, class Pred, class Alloc>
void swap(
   unordered_multiset <Key, Hash, Pred, Alloc>& left,
   unordered_multiset <Key, Hash, Pred, Alloc>& right);
```

### <a name="parameters"></a>Parameter

`Key` Der Schlüsseltyp.

`Hash` Der hashfunktionsobjekttyp.

`Pred` Die Gleichheit-funktionsobjekttyp.

`Alloc` Die Allocator-Klasse.

`left` Der erste zu tauschende Container.

`right` Der zweite zu tauschende Container.

### <a name="remarks"></a>Hinweise

Die Vorlagenfunktion führt `left.`[unordered_multiset::swap](../standard-library/unordered-multiset-class.md#swap)`(right)` aus.

### <a name="example"></a>Beispiel

```cpp
// std__unordered_set__u_ms_swap.cpp
// compile with: /EHsc
#include <unordered_set>
#include <iostream>

typedef std::unordered_multiset<char> Myset;
int main()
{
    Myset c1;

    c1.insert('a');
    c1.insert('b');
    c1.insert('c');

    // display contents " [c] [b] [a]"
    for (Myset::const_iterator it = c1.begin();
        it != c1.end(); ++it)
        std::cout << " [" << *it << "]";
    std::cout << std::endl;

    Myset c2;

    c2.insert('d');
    c2.insert('e');
    c2.insert('f');

    c1.swap(c2);

    // display contents " [f] [e] [d]"
    for (Myset::const_iterator it = c1.begin();
        it != c1.end(); ++it)
        std::cout << " [" << *it << "]";
    std::cout << std::endl;

    swap(c1, c2);

    // display contents " [c] [b] [a]"
    for (Myset::const_iterator it = c1.begin();
        it != c1.end(); ++it)
        std::cout << " [" << *it << "]";
    std::cout << std::endl;

    return (0);
}

```

```Output

[c] [b] [a]
[f] [e] [d]
[c] [b] [a]

```

## <a name="see-also"></a>Siehe auch

[<unordered_set>](../standard-library/unordered-set.md)<br/>
