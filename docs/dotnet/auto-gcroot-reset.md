---
title: auto_gcroot::Reset | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- msclr::auto_gcroot::reset
- auto_gcroot::reset
- msclr.auto_gcroot.reset
- auto_gcroot.reset
dev_langs:
- C++
helpviewer_keywords:
- reset method
ms.assetid: dd58467f-3885-4a15-99fb-ed6dd5d19622
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: d2ff59b6fc9c4f893f87fbb59b0531c5ba8917fb
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="autogcrootreset"></a>auto_gcroot::reset
Die aktuelle im Besitz befindliches Objekt zu zerstören, und optional ein neues Objekt zurückzufordern.  
  
## <a name="syntax"></a>Syntax  
  
```  
void reset(  
   _element_type _new_ptr = nullptr  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `_new_ptr`  
 (Optional) Das neue Objekt.  
  
## <a name="example"></a>Beispiel  
  
```  
// msl_auto_gcroot_reset.cpp  
// compile with: /clr  
#include <msclr\auto_gcroot.h>  
  
using namespace System;  
using namespace msclr;  
  
ref class ClassA {  
   String^ m_s;  
public:  
   ClassA( String^ s ) : m_s( s ) {  
      Console::WriteLine( "ClassA constructor: " + m_s );  
   }  
   ~ClassA() {  
      Console::WriteLine( "ClassA destructor: " + m_s );  
   }  
  
   void PrintHello() {  
      Console::WriteLine( "Hello from {0} A!", m_s );  
   }  
};  
  
int main()  
{  
   auto_gcroot<ClassA^> agc1 = gcnew ClassA( "first" );  
   agc1->PrintHello();  
  
   ClassA^ ha = gcnew ClassA( "second" );  
   agc1.reset( ha ); // release first object, reference second  
   agc1->PrintHello();  
  
   agc1.reset(); // release second object, set to nullptr  
  
   Console::WriteLine( "done" );  
}  
```  
  
```Output  
ClassA constructor: first  
Hello from first A!  
ClassA constructor: second  
ClassA destructor: first  
Hello from second A!  
ClassA destructor: second  
done  
```  
  
## <a name="requirements"></a>Anforderungen  
 **Headerdatei** \<msclr\auto_gcroot.h >  
  
 **Namespace** Msclr  
  
## <a name="see-also"></a>Siehe auch  
 [Auto_gcroot-Elemente](../dotnet/auto-gcroot-members.md)   
 [auto_gcroot::Release](../dotnet/auto-gcroot-release.md)   
 [auto_gcroot::attach](../dotnet/auto-gcroot-attach.md)