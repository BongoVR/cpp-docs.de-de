---
title: '/ Zc: strictstrings (Zeichenfolgenliteral-typkonvertierung deaktivieren) | Microsoft Docs'
ms.custom: ''
ms.date: 03/06/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /Zc:strictStrings
- strictStrings
dev_langs:
- C++
helpviewer_keywords:
- /Zc:strictStrings
- -Zc compiler options (C++)
- strictStrings
- /Zc compiler options (C++)
- Zc compiler options (C++)
ms.assetid: b7eb3f3b-82c1-48a2-8e63-66bad7397b46
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7025a4bae2d4a7474cb366b041a3c62f3d7db819
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="zcstrictstrings-disable-string-literal-type-conversion"></a>/Zc:strictStrings (Zeichenfolgenliteral-Typkonvertierung deaktivieren)

Wenn dies angegeben wird, benötigt der Compiler eine strenge `const`-Qualifikationsübereinstimmung für Zeiger, die mithilfe von Zeichenfolgenliteralen initialisiert werden.

## <a name="syntax"></a>Syntax

> **/Zc:strictStrings**[**-**]

## <a name="remarks"></a>Hinweise

Wenn **/Zc: strictstrings** angegeben ist, erzwingt der Compiler die standardmäßigen C++ `const` -Qualifikationen für Zeichenfolgenliterale als Typ "Array von `const char`" oder "Array von `const wchar_t`", je nachdem, in der Deklaration. Zeichenfolgenliterale sind unveränderlich. Der Versuch, den Inhalt von einem von ihnen zu ändern, führt zu einem Zugriffsverletzungsfehler in der Laufzeit. Sie müssen einen Zeichenfolgenzeiger als `const` deklarieren, um ihn mithilfe eines Zeichenfolgenliterals zu initialisieren, oder sie müssen eine explizite `const_cast` verwenden, um einen Zeiger zu initialisieren, der nicht `const` ist. Standardmäßig oder wenn **/Zc:strictStrings-** angegeben ist, wird der Compiler erzwingt keine der standardmäßigen C++ `const` Qualifikationen für Zeichenfolgenzeiger mithilfe von Zeichenfolgenliteralen initialisiert werden.

Die **/Zc: strictstrings** Option ist standardmäßig deaktiviert. Die [/ liberalen-](permissive-standards-conformance.md) Compileroption legt implizit diese Option, jedoch können sie mithilfe von außer Kraft gesetzt werden **/Zc:strictStrings-**.

Verwenden der **/Zc: strictstrings** Option aus, um zu verhindern, dass bei der Kompilierung von fehlerhaftem Code. Dieses Beispiel zeigt, wie ein einfacher Deklarationsfehler zu einem Absturz während der Laufzeit führt:

```cpp
// strictStrings_off.cpp
// compile by using: cl /W4 strictStrings_off.cpp
int main() {
   wchar_t* str = L"hello";
   str[2] = L'a'; // run-time error: access violation
}
```

Wenn **/Zc: strictstrings** ist aktiviert, meldet der gleiche Code einen Fehler in der Deklaration des `str`.

```cpp
// strictStrings_on.cpp
// compile by using: cl /Zc:strictStrings /W4 strictStrings_on.cpp
int main() {
   wchar_t* str = L"hello"; // error: Conversion from string literal
   // loses const qualifier
   str[2] = L'a';
}
```

Wenn Sie `auto` verwenden, um einen Zeichenfolgenzeiger zu deklarieren, erstellt der Compiler die richtige `const` Zeigertypdeklaration für Sie. Ein Versuch, den Inhalt eines `const`-Zeigers zu ändern, wird vom Compiler als Fehler gemeldet.

> [!NOTE]
> Der C++-Standardbibliothek in [!INCLUDE[cpp_dev12_long](../../build/reference/includes/cpp_dev12_long_md.md)] unterstützt nicht die **/Zc: strictstrings** -Compileroption in Debugversionen erstellt. Wenn Sie mehrere finden Sie unter [C2665](../../error-messages/compiler-errors-2/compiler-error-c2665.md) Fehler in Ihrem Build ausgeben, kann dies die Ursache sein.

Weitere Informationen über Konformitätsprobleme in Visual C++ finden Sie unter [Nonstandard Behavior](../../cpp/nonstandard-behavior.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Compileroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [arbeiten mit Projekteigenschaften](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Konfigurationseigenschaften** > **C/C++-** > **Befehlszeile** Eigenschaftenseite.

1. Ändern der **Zusatzoptionen** Eigenschaft einschließen **/Zc: strictstrings** und wählen Sie dann **OK**.

## <a name="see-also"></a>Siehe auch

[/Zc (Übereinstimmung)](../../build/reference/zc-conformance.md)<br/>
