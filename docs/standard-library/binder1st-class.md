---
title: binder1st-Klasse | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- xfunctional/std::binder1st
dev_langs:
- C++
helpviewer_keywords:
- binder1st class
ms.assetid: 6b8ee343-c82f-48f8-867d-06f9d1d324c0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 55f000ea8458925f8ea3faa4896943e045de127d
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="binder1st-class"></a>binder1st-Klasse

Eine Vorlagenklasse, mit der ein Konstruktor bereitgestellt wird, der ein binäres Funktionsobjekt in ein unäres Funktionsobjekt konvertiert, indem das erste Argument der binären Funktion an einen angegebenen Wert gebunden wird.

## <a name="syntax"></a>Syntax

```cpp
template <class Operation>
class binder1st
    : public unaryFunction <typename Operation::second_argument_type,
                             typename Operation::result_type>
{
public:
    typedef typename Operation::argument_type argument_type;
    typedef typename Operation::result_type result_type;
    binder1st(
        const Operation& Func,
        const typename Operation::first_argument_type& left);

    result_type operator()(const argument_type& right) const;
    result_type operator()(const argument_type& right) const;

protected:
    Operation op;
    typename Operation::first_argument_type value;
};
```

### <a name="parameters"></a>Parameter

`Func` Der binäres Funktionsobjekt in ein unäres Funktionsobjekt konvertiert werden.

`left` Der Wert, der das erste Argument der binären Funktion-Objekts gebunden werden.

`right` Der Wert des Arguments, das angepasste binary Object mit der feste Wert des zweiten Arguments verglichen werden soll.

## <a name="return-value"></a>Rückgabewert

Das unäre Funktionsobjekt, das aus dem Binden des ersten Arguments des binären Funktionsobjekts an den Wert `left.` resultiert

## <a name="remarks"></a>Hinweise

Die Vorlagenklasse speichert eine Kopie eines binären Funktionsobjekts `Func` in **op** und eine Kopie von `left` in **value**. Für seine Memberfunktion `operator()` definiert sie den Rückgabewert **op**( **value**, `right`).

Wenn `Func` ein Objekt vom Typ **Operation** und `c` eine Konstante ist, dann entspricht [bind1st](../standard-library/functional-functions.md#bind1st) ( `Func`, `c` ) dem `binder1st`-Klassenkonstruktor `binder1st`\< **Operation**> ( `Func`, `c` ) und ist komfortabler.

## <a name="example"></a>Beispiel

```cpp
// functional_binder1st.cpp
// compile with: /EHsc
#include <vector>
#include <functional>
#include <algorithm>
#include <iostream>

using namespace std;

int main()
{
    vector<int> v1;
    vector<int>::iterator Iter;

    int i;
    for (i = 0; i <= 5; i++)
    {
        v1.push_back(5 * i);
    }

    cout << "The vector v1 = ( ";
    for (Iter = v1.begin(); Iter != v1.end(); Iter++)
        cout << *Iter << " ";
    cout << ")" << endl;

    // Count the number of integers > 10 in the vector
    vector<int>::iterator::difference_type result1;
    result1 = count_if(v1.begin(), v1.end(),
        binder1st<less<int> >(less<int>(), 10));
    cout << "The number of elements in v1 greater than 10 is: "
         << result1 << "." << endl;

    // Compare use of binder2nd fixing 2nd argument:
    // count the number of integers < 10 in the vector
    vector<int>::iterator::difference_type result2;
    result2 = count_if(v1.begin(), v1.end(),
        binder2nd<less<int> >(less<int>(), 10));
    cout << "The number of elements in v1 less than 10 is: "
         << result2 << "." << endl;
}
\* Output:
The vector v1 = ( 0 5 10 15 20 25 )
The number of elements in v1 greater than 10 is: 3.
The number of elements in v1 less than 10 is: 2.
*\
```

## <a name="requirements"></a>Anforderungen

**Header:** \<functional>

**Namespace:** std

## <a name="see-also"></a>Siehe auch

[Threadsicherheit in der C++-Standardbibliothek](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
[C++-Standardbibliotheksreferenz](../standard-library/cpp-standard-library-reference.md)<br/>
