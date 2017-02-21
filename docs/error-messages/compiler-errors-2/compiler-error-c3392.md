---
title: "Compilerfehler C3392 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3392"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3392"
ms.assetid: e4757596-e2aa-4314-b01e-5c4bfd2110e9
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C3392
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Typargument': Ungültiges Typargument für den generischen 'Param'\-Parameter von 'generischer\_Typ' \(generisch\). Muss einen öffentlichen parameterlosen Konstruktor aufweisen.  
  
 Ein generischer Typ wurde fehlerhaft instanziiert.  Überprüfen Sie die Typdefinition.  Weitere Informationen finden Sie unter [Generics](../../windows/generics-cpp-component-extensions.md).  
  
## Beispiel  
 Im folgenden Beispiel wird mit C\# eine Komponente erstellt, die einen generischen Typ mit bestimmten Einschränkungen enthält, die nicht unterstützt werden, wenn generische Typen in [!INCLUDE[vcprvclong](../../error-messages/compiler-errors-2/includes/vcprvclong_md.md)] geschrieben werden. Weitere Informationen finden Sie unter [Einschränkungen für Typparameter](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
```  
// C3392.cs // compile with: /target:library // a C# program public class GR<C, V, N> where C : class where V : struct where N : new() {}  
```  
  
## Beispiel  
 Im folgenden Beispiel wird C3392 generiert:  
  
```  
// C3392_b.cpp // compile with: /clr #using <C3392.dll> ref class R { R(int) {} }; ref class N { N() {} }; value class V {}; ref class N2 { public: N2() {} }; ref class R2 { public: R2() {} }; int main () { GR<R^, V, N^>^ gr1;   // C3392 GR<R^, V, N2^>^ gr1a;   // OK GR<R^, N^, N^>^ gr3;   // C3392 GR<R^, V, N2^>^ gr3a;   // OK GR<R^, V, R^>^ gr4;   // C3392 GR<R^, V, R2^>^ gr4a;   // OK }  
```