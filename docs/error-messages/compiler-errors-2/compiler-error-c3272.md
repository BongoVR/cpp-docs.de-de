---
title: "Compilerfehler C3272 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3272"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3272"
ms.assetid: 7cdf254d-f207-4116-a1bf-7386f3b82a6f
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Compilerfehler C3272
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"Symbol": Symbol erfordert "FieldOffset", da es ein Member des Typs "Typname" ist, der mit "StructLayout\(LayoutKind::Explicit\)" definiert wurde.  
  
 Wenn [StructLayout](frlrfSystemRuntimeInteropServicesStructLayoutAttributeClassTopic) `Explicit` aktiv ist, müssen Felder mit [FieldOffset](frlrfSystemRuntimeInteropServicesFieldOffsetAttributeClassTopic) gekennzeichnet werden.  
  
 Im folgenden Beispiel wird C3272 generiert:  
  
```  
// C3272_2.cpp // compile with: /clr /c using namespace System; using namespace System::Runtime::InteropServices; [StructLayout(LayoutKind::Explicit)] ref struct X { int data_;   // C3272 // try the following line instead // [FieldOffset(0)] int data_; };  
```  
  
 Im folgenden Beispiel wird C3272 generiert:  
  
```  
// C3272.cpp // compile with: /clr:oldSyntax /LD #using <mscorlib.dll> using namespace System; using namespace System::Runtime::InteropServices; [StructLayout(LayoutKind::Explicit)] __gc struct X { int data_;   // C3272 // try the following line instead // [FieldOffset(0)] int data_; };  
```