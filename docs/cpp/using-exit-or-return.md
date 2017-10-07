---
title: "Beenden oder zurückgeben mit | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- Exit
dev_langs:
- C++
helpviewer_keywords:
- exit function
- return keyword [C++], using for program termination
ms.assetid: b5136c5c-2505-4229-8691-2a1d6a98760b
caps.latest.revision: 8
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: 9fc6588a6593559314774e30a4d65c5a60779eb5
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="using-exit-or-return"></a>Verwenden von "exit" oder "return"
Beim Aufruf **beenden** oder führen Sie eine `return` -Anweisung vom **main**, statische Objekte werden in umgekehrter Reihenfolge ihrer Initialisierung zerstört. Das folgende Beispiel zeigt, wie so eine Initialisierung und Bereinigung funktionieren.  
  
## <a name="example"></a>Beispiel  
  
```  
// using_exit_or_return1.cpp  
#include <stdio.h>  
class ShowData {  
public:  
   // Constructor opens a file.  
   ShowData( const char *szDev ) {  
   errno_t err;  
      err = fopen_s(&OutputDev, szDev, "w" );  
   }  
  
   // Destructor closes the file.  
   ~ShowData() { fclose( OutputDev ); }  
  
   // Disp function shows a string on the output device.  
   void Disp( char *szData ) {   
      fputs( szData, OutputDev );  
   }  
private:  
   FILE *OutputDev;  
};  
  
//  Define a static object of type ShowData. The output device  
//   selected is "CON" -- the standard output device.  
ShowData sd1 = "CON";  
  
//  Define another static object of type ShowData. The output  
//   is directed to a file called "HELLO.DAT"  
ShowData sd2 = "hello.dat";  
  
int main() {  
   sd1.Disp( "hello to default device\n" );  
   sd2.Disp( "hello to file hello.dat\n" );  
}  
```  
  
 Im vorherigen Beispiel werden die statischen Objekte `sd1` und `sd2` vor der Eingabe in `main` erstellt und initialisiert. Nachdem das Programm mithilfe der `return`-Anweisung beendet ist, wird zuerst `sd2` und danach `sd1` gelöscht. Der Destruktor für die Klasse `ShowData` schließt die Dateien, die diesen statischen Objekten zugeordnet sind.   
  
 Eine andere Möglichkeit zum Schreiben des Codes besteht darin, die `ShowData`-Objekte mit dem Blockbereich zu deklarieren, sodass sie gelöscht werden, wenn sie den Gültigkeitsbereich verlassen:  
  
```  
int main() {  
   ShowData sd1, sd2( "hello.dat" );  
  
   sd1.Disp( "hello to default device\n" );  
   sd2.Disp( "hello to file hello.dat\n" );  
}  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Weitere Überlegungen zur Beendigung](../cpp/additional-termination-considerations.md)
