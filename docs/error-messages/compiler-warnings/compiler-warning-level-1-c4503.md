---
title: Compilerwarnung (Stufe 1) C4503 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4503
dev_langs:
- C++
helpviewer_keywords:
- C4503
ms.assetid: 7c5a98ae-5b6d-41d8-b881-12d3ffd5e392
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: adafddff679cbe04cf26a39647760bf595af0bd3
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4503"></a>Compilerwarnung (Stufe 1) C4503
'Bezeichner': ergänzter Name zu lang, Name wurde abgeschnitten.  
  
 Der ergänzte Name wurde länger als das Compilerlimit überschritten (4096) und wurde abgeschnitten. Um diese Warnung und das Abschneiden zu vermeiden, reduzieren Sie die Anzahl der Argumente oder die Länge von Bezeichnern verwendet.  
  
 Eine Situation, in dem diese Warnung ausgegeben wird, ist, wenn der Code enthält spezialisiert Vorlagen auf Vorlagen wiederholt.  Z. B. eine Zuordnung von Karten (aus der C++-Standardbibliothek).  In diesem Fall können Sie den Typdefinitionen an einen Typ (z. B. "Struct"), mit der Zuordnung.  
  
 Sie könnten jedoch nicht den Code umstrukturieren.  Es ist möglich, eine Anwendung ausgeliefert, die C4503 generiert, aber wenn Sie auf ein Symbol, das abgeschnittene Kompilierungsfehlern Link erhalten haben, wird möglicherweise schwerer zum Bestimmen des Typs des Symbols in der Fehler.  Debuggen wird auch schwieriger sein. der Debugger müssen zudem difficultly Zuordnung Symbolname Namen eingeben.  Die Richtigkeit des Programms, ist jedoch nicht betroffen, durch den gekürzten Namen.  
  
 Im folgenden Beispiel wird C4503 generiert:  
  
```  
// C4503.cpp  
// compile with: /W1 /EHsc /c  
// C4503 expected  
#include <string>  
#include <map>  
  
class Field{};  
  
typedef std::map<std::string, Field> Screen;  
typedef std::map<std::string, Screen> WebApp;  
typedef std::map<std::string, WebApp> WebAppTest;  
typedef std::map<std::string, WebAppTest> Hello;  
Hello MyWAT;  
```  
  
 Das folgende Beispiel zeigt eine Möglichkeit, Schreiben Sie Code um C4503 zu beheben:  
  
```  
// C4503b.cpp  
// compile with: /W1 /EHsc /c  
#include <string>  
#include <map>  
  
class Field{};  
struct Screen2 {  
   std::map<std::string, Field> Element;  
};  
  
struct WebApp2 {  
   std::map<std::string, Screen2> Element;  
};  
  
struct WebAppTest2 {  
   std::map<std::string, WebApp2> Element;  
};  
  
struct Hello2 {  
   std::map<std::string, WebAppTest2> Element;  
};  
  
Hello2 MyWAT2;  
```