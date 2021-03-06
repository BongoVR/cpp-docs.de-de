---
title: Mit C++-Interop (implizites PInvoke) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- blittable types [C++]
- platform invoke [C++], implicit
- interop [C++], features
- data marshaling [C++], C++ Interop features
- porting [C++], C++ native to .NET
- COM interfaces [C++]
- implicit platform invoke
- examples [C++], interoperability
- types [C++], blittable
- marshaling [C++], C++ Interop features
- platform invoke [C++], examples
- interoperability [C++]
- C++ Interop
- interoperability [C++], Implicit PInvoke
- C++, interop
- C++ COM Interop
- .NET [C++], porting C++ native to
ms.assetid: 5f710bf1-88ae-4c4e-8326-b3f0b7c4c68a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: a91c9833358744730b9ad9c63f5a14729d9d0968
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="using-c-interop-implicit-pinvoke"></a>Verwenden von C++-Interop (implizites PInvoke)
Im Gegensatz zu anderen Sprachen .NET Visual C++ bietet interoperabilitätsunterstützung, die verwalteten und nicht verwalteten Code vorhanden sein, in der gleichen Anwendung und sogar in der gleichen Datei ermöglicht (mit der [verwaltete, unverwaltete](../preprocessor/managed-unmanaged.md) Pragmas). Auf diese Weise können Visual C++-Entwickler .NET-Funktionalität in vorhandene Visual C++-Anwendungen integrieren, ohne den Rest der Anwendung zu beeinträchtigen.  
  
 Sie können auch nicht verwaltete Funktionen aufrufen, aus einer verwalteten Kompiliereinheit mit [Dllexport, Dllimport](../cpp/dllexport-dllimport.md).  
  
 Implizites PInvoke ist sinnvoll, wenn Sie das Marshalling von Funktionsparametern oder andere Details, die bei einem expliziten Aufruf von DllImportAttribute angegeben werden können, nicht festlegen müssen.  
  
 Visual C++ bietet zwei Möglichkeiten für die Interoperation von verwalteten und nicht verwalteten Funktionen:  
  
-   [Verwenden von explizitem PInvoke in C++ (DllImport-Attribut)](../dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute.md)  
  
 Explizites PInvoke wird von .NET Framework unterstützt und ist in den meisten .NET-Sprachen verfügbar. Doch wie der Name schon sagt, ist C++-Interop Visual C++-spezifisch.  
  
## <a name="c-interop"></a>C++ Interop  
 C++-Interop wird gegenüber explizitem PInvoke empfohlen, da es bessere Typsicherheit bietet, normalerweise einfacher zu implementieren ist, sich bei Änderungen der nicht verwalteten API leichter handhaben lässt und Leistungsverbesserungen erlaubt, die mit explizitem PInvoke nicht möglich sind. C++-Interop ist allerdings nicht möglich, wenn der nicht verwaltete Quellcode nicht verfügbar ist.  
  
## <a name="c-com-interop"></a>C++-COM-Interop  
 Die von Visual C++ unterstützten Interoperabilitätsfunktionen bieten einen besonderen Vorteil gegenüber anderen .NET-Sprachen, wenn es um die Interoperation mit COM-Komponenten geht. Keine Beschränkung auf die Einschränkungen von .NET Framework [Tlbimp.exe (Type Library Importer-Tool)](/dotnet/framework/tools/tlbimp-exe-type-library-importer), z. B. eingeschränkte Unterstützung für Datentypen und die erforderliche Offenlegung von jedes Mitglied jeder COM-Schnittstelle, C++-Interop ermöglicht es COM Komponenten am Zugriff auf und erfordert keine separate Interop-Assemblys. Weitere Informationen finden Sie unter [Using COM aus .NET](http://msdn.microsoft.com/en-us/03976661-6278-4227-a6c1-3b3315502c15).  
  
## <a name="blittable-types"></a>Blitfähige Typen  
 Für nicht verwaltete APIs, die einfache, systeminterne Typen verwenden (siehe [blitfähige und nicht blitfähige Typen](http://msdn.microsoft.com/Library/d03b050e-2916-49a0-99ba-f19316e5c1b3)), keine besondere Codierung ist erforderlich, da diese Datentypen die gleiche Darstellung im Arbeitsspeicher haben, aber eine komplexere Datentypen ist erforderlich, explizite Daten-Marshalling. Ein Beispiel finden Sie unter [Vorgehensweise: Aufrufen von systemeigenen DLLs aus verwaltetem Code mithilfe von PInvoke](../dotnet/how-to-call-native-dlls-from-managed-code-using-pinvoke.md).  
  
## <a name="example"></a>Beispiel  
  
```  
// vcmcppv2_impl_dllimp.cpp  
// compile with: /clr:pure user32.lib  
using namespace System::Runtime::InteropServices;  
  
// Implicit DLLImport specifying calling convention  
extern "C" int __stdcall MessageBeep(int);  
  
// explicit DLLImport needed here to use P/Invoke marshalling because  
// System::String ^ is not the type of the first parameter to printf  
[DllImport("msvcrt.dll", EntryPoint = "printf", CallingConvention = CallingConvention::Cdecl,  CharSet = CharSet::Ansi)]  
// or just  
// [DllImport("msvcrt.dll")]  
int printf(System::String ^, ...);   
  
int main() {  
   // (string literals are System::String by default)  
   printf("Begin beep\n");  
   MessageBeep(100000);  
   printf("Done\n");  
}  
```  
  
```Output  
Begin beep  
Done  
```  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
  
-   [Vorgehensweise: Marshallen von ANSI-Zeichenfolgen mit C++-Interop](../dotnet/how-to-marshal-ansi-strings-using-cpp-interop.md)  
  
-   [Vorgehensweise: Marshallen von Unicode-Zeichenfolgen mit C++-Interop](../dotnet/how-to-marshal-unicode-strings-using-cpp-interop.md)  
  
-   [Vorgehensweise: Marshallen von COM-Zeichenfolgen mit C++-Interop](../dotnet/how-to-marshal-com-strings-using-cpp-interop.md)  
  
-   [Vorgehensweise: Marshallen von Strukturen mit C++-Interop](../dotnet/how-to-marshal-structures-using-cpp-interop.md)  
  
-   [Vorgehensweise: Marshallen von Arrays mit C++-Interop](../dotnet/how-to-marshal-arrays-using-cpp-interop.md)  
  
-   [Vorgehensweise: Marshallen von Rückrufen und Delegaten mit C++-Interop](../dotnet/how-to-marshal-callbacks-and-delegates-by-using-cpp-interop.md)  
  
-   [Vorgehensweise: Marshallen von eingebetteten Zeigern mit C++-Interop](../dotnet/how-to-marshal-embedded-pointers-using-cpp-interop.md)  
  
-   [Vorgehensweise: Zugriff auf Zeichen in einem System::String](../dotnet/how-to-access-characters-in-a-system-string.md)  
  
-   [Vorgehensweise: Umwandeln von char * String nach System::Byte Array](../dotnet/how-to-convert-char-star-string-to-system-byte-array.md)  
  
-   [Vorgehensweise: Konvertieren von System:: String nach Wchar_t * oder Char\*](../dotnet/how-to-convert-system-string-to-wchar-t-star-or-char-star.md)  
  
-   [Vorgehensweise: Konvertieren von System::String zu Standardzeichenfolge](../dotnet/how-to-convert-system-string-to-standard-string.md)  
  
-   [Vorgehensweise: Konvertieren einer Standardzeichenfolge nach System::String](../dotnet/how-to-convert-standard-string-to-system-string.md)  
  
-   [Vorgehensweise: Abrufen eines Zeigers auf ein Byte-Array](../dotnet/how-to-obtain-a-pointer-to-byte-array.md)  
  
-   [Vorgehensweise: Laden von nicht verwalteten Ressourcen in ein Byte-Array](../dotnet/how-to-load-unmanaged-resources-into-a-byte-array.md)  
  
-   [Vorgehensweise: Ändern der Verweisklasse in einer nativen Funktion](../dotnet/how-to-modify-reference-class-in-a-native-function.md)  
  
-   [Vorgehensweise: Ermitteln, ob ein Bild nativ oder CLR ist](../dotnet/how-to-determine-if-an-image-is-native-or-clr.md)  
  
-   [Vorgehensweise: Hinzufügen einer nativen DLL zum globalen Assemblycache](../dotnet/how-to-add-native-dll-to-global-assembly-cache.md)  
  
-   [Vorgehensweise: Verweis auf Werttyp in nativem Typ](../dotnet/how-to-hold-reference-to-value-type-in-native-type.md)  
  
-   [Vorgehensweise: Objektverweis in nicht verwaltetem Arbeitsspeicher](../dotnet/how-to-hold-object-reference-in-unmanaged-memory.md)  
  
-   [Vorgehensweise: Erkennen von/CLR-Kompilierung](../dotnet/how-to-detect-clr-compilation.md)  
  
-   [Vorgehensweise: Konvertieren zwischen System::Guid und _GUID](../dotnet/how-to-convert-between-system-guid-and-guid.md)  
  
-   [Vorgehensweise: Angeben eines out-Parameters](../dotnet/how-to-specify-an-out-parameter.md)  
  
-   [Vorgehensweise: Verwenden eines systemeigenen Typs in einer/CLR-Kompilierung](../dotnet/how-to-use-a-native-type-in-a-clr-compilation.md)  
  
-   [Vorgehensweise: Deklarieren von Handles in nativen Typen](../dotnet/how-to-declare-handles-in-native-types.md)  
  
-   [Vorgehensweise: Kapseln einer nativen Klasse zur Verwendung in C#](../dotnet/how-to-wrap-native-class-for-use-by-csharp.md)  
  
 Informationen zum Verwenden von Delegaten in einem Interop-Szenario finden Sie unter [Delegate (Komponentenerweiterungen für C++)](../windows/delegate-cpp-component-extensions.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Aufrufen nativer Funktionen aus verwaltetem Code](../dotnet/calling-native-functions-from-managed-code.md)