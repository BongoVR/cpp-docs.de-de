---
title: binder2nd-Klasse | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: xfunctional/std::binder2nd
dev_langs: C++
helpviewer_keywords: binder2nd class
ms.assetid: b2a9c1d1-dfc4-4ca9-a10e-ae84e195a62d
caps.latest.revision: "22"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 2426298a05542bb0e68fa8c068adea71f630814d
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="binder2nd-class"></a>binder2nd-Klasse
Eine Vorlagenklasse, mit der ein Konstruktor bereitgestellt wird, der ein binäres Funktionsobjekt in ein unäres Funktionsobjekt konvertiert, indem das zweite Argument der binären Funktion an einen angegebenen Wert gebunden wird.  
  
## <a name="syntax"></a>Syntax  
  
```
template <class Operation>
class binder2nd
    : public unaryFunction <typename Operation::first_argument_type,
    typename Operation::result_type>
{
public:
    typedef typename Operation::argument_type argument_type;
    typedef typename Operation::result_type result_type;
    binder2nd(
        const Operation& Func,
        const typename Operation::second_argument_type& right);

    result_type operator()(const argument_type& left) const;
    result_type operator()(argument_type& left) const;

protected:
    Operation op;
    typename Operation::second_argument_type value;
};
```  
  
#### <a name="parameters"></a>Parameter  
 `Func`  
 Das binäre Funktionsobjekt, das in ein unäres Funktionsobjekt konvertiert werden soll.  
  
 `right`  
 Der Wert, an den das zweite Argument des binären Funktionsobjekts gebunden werden soll.  
  
 `left`  
 Der Wert des Arguments, den das angepasste binäre Objekt mit dem festen Wert des zweiten Arguments vergleicht.  
  
## <a name="return-value"></a>Rückgabewert  
 Das unäre Funktionsobjekt, das aus dem Binden des zweiten Arguments des binären Funktionsobjekts an den Wert `right.` resultiert  
  
## <a name="remarks"></a>Hinweise  
 Die Vorlagenklasse speichert eine Kopie eines binären Funktionsobjekts _ *Func* in **op** und eine Kopie von `right` in **value**. Für seine Memberfunktion `operator()` definiert sie die Rückgabe **op**( `left`, **value**).  
  
 Wenn `Func` ein Objekt vom Typ **Operation** und c eine Konstante ist, dann entspricht [bind2nd](../standard-library/functional-functions.md#bind2nd) ( `Func`, `c` ) dem `binder2nd`-Klassenkonstruktor `binder2nd`\< **Operation**> ( `Func`, `c` ) und ist komfortabler.  
  
## <a name="example"></a>Beispiel  
  
```cpp  
// functional_binder2nd.cpp  
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
        binder2nd<greater<int> >(greater<int>(), 10));  
    cout << "The number of elements in v1 greater than 10 is: "  
         << result1 << "." << endl;  
  
    // Compare using binder1st fixing 1st argument:  
    // count the number of integers < 10 in the vector  
    vector<int>::iterator::difference_type result2;  
    result2 = count_if(v1.begin(), v1.end(),  
        binder1st<greater<int> >(greater<int>(), 10));  
    cout << "The number of elements in v1 less than 10 is: "  
         << result2 << "." << endl;  
}  
/* Output:  
The vector v1 = ( 0 5 10 15 20 25 )  
The number of elements in v1 greater than 10 is: 3.  
The number of elements in v1 less than 10 is: 2.  
*/  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<functional>  
  
 **Namespace:** std  
  
## <a name="see-also"></a>Siehe auch  
 [Threadsicherheit in der C++-Standardbibliothek](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [C++-Standardbibliotheksreferenz](../standard-library/cpp-standard-library-reference.md)


