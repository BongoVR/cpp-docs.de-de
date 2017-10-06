---
title: __interface | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- __interface_cpp
dev_langs:
- C++
helpviewer_keywords:
- __interface keyword [C++]
ms.assetid: ca5d400b-d6d8-4ba2-89af-73f67e5ec056
caps.latest.revision: 10
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
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: e502574b9d55238d6f9aed33949e06db3ec6349d
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="interface"></a>__interface
**Microsoft-spezifisch**  
  
 Eine Visual C++-Schnittstelle kann wie folgt definiert werden:  
  
-   Kann von null oder mehreren Basisschnittstellen erben.  
  
-   Kann nicht von einer Basisklasse erben.  
  
-   Kann nur öffentliche, rein virtuelle Methoden enthalten.  
  
-   Kann keine Konstruktoren, Destruktoren oder Operatoren enthalten.  
  
-   Kann keine statischen Methoden enthalten.  
  
-   Kann keine Datenmember enthalten. Eigenschaften sind zulässig.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
modifier  
 __interface interface-name {interface-definition};  
```  
  
## <a name="remarks"></a>Hinweise  
 C++ [Klasse](../cpp/class-cpp.md) oder [Struktur](../cpp/struct-cpp.md) mit diesen Regeln implementiert werden kann, aber `__interface` erzwingt diese.  
  
 Im Folgenden ist eine Beispiel-Schnittstellendefinition angegeben:  
  
```  
__interface IMyInterface {  
   HRESULT CommitX();  
   HRESULT get_X(BSTR* pbstrName);  
};  
```  
  
 Informationen zu verwalteten Schnittstellen finden Sie unter [Schnittstellenklasse](../windows/interface-class-cpp-component-extensions.md).  
  
 Sie müssen nicht explizit angeben, dass die `CommitX`- und `get_X`-Funktionen rein virtuell sind. Eine entsprechende Deklaration für die erste Funktion wäre:  
  
```  
virtual HRESULT CommitX() = 0;  
```  
  
 `__interface`impliziert den [Novtable](../cpp/novtable.md) `__declspec` Modifizierer.  
  
## <a name="example"></a>Beispiel  
 Die folgenden Beispiele zeigen, wie die in einer Schnittstelle deklarierten Eigenschaften verwendet werden.  
  
```  
// deriv_interface.cpp  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
#include <atlcom.h>  
#include <string.h>  
#include <comdef.h>  
#include <stdio.h>  
  
[module(name="test")];  
  
[ object, uuid("00000000-0000-0000-0000-000000000001"), library_block ]  
__interface IFace {  
   [ id(0) ] int int_data;  
   [ id(5) ] BSTR bstr_data;  
};  
  
[ coclass, uuid("00000000-0000-0000-0000-000000000002") ]  
class MyClass : public IFace {  
private:  
    int m_i;  
    BSTR m_bstr;   
  
public:  
    MyClass()  
    {  
        m_i = 0;  
        m_bstr = 0;  
    }  
  
    ~MyClass()  
    {  
        if (m_bstr)   
            ::SysFreeString(m_bstr);  
    }  
  
    int get_int_data()  
    {  
        return m_i;  
    }  
  
    void put_int_data(int _i)   
    {  
        m_i = _i;  
    }  
  
    BSTR get_bstr_data()  
    {   
        BSTR bstr = ::SysAllocString(m_bstr);  
        return bstr;   
    }  
  
    void put_bstr_data(BSTR bstr)   
    {   
        if (m_bstr)   
            ::SysFreeString(m_bstr);  
        m_bstr = ::SysAllocString(bstr);  
    }  
};  
  
int main()  
{  
    _bstr_t bstr("Testing");  
    CoInitialize(NULL);  
    CComObject<MyClass>* p;  
    CComObject<MyClass>::CreateInstance(&p);  
    p->int_data = 100;  
    printf_s("p->int_data = %d\n", p->int_data);                
    p->bstr_data = bstr;  
    printf_s("bstr_data = %S\n", p->bstr_data);  
}  
```  
  
```Output  
p->int_data = 100  
bstr_data = Testing  
```  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Stichwörter](../cpp/keywords-cpp.md)   
 [Schnittstellenattribut](../windows/interface-attributes.md)
