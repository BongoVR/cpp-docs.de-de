---
title: 'Vorgehensweise: Verwenden von regulären Ausdrücken zum Extrahieren von Datenfeldern (C + c++ / CLI) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- strings [C++], extracting data from
- formatted strings [C++]
- regular expressions [C++], extracting data fields
- data [C++], extracting from strings
ms.assetid: b581d9b6-630e-48fa-94fe-20b0f7b89b06
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 20e1139ccee0c3cc1533f42fb1b9e1eafaca3afd
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-use-regular-expressions-to-extract-data-fields-ccli"></a>Gewusst wie: Verwenden von regulären Ausdrücken zum Extrahieren von Datenfeldern (C++/CLI)
Das folgende Codebeispiel veranschaulicht die Verwendung von regulären Ausdrücken zum Extrahieren von Daten aus einer formatierten Zeichenfolge. Im folgenden Codebeispiel wird mit der <xref:System.Text.RegularExpressions.Regex> Klasse, um ein Muster anzugeben, die eine e-Mail-Adresse entspricht. Diese gehören Feldbezeichner, die verwendet werden kann, um den Benutzer und Hostbereich alle e-Mail-Adressen abzurufen. Die <xref:System.Text.RegularExpressions.Match> Klasse wird verwendet, um die eigentlichen Mustervergleich auszuführen. Wenn die angegebene e-Mail-Adresse gültig ist, den Benutzernamen und den Hostnamen extrahiert und angezeigt.  
  
## <a name="example"></a>Beispiel  
  
```  
// Regex_extract.cpp  
// compile with: /clr  
#using <System.dll>  
  
using namespace System;  
using namespace System::Text::RegularExpressions;  
  
int main()  
{  
    array<String^>^ address=  
    {  
        "jay@southridgevideo.com",  
        "barry@adatum.com",  
        "treyresearch.net",  
        "karen@proseware.com"  
    };  
  
    Regex^ emailregex = gcnew Regex("(?<user>[^@]+)@(?<host>.+)");  
  
    for (int i=0; i<address->Length; i++)  
    {  
        Match^ m = emailregex->Match( address[i] );  
        Console::Write("\n{0,25}", address[i]);  
  
        if ( m->Success )   
        {  
            Console::Write("   User='{0}'",   
            m->Groups["user"]->Value);  
            Console::Write("   Host='{0}'",   
            m->Groups["host"]->Value);  
        }  
        else   
            Console::Write("   (invalid email address)");  
        }  
  
    Console::WriteLine("");  
    return 0;  
}  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Reguläre Ausdrücke von .NET Framework](/dotnet/standard/base-types/regular-expressions)   
 [.NET-Programmierung mit C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)