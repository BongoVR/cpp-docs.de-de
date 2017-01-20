---
title: "Gewusst wie: &#196;ndern der Verweisklasse in einer systemeigenen Funktion"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "get-started-article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "Plattformaufruf, Verweisklassen"
  - "Verweistypen, Bearbeiten in einer C++-eigenen Funktion"
ms.assetid: c701145b-62a0-4c4b-b32a-db8d69a59720
caps.latest.revision: 12
caps.handback.revision: "10"
ms.author: "mblome"
manager: "ghogen"
---
# Gewusst wie: &#196;ndern der Verweisklasse in einer systemeigenen Funktion
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Sie können eine Verweisklasse mit einem CLR\-Array an eine systemeigene Funktion übergeben und die Klasse mithilfe der PInvoke\-Dienste bearbeiten.  
  
## Beispiel  
 Kompilieren Sie die folgenden systemeigene Bibliothek.  
  
```  
// modify_ref_class_in_native_function.cpp  
// compile with: /LD  
#include <stdio.h>  
#include <windows.h>  
  
struct S {  
   wchar_t* str;  
   int intarr[2];  
};  
  
extern "C"  {  
   __declspec(dllexport) int bar(S* param) {  
      printf_s("str: %S\n", param->str);  
      fflush(stdin);  
      fflush(stdout);  
      printf_s("In native: intarr: %d, %d\n",  
                param->intarr[0], param->intarr[1]);  
      fflush(stdin);  
      fflush(stdout);  
      param->intarr[0]=300;param->intarr[1]=400;  
      return 0;  
    }  
};  
```  
  
## Beispiel  
 Kompilieren Sie die folgende Assembly.  
  
```  
// modify_ref_class_in_native_function_2.cpp  
// compile with: /clr  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
[StructLayout(LayoutKind::Sequential, CharSet = CharSet::Unicode)]  
ref class S  {  
public:  
   [MarshalAsAttribute(UnmanagedType::LPWStr)]  
   String ^ str;  
   [MarshalAsAttribute(UnmanagedType::ByValArray,  
        ArraySubType=UnmanagedType::I4, SizeConst=2)]  
   array<Int32> ^ intarr;  
};  
  
[DllImport("modify_ref_class_in_native_function.dll",  
           CharSet=CharSet::Unicode)]  
int bar([In][Out] S ^ param);  
  
int main() {  
   S ^ param = gcnew S;  
   param->str = "Hello";  
   param->intarr = gcnew array<Int32>(2);  
   param->intarr[0] = 100;  
   param->intarr[1] = 200;  
   bar(param);   // Call to native function  
   Console::WriteLine("In managed: intarr: {0}, {1}",  
                       param->intarr[0], param->intarr[1]);  
}  
```  
  
  **str: Hello**  
**Im systemeigenen Code: intarr: 100, 200**  
**In verwaltetem Code: intarr: 300, 400**   
## Siehe auch  
 [Verwenden von C\+\+\-Interop \(implizites PInvoke\)](../dotnet/using-cpp-interop-implicit-pinvoke.md)