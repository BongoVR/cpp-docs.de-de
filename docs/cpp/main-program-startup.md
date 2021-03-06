---
title: 'main: Programmstart | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- vc.main.startup
- _tmain
dev_langs:
- C++
helpviewer_keywords:
- program startup [C++]
- entry points, program
- wmain function
- _tmain function
- startup code, main function
- main function, program startup
ms.assetid: f9581cd6-93f7-4bcd-99ec-d07c3c107dd4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2999596fe30afca4c9945efc34a8537e9f45e14a
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="main-program-startup"></a>main: Programmstart
Eine spezielle Funktion mit dem Namen `main` ist der Ausgangspunkt der Ausführung für C- und C++-Programme. Wenn Sie Code schreiben, der dem [!INCLUDE[TLA#tla_unicode](../atl-mfc-shared/reference/includes/tlasharptla_unicode_md.md)]-Programmiermodell entspricht, können Sie `wmain` verwenden. Dies ist die Breitzeichenversion von `main`.  
  
 Die `main`-Funktion wird vom Compiler nicht vordefiniert. Sie muss im Programmtext angegeben werden.  
  
 Die Deklarationssyntax für `main` lautet  
  
```  
int main();  
```  
  
 oder optional  
  
```  
int main(int argc, char *argv[], char *envp[]);  
```  
  
## <a name="microsoft-specific"></a>Microsoft-spezifisch  
 Die Deklarationssyntax für `wmain` lautet wie folgt:  
  
```  
int wmain( );  
```  
  
 oder optional  
  
```  
int wmain(int argc, wchar_t *argv[], wchar_t *envp[]);  
```  
  
 Sie können auch das in TCHAR.h definierte `_tmain` verwenden. `_tmain` wird in `main` aufgelöst, es sei denn, _UNICODE ist definiert. In diesem Fall wird `_tmain` in `wmain` aufgelöst.  
  
 Alternativ können die Funktionen `main` und `wmain` als Rückgabe von `void` (kein Rückgabewert) deklariert werden. Wenn Sie deklarieren `main` oder `wmain` als Rückgabe `void`, Sie können nicht auf den übergeordneten Prozess oder dem Betriebssystem einen Exitcode zurückgeben, indem eine [zurückgeben](../cpp/return-statement-in-program-termination-cpp.md) Anweisung. Zurückzugebenden ein Exitcode Wenn `main` oder `wmain` wird deklariert als `void`, verwenden Sie die [beenden](../cpp/exit-function.md) Funktion.  
  
**Ende Microsoft-spezifisch**  
 Die Typen für `argc` und `argv` werden von der Programmiersprache definiert. Die Namen `argc`, `argv` und `envp` sind üblich, für den Compiler jedoch nicht erforderlich. Weitere Informationen und ein Beispiel finden Sie unter [Argumentdefinitionen](../cpp/argument-definitions.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Stichwörter](../cpp/keywords-cpp.md)   
 [Mithilfe von "wmain" anstelle von main](../cpp/using-wmain-instead-of-main.md)   
 [Einschränkungen der main-Funktion](../cpp/main-function-restrictions.md)