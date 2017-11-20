---
title: Compilerwarnung (Stufe 4) C4564 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4564
dev_langs: C++
helpviewer_keywords: C4564
ms.assetid: 555b301b-313e-4262-9f81-eb878674be60
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 43462a2ea15ea50306b346d02a149a185cee902f
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-warning-level-4-c4564"></a>Compilerwarnung (Stufe 4) C4564
Methode 'Methode' Klasse 'Klasse' definiert den nicht unterstützten Standardparameter 'Parameter'  
  
 Der Compiler hat eine Methode mit einem oder mehreren Parametern mit Standardwerten. Die Standardwerte für die Parameter wird ignoriert, wenn die Methode aufgerufen wird. Geben Sie explizit Werte für diese Parameter. Wenn Sie Werte für diese Parameter nicht explizit angeben, generiert der C++-Compiler einen Fehler.  
  
 Der angegebene die folgenden DLL-Datei erstellt, die mit Visual Basic ermöglicht die Standardparameter für Methodenargumente:  
  
```  
' C4564.vb  
' compile with: vbc /t:library C4564.vb  
Public class TestClass  
   Public Sub MyMethod (a as Integer, _  
                        Optional c as Integer=1)  
   End Sub  
End class  
```  
  
 Und die folgenden C++-Beispiel, das die DLL-Datei erstellt, die mit Visual Basic verwendet,  
  
```  
// C4564.cpp  
// compile with: /clr /W4 /WX  
#using <C4564.dll>  
  
int main() {  
   TestClass ^ myx = gcnew TestClass();   // C4564  
   myx->MyMethod(9);  
   // try the following line instead, to avoid an error  
   // myx->MyMethod(9, 1);  
}  
```