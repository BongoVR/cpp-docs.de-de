---
title: Public (C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- public_cpp
dev_langs:
- C++
helpviewer_keywords:
- public keyword [C++]
ms.assetid: f3e10a59-39f6-4bcd-827e-3e99f8f89497
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 49c7f113aa234a5e682576ff509199c0223b7cc5
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="public-c"></a>public (C++)
## <a name="syntax"></a>Syntax  
  
```  
public:  
   [member-list]  
public base-class  
```  
  
## <a name="remarks"></a>Hinweise  
 Wenn Sie eine Liste von Klassenmembern vorangestellt der **öffentliche** -Schlüsselwort Gibt an, dass diese Member aus jeder Funktion zugegriffen werden. Dies gilt für alle Member, die bis zum nächsten Zugriffsspezifizierer oder am Ende der Klasse deklariert werden.  
  
 Wenn Sie den Namen einer Basisklasse vorangestellt der **öffentlichen** Schlüsselwort Gibt an, dass die öffentlichen und geschützten Member der Basisklasse öffentliche bzw. geschützte Member der abgeleiteten Klasse.  
  
 Der Standardzugriff von Membern einer Klasse ist privat. Der Standardzugriff der Member in einer Struktur oder Union ist öffentlich.  
  
 Der Standardzugriff einer Basisklasse ist bei Klassen privat und bei Strukturen öffentlich. Unions können keine Basisklassen aufweisen.  
  
 Weitere Informationen finden Sie unter [private](../cpp/private-cpp.md), [geschützt](../cpp/protected-cpp.md), ["Friend"](../cpp/friend-cpp.md), und der memberzugriffstabelle in [Steuern des Zugriffs auf Klassenmember](member-access-control-cpp.md) .  
  
## <a name="clr-specific"></a>"/clr"-spezifisch  
 In CLR-Typen, die C++ Schlüsselwörter für Zugriffsspezifizierer zugreifen (**öffentlichen**, `private`, und `protected`) kann die Sichtbarkeit von Typen und Methoden hinsichtlich der Assemblys beeinträchtigen. Weitere Informationen finden Sie unter [Memberzugriffssteuerung](member-access-control-cpp.md).  
  
> [!NOTE]
>  Dateien mit kompiliert [/ln](../build/reference/ln-create-msil-module.md) nicht durch dieses Verhalten beeinträchtigt werden. In diesem Fall werden alle verwalteten Klassen (entweder "public" oder "private") angezeigt.  
  
## <a name="end-clr-specific"></a>"/clr"-spezifisch – Ende  
  
## <a name="example"></a>Beispiel  
  
```  
// keyword_public.cpp  
class BaseClass {  
public:  
   int pubFunc() { return 0; }  
};  
  
class DerivedClass : public BaseClass {};  
  
int main() {  
   BaseClass aBase;  
   DerivedClass aDerived;  
   aBase.pubFunc();       // pubFunc() is accessible   
                          //    from any function  
   aDerived.pubFunc();    // pubFunc() is still public in   
                          //    derived class  
}  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Steuern des Zugriffs auf Klassenmember](member-access-control-cpp.md)   
 [Schlüsselwörter](../cpp/keywords-cpp.md)