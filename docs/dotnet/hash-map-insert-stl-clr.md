---
title: 'hash_map:: Insert (STL/CLR) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::hash_map::insert
dev_langs:
- C++
helpviewer_keywords:
- insert member [STL/CLR]
ms.assetid: 52926ec7-ad4e-4791-a043-46136ee40a69
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 89f6000f7950aa55b4b547def13dcb9cfe34012c
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="hashmapinsert-stlclr"></a>hash_map::insert (STL/CLR)
Fügt Elemente hinzu.  
  
## <a name="syntax"></a>Syntax  
  
```  
cliext::pair<iterator, bool> insert(value_type val);  
iterator insert(iterator where, value_type val);  
template<typename InIter>  
    void insert(InIter first, InIter last);  
void insert(System::Collections::Generic::IEnumerable<value_type>^ right);  
```  
  
#### <a name="parameters"></a>Parameter  
 first  
 Anfang des Bereichs, der eingefügt.  
  
 last  
 Das Ende des Bereichs einfügen.  
  
 Rechts  
 Die Enumeration eingefügt.  
  
 Val  
 Schlüssel-Wert einfügen.  
  
 wo  
 Die Position, im Container (nur Hinweis) einfügen.  
  
## <a name="remarks"></a>Hinweise  
 Jede der Memberfunktionen Fügt eine Sequenz, die von den verbleibenden Operanden angegeben.  
  
 Die erste Memberfunktion zum Einfügen eines Elements mit dem Wert versucht `val`, und gibt ein Wertepaar `X`. Wenn `X.second` ist "true", `X.first` bestimmt das neu eingefügte Element; andernfalls `X.first` kennzeichnet ein Element mit entsprechender Sortierung, die bereits vorhanden ist und kein neues Element eingefügt wird. Es können Sie verwenden, um ein einzelnes Element einzufügen.  
  
 Die zweite Memberfunktion Fügt ein Element mit dem Wert `val`mit `where` als Hinweis (zur Verbesserung der Leistung), und gibt einen Iterator, der das neu eingefügte Element festlegt. Damit können sie ein einzelnes Element einfügen, das neben einem Element möglicherweise, die Sie kennen.  
  
 Die dritte Memberfunktion fügt die Sequenz [`first`, `last`). Sie verwenden ihn zum Einfügen von NULL oder mehr Elementen aus einer anderen Sequenz kopiert.  
  
 Die vierte Memberfunktion fügt die Sequenz, die vom angegebenen der `right`. Sie verwenden es, fügen Sie eine Sequenz, die durch einen Enumerator beschrieben.  
  
 Jede elementeinfügung dauert einige Zeit, die proportional zum Logarithmus der Anzahl der Elemente in der kontrollierten Sequenz. Kann in amortisierter konstanter Zeit, jedoch die Einfügung erhält einen Hinweis, der ein Element, das neben der Einfügemarke festlegt.  
  
## <a name="example"></a>Beispiel  
  
```  
// cliext_hash_map_insert.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
typedef Myhash_map::pair_iter_bool Pairib;   
int main()   
    {   
    Myhash_map c1;   
    c1.insert(Myhash_map::make_value(L'a', 1));   
    c1.insert(Myhash_map::make_value(L'b', 2));   
    c1.insert(Myhash_map::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// insert a single value, unique and duplicate   
    Pairib pair1 =   
        c1.insert(Myhash_map::make_value(L'x', 24));   
    System::Console::WriteLine("insert([L'x' 24]) = [{0} {1}] {2}",   
        pair1.first->first, pair1.first->second, pair1.second);   
  
    pair1 = c1.insert(Myhash_map::make_value(L'b', 2));   
    System::Console::WriteLine("insert([L'b' 2]) = [{0} {1}] {2}",   
        pair1.first->first, pair1.first->second, pair1.second);   
  
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// insert a single value with hint   
    Myhash_map::iterator it =   
        c1.insert(c1.begin(), Myhash_map::make_value(L'y', 25));   
    System::Console::WriteLine("insert(begin(), [L'y' 25]) = [{0} {1}]",   
        it->first, it->second);   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// insert an iterator range   
    Myhash_map c2;   
    it = c1.end();   
    c2.insert(c1.begin(), --it);   
    for each (Myhash_map::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// insert an enumeration   
    Myhash_map c3;   
    c3.insert(   // NOTE: cast is not needed   
        (System::Collections::Generic::   
            IEnumerable<Myhash_map::value_type>^)%c1);   
    for each (Myhash_map::value_type elem in c3)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
 [a 1] [b 2] [c 3]  
insert([L'x' 24]) = [x 24] True  
insert([L'b' 2]) = [b 2] False  
 [a 1] [b 2] [c 3] [x 24]  
insert(begin(), [L'y' 25]) = [y 25]  
 [a 1] [b 2] [c 3] [x 24] [y 25]  
 [a 1] [b 2] [c 3] [x 24]  
 [a 1] [b 2] [c 3] [x 24] [y 25]  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext Hash_map/>  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [hash_map (STL/CLR)](../dotnet/hash-map-stl-clr.md)