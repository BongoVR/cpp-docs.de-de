---
title: 'Vorgehensweise: Schreiben einer Textdatei (C + c++ / CLI) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- files [C++], text
- text files, writing in C++
ms.assetid: 39ecdba6-84e0-485c-a202-84cf6d7b8d4a
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 58b53159bab17ef0fddf5b26606889f89412856e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="how-to-write-a-text-file-ccli"></a>Gewusst wie: Schreiben einer Textdatei (C++/CLI)
Im folgenden Codebeispiel wird veranschaulicht, wie eine Textdatei erstellt und in diese mithilfe der im <xref:System.IO.StreamWriter>-Namespace definierten <xref:System.IO>-Klasse geschrieben wird. Der Name der zu erstellenden Datei wird vom <xref:System.IO.StreamWriter>-Konstruktor übernommen. Wenn die Datei existiert, wird sie überschrieben (außer wenn Sie True als zweites <xref:System.IO.StringWriter>-Konstruktorargument übergeben).  
  
 Die Datei wird dann mithilfe der Funktionen <xref:System.IO.StreamWriter.Write%2A> und <xref:System.IO.TextWriter.WriteLine%2A> abgelegt.  
  
## <a name="example"></a>Beispiel  
  
```  
// text_write.cpp  
// compile with: /clr  
using namespace System;  
using namespace System::IO;  
  
int main()   
{  
   String^ fileName = "textfile.txt";  
  
   StreamWriter^ sw = gcnew StreamWriter(fileName);  
   sw->WriteLine("A text file is born!");  
   sw->Write("You can use WriteLine");  
   sw->WriteLine("...or just Write");  
   sw->WriteLine("and do {0} output too.", "formatted");  
   sw->WriteLine("You can also send non-text objects:");  
   sw->WriteLine(DateTime::Now);  
   sw->Close();  
   Console::WriteLine("a new file ('{0}') has been written", fileName);  
  
   return 0;  
}  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Datei- und Datenstrom-E/A](http://msdn.microsoft.com/Library/4f4a33a9-66b7-4cd7-a285-4ad3e4276cd2)   
 [.NET-Programmierung mit C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)