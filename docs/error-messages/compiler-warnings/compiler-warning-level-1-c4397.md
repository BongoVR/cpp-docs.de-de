---
title: Compilerwarnung (Stufe 1) C4397 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4397
dev_langs:
- C++
helpviewer_keywords:
- C4397
ms.assetid: 6346fdc2-dbbf-4fba-803a-32b0d0a707be
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ce5c1a23c37ed572a716bdf6aa7a3216d8bdb771
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4397"></a>Compilerwarnung (Stufe 1) C4397
DefaultCharSetAttribute wird ignoriert.  
  
 <xref:System.Runtime.InteropServices.DefaultCharSetAttribute> wird von der Visual C++-Compiler ignoriert. Um einen Zeichensatz für die DLL anzugeben, verwenden Sie die CharSet-Option von DllImport. Weitere Informationen finden Sie unter [mithilfe von C++-Interop (implizites PInvoke)](../../dotnet/using-cpp-interop-implicit-pinvoke.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4397 generiert.  
  
```  
// C4397.cpp  
// compile with: /W1 /c /clr  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
[module:DefaultCharSetAttribute(CharSet::Unicode)];   // C4397  
  
[DllImport("kernel32", EntryPoint="CloseHandle", CharSet=CharSet::Unicode)]   // OK  
extern "C" bool ImportDefault(IntPtr hObject);  
  
public ref class MySettingVC {  
public:  
   void method() {  
      ImportDefault(IntPtr::Zero);  
   }  
};  
  
[StructLayout(LayoutKind::Explicit)]  
public ref struct StructDefault1{};  
  
public ref class ClassDefault1{};  
```