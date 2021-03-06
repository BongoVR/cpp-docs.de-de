---
title: naked (C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- naked_cpp
dev_langs:
- C++
helpviewer_keywords:
- __declspec keyword [C++], naked
- naked __declspec keyword
ms.assetid: 69723241-05e1-439b-868e-20a83a16ab6d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 84e172c24bbb87f9243a4c0de25a98c90e043acc
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="naked-c"></a>naked (C++)
**Microsoft-spezifisch**  
  
 Für die Funktionen, die mit dem `naked`-Attribut deklariert werden, generiert der Compiler Code ohne Prolog- und Epilogcode. Sie können diese Funktion verwenden, um eigene Prolog-/Epilogcodesequenzen mithilfe von Inlineassemblercode zu schreiben. Naked-Funktionen sind vor allem beim Schreiben von virtuellen Gerätetreibern hilfreich.  Beachten Sie, dass das `naked`-Attribut nur für x86 und ARM gültig und nicht für [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)] verfügbar ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
__declspec(naked) declarator  
```  
  
## <a name="remarks"></a>Hinweise  
 Da die `naked` Attribut nur für die Definition einer Funktion relevant ist und kein Typmodifizierer, naked-Funktionen müssen die erweiterte Attributsyntax verwenden und die [__declspec](../cpp/declspec.md) Schlüsselwort.  
  

 Der Compiler nicht Generieren einer Inlinefunktion für eine Funktion mit dem naked-Attribut markiert, auch wenn die Funktion auch mit gekennzeichnet ist die ["__forceinline"](inline-functions-cpp.md) Schlüsselwort.  

  
 Der Compiler gibt einen Fehler aus, wenn das `naked`-Attribut auf einen anderen Wert als die Definition einer Nichtmembermethode angewendet wird.  
  
## <a name="examples"></a>Beispiele  
 Dieser Code definiert eine Funktion mit dem `naked`-Attribut:  
  
```  
__declspec( naked ) int func( formal_parameters ) {}  
```  
  
 Oder auch:  
  
```  
#define Naked __declspec( naked )  
Naked int func( formal_parameters ) {}  
```  
  
 Das `naked`-Attribut wirkt sich nur auf die Codegenerierung des Compilers für die Prolog- und Epilogsequenzen der Funktion aus. Es hat keine Auswirkungen auf den Code, der zum Aufrufen solcher Funktionen generiert wird. Daher gilt das `naked`-Attribut nicht als Teil des Typs der Funktion, und Funktionszeiger dürfen nicht das `naked`-Attribut enthalten. Darüber hinaus kann das `naked`-Attribut nicht auf eine Datendefinition angewendet werden. Beispielsweise wird mit diesem Codebeispiel ein Fehler generiert:  
  
```  
__declspec( naked ) int i;       // Error--naked attribute not  
                                 // permitted on data declarations.  
```  
  
 Das `naked`-Attribut ist nur für die Funktionsdefinition relevant und kann nicht im Funktionsprototyp angegeben werden. Beispielsweise wird mit dieser Deklaration ein Compilerfehler generiert:  
  
```  
__declspec( naked ) int func();  // Error--naked attribute not   
                                 // permitted on function declarations  
```  
  
 **Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [__declspec](../cpp/declspec.md)   
 [Stichwörter](../cpp/keywords-cpp.md)   
 [Naked-Funktionsaufrufe](../cpp/naked-function-calls.md)