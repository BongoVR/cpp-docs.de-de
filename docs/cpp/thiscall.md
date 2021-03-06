---
title: __thiscall | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- __thiscall
- __thiscall_cpp
dev_langs:
- C++
helpviewer_keywords:
- __thiscall keyword [C++]
ms.assetid: a6a22dd2-0101-4885-b33b-22f6057965df
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9dccd9e80a23b1636bd869d406824c9997f4cdef
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="thiscall"></a>__thiscall
## <a name="microsoft-specific"></a>Microsoft-spezifisch  
 Die `__thiscall`-Aufrufkonvention wird für Memberfunktionen verwendet und ist die Standardaufrufkonvention, die von C++-Memberfunktionen verwendet wird, die keine variablen Argumente verwenden. Unter `__thiscall` entleert der Aufgerufene den Stapel, was für `vararg`-Funktionen nicht möglich ist. Argumente werden von rechts nach links auf den Stapel geschoben, wobei der `this`-Zeiger auf der x86-Architektur über das Register "ECX" übergeben wird, und nicht auf dem Stapel.  
  
 Die Verwendung von `__thiscall` ist in Klassen sinnvoll, deren Memberfunktionen standardmäßig `__clrcall` verwenden. In diesem Fall können Sie `__thiscall` verwenden, um individuelle Memberfunktionen aus dem systemeigenen Code aufrufbar zu machen.  
  
 Beim Kompilieren mit [/CLR: pure](../build/reference/clr-common-language-runtime-compilation.md), sind alle Funktionen und Funktionszeiger `__clrcall` sofern nicht anders angegeben. Die Compileroptionen **/clr:pure** und **/clr:safe** sind in Visual Studio 2015 veraltet.  
  
 In Versionen vor Visual C++ 2005 konnte die thiscall-Aufrufkonvention nicht explizit in einem Programm angegeben werden, da `thiscall` kein Schlüsselwort war.  
  
 `vararg`-Memberfunktionen verwenden die `__cdecl`-Aufrufkonvention. Alle Funktionsargumente werden auf dem Stapel abgelegt, wobei der `this`-Zeiger zuletzt auf dem Stapel abgelegt wird.  
  
 Da diese Aufrufkonvention nur für C++ gültig ist, gibt es kein Schema zur C-Namensergänzung.  
  
 Auf ARM und [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)] Computern `__thiscall` akzeptiert und vom Compiler ignoriert.  
  
 Wenn die Funktion bei nicht statischen Klassenfunktionen abweichend definiert ist, muss der Aufrufkonventionsmodifizierer nicht in der abweichenden Definition angegeben werden. Das bedeutet, dass für nicht statische Membermethoden der Klasse zum Zeitpunkt der Definition die während der Deklaration angegebene Aufrufkonvention angenommen wird.  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Argumentübergabe und Benennungskonventionen](../cpp/argument-passing-and-naming-conventions.md)