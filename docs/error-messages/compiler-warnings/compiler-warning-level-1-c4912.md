---
title: "Compilerwarnung (Stufe 1) C4912"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "C4912"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4912"
ms.assetid: ba1f1a66-8c20-4792-9ac8-43e49f729ae2
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "corob"
manager: "ghogen"
---
# Compilerwarnung (Stufe 1) C4912
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Attribut': Das Attribut besitzt ein nicht definiertes Verhalten für ein geschachteltes UDT.  
  
 Auf geschachtelte UDTs \(benutzerdefinierter Typ, z. B. eine Typdefinition, Union oder Struktur\) anwendbare Attribute werden möglicherweise ignoriert.  
  
 Der folgende Code zeigt, wie diese Warnung generiert werden würde:  
  
```  
// C4912.cpp // compile with: /W1 #include <windows.h> [emitidl, module(name="xx")]; [object, uuid("00000000-0000-0000-0000-000000000002")] __interface IMy { }; [coclass, default(IMy), appobject, uuid("00000000-0000-0000-0000-000000000001")] class CMy : public IMy { [export, v1_enum] typedef enum myEnum { k3_1 = 1, k3_2 = 2 } myEnumv;   // C4912 }; int main() { }  
```