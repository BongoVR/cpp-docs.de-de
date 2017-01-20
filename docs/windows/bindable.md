---
title: "bindable"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "language-reference"
f1_keywords: 
  - "vc-attr.bindable"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "bindable attribute"
ms.assetid: a2360f92-927b-4af8-98cc-6eca7f4ec954
caps.latest.revision: 12
caps.handback.revision: "12"
ms.author: "mblome"
manager: "ghogen"
---
# bindable
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Gibt an, dass die Eigenschaft Datenbindungen unterstützt.  
  
## Syntax  
  
```  
  
[bindable]  
  
```  
  
## Hinweise  
 Das Attribut **bindable** C\+\+ verfügt über die gleichen Funktionen wie das [bindbar](http://msdn.microsoft.com/library/windows/desktop/aa366738) MIDL\-Attribut.  Sie können es für die Eigenschaften verwenden, die mit [propget](../windows/propget.md), [propput](../windows/propput.md)oder [propputref](../windows/propputref.md)\-Attributen definiert werden, oder Sie können eine bindbare Methode manuell definieren.  
  
 Die folgenden MFC\-Beispiele veranschaulichen die Verwendung von **bindable**an:  
  
-   [Kontrollproben: ActiveX\-Steuerelemente MFC\-basierte](assetId:///a44adf86-0ba0-4504-bedb-512b6cba2e63)  
  
-   [CIRC\-Beispiel: ActiveX\-Steuerelement](assetId:///9ba34d04-280e-49f4-90ae-41a6be44c95b)  
  
-   [TESTHELP\-Beispiel: ActiveX\-Steuerelement mit QuickInfo und Hilfe](assetId:///d822861d-c6f0-4d0a-ad11-970eebb1e8cd)  
  
## Beispiel  
 Der folgende Code zeigt, wie Sie **bindable** für eine Eigenschaft verwenden können:  
  
```  
// cpp_attr_ref_bindable.cpp  
// compile with: /LD  
#include <windows.h>  
[  
   uuid("479B29E3-9A2C-11D0-B696-00A0C903487A"),  
   dispinterface,  
   helpstring("property demo Interface")  
]  
__interface IPropDemo : IDispatch {  
  
   [propget, id(1), bindable, displaybind, defaultbind, requestedit] HRESULT P1([out, retval] long *nSize);  
   [propput, id(1), bindable, displaybind, defaultbind, requestedit] HRESULT P1([in] long nSize);  
   [id(3), bindable, propget] HRESULT Object([out, retval] IDispatch **ppObj);  
   [id(3), bindable, propputref] HRESULT Object([in] IDispatch* pObj);     
   [id(-552), helpstring("method AboutBox")] HRESULT AboutBox();  
};  
  
[ module(name="PropDemoLib", uuid="479B29E2-9A2C-11D0-B696-00A0C903487A", version="1.0", helpstring="property demo") ];  
```  
  
## Anforderungen  
  
### Attribut\-Kontext  
  
|||  
|-|-|  
|**Betrifft**|Schnittstellenmethode|  
|**Wiederholbar**|Nein|  
|**Erforderliche Attribute**|None|  
|**Ungültige Attribute**|None|  
  
 Weitere Informationen über das kontexte finden Sie unter [Attribut\-Kontexte](../windows/attribute-contexts.md).  
  
## Siehe auch  
 [IDL Attributes](../windows/idl-attributes.md)   
 [Method Attributes](../windows/method-attributes.md)   
 [defaultbind](../windows/defaultbind.md)   
 [displaybind](../windows/displaybind.md)   
 [immediatebind](../windows/immediatebind.md)   
 [requestedit](../windows/requestedit.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)