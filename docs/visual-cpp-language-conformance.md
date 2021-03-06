---
title: Visual C++-Sprachkonformität | Microsoft-Dokumentation
ms.date: 11/15/2017
ms.technology:
- cpp-language
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 475da6e9-0d78-4b4e-bd23-f41c406c4efe
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 722b1dadbdd5e1855ea8d8cc163de705f3e2cbcd
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="visual-c-language-conformance"></a>Visual C++-Sprachkonformität

Dieses Thema bietet einen Überblick über die Konformität von Compiler- und Standardbibliotheksfeatures des C++-Compilers in Visual Studio 2017 und früheren Versionen mit den Sprachstandards ISO C++03, C++11, C++14, C++17 und dem Entwurf von C++20. Jeder Name eines Features im Compiler und in der Standardbibliothek verweist auf das ISO C++-Standardvorschlagsdokument, in dem das Feature beschrieben ist, falls zum Zeitpunkt der Veröffentlichung ein solches Dokument verfügbar ist. Die Spalte „Supported“ (Unterstützt) listet die Visual Studio-Version auf, in der die Unterstützung für die Funktion zum ersten Mal aufgetreten ist.

Informationen zu Kompatibilitätsverbesserungen und anderen Änderungen in Visual Studio 2017 finden Sie unter [Verbesserungen bei der Übereinstimmung mit C++-Standards in Visual C++ 2017](cpp-conformance-improvements-2017.md) und [Neuerungen bei Visual C++ in Visual Studio 2017](what-s-new-for-visual-cpp-in-visual-studio.md). Kompatibilitätsänderungen in früheren Versionen finden Sie unter [Änderungsverlauf von Visual C++ von 2003 bis 2015](porting/visual-cpp-change-history-2003-2015.md) und [Visual C++ What's New 2003 through 2015](porting/visual-cpp-what-s-new-2003-through-2015.md) (Visual C++ – Neuerungen von 2003 bis 2015). Aktuelle Nachrichten vom C++-Team finden Sie im [Visual C++-Teamblog](https://blogs.msdn.microsoft.com/vcblog/).

> [!NOTE]
> Es gibt keine binären Änderungen von Visual Studio 2015 auf Visual Studio 2017.

## <a name="compiler-features"></a>Compilerfunktionen

|Bereich „Funktionen“| |
|----|---|
|__Funktionen der C++03/11-Kernsprache__|__Unterstützt__|
|&nbsp;&nbsp;Alles andere|VS 2015 <sup>[A](#note_A)</sup>|
|&nbsp;&nbsp;Zwei-Phasen Namenssuche|Teilweise <sup>[B](#note_B)</sup>|
|&nbsp;&nbsp;[N2634 SFINAE für Ausdrücke](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2008/n2634.html)|Teilweise <sup>[C](#note_C)</sup>|
|&nbsp;&nbsp;[N1653 C99-Präprozessor](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2004/n1653.htm)|Teilweise <sup>[D](#note_D)</sup>|
|&nbsp;&nbsp;[N1988 Erweiterte Ganzzahltypen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2006/n1988.pdf)|Nicht zutreffend <sup>[E](#note_E)</sup>|
|__Funktionen der C++14-Kernsprache__|__Unterstützt__|
|&nbsp;&nbsp;[N3323 Optimierte Formulierungen für kontextbezogene Konvertierungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3323.pdf)|VS 2013|
|&nbsp;&nbsp;[N3472 Binäre Literale](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3472.pdf)|VS 2015|
|&nbsp;&nbsp;[N3638 Rückagebetypen „auto“ und „decltype(auto)“](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3638.html)|VS 2015|
|&nbsp;&nbsp;[N3648 init-captures](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3648.html)|VS 2015|
|&nbsp;&nbsp;[N3649 Generische Lambda-Ausdrücke](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3649.html)|VS 2015|
|&nbsp;&nbsp;[N3760 [[veraltet]]-Attribute](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3760.html)|VS 2015|
|&nbsp;&nbsp;[N3778 Zuordnungsaufhebung mit Größenangabe](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3778.html)|VS 2015|
|&nbsp;&nbsp;[N3781 Zahlentrennzeichen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3781.pdf)|VS 2015|
|&nbsp;&nbsp;[N3651 Variablenvorlagen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3651.pdf)|VS 2015.2|
|&nbsp;&nbsp;[N3652 Erweiterte constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3652.html)|VS 2017|
|&nbsp;&nbsp;[N3653 NSDMIs für Aggregate](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3653.html)|VS 2017|
|&nbsp;&nbsp;[N3664 Zuordnungen vermeiden/zusammenführen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3664.html)|Nicht zutreffend <sup>[F](#note_F)</sup>|
|__Funktionen der C++17-Kernsprache__|__Unterstützt__|
|&nbsp;&nbsp;[N4086 Entfernen von Trigraphen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4086.html)|VS 2010 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N3922 Neue Regeln für „auto“ mit „braced-init-lists“](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3922.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4051 „typename“ in Vorlagen-Vorlagenparametern](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4051.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4266 Attribute für Namespaces und Enumeratoren](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4266.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4267 u8-Zeichenliterale](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4267.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4230 Geschachtelte Namespacedefinitionen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4230.html)|VS 2015.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N3928 Knappes static_assert](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3928.pdf)|VS 2017 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0184R0 Generalisierte bereichsbasierte for-Schleifen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0184r0.html)|VS 2017 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0188R1 [[fallthrough]]-Attribut](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0188r1.pdf)|VS 2017 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0001R1 Entfernen des register-Schlüsselworts](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0001r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0002R1 Entfernen von operator++ für bool](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0002r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0018R3 *dies nach Wert erfassen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0018r3.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0028R4 Verwenden des Attribut Namespaces ohne Wiederholung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0028r4.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0061R1 __has_include](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0061r1.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0138R2 Direct-Liste-Init von festen Enumerationen von Ganzzahlen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0138r2.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0170R1 constexpr-Lambdas](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0170r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0189R1 [[nodiscard]]-Attribut](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0189r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0212R1 [[maybe_unused]]-Attribut](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0212r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0217R3 Strukturierte Bindungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0217r3.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0292R2 constexpr if-Anweisung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0292r2.html)|VS 2017 15.3 <sup>[G](#note_G)</sup>|
|&nbsp;&nbsp;[P0305R1 Auswahlanweisungen mit Initialisierern](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0305r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0245R1 Hexfloat-Literale](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0245r1.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N4268 Mehr Nicht-Typen-Vorlagenargumente erlauben](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4268.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N4295 Fold-Ausdrücke](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4295.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0003R5 Entfernen von dynamischen Ausnahmespezifikationen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0003r5.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0012R1 noexcept zum Typsystem hinzufügen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0012r1.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0035R4 Über-ausgerichtete dynamische Speicherbelegung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0035r4.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0386R2 Inline-Variablen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0386r2.pdf)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0522R0 Übereinstimmender template-Vorlagenparameter zu kompatiblen Argumenten](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0522r0.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0036R0 Entfernen einiger leerer unärer Folds](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0036r0.pdf)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N4261 Qualifikationskonvertierungen beheben](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4261.html)|Nein|
|&nbsp;&nbsp;[P0017R1 Erweiterte ungültige Aggregatinitialisierung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0017r1.html)|Nein|
|&nbsp;&nbsp;[P0091R3 Vorlagenargumentableitung für Klassenvorlagen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0091r3.html)<br />&nbsp;&nbsp;[P0512R0 Probleme mit der Argumentableitung für Klassenvorlagen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0512r0.pdf)|Nein|
|&nbsp;&nbsp;[P0127R2 Deklarieren von Nichttyp-Vorlagenparameter mit auto](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0127r2.html)|Nein|
|&nbsp;&nbsp;[P0135R1 Garantierte copy elision](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0135r1.html)|Nein <sup>[H](#note_H)</sup>|
|&nbsp;&nbsp;[P0136R1 Umformulierung der Konstruktorvererbung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0136r1.html)|Nein|
|&nbsp;&nbsp;[P0145R3 Reihenfolge der Ausdrucksauswertung optimieren](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0145r3.pdf)<br />&nbsp;&nbsp;[P0400R0 Auswertungsreihenfolge von Funktionsargumenten](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0400r0.html)|Nein|
|&nbsp;&nbsp;[P0195R2 Pack-Erweiterungen in der using-Deklarationen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0195r2.html)|Nein|
|&nbsp;&nbsp;[P0283R2 Ignoriert nicht erkannte Attribute](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0283r2.html)|Nein|
|&nbsp;&nbsp;[P0702R1 Beheben von Problemen mit der Argumentableitung für Klassenvorlagen für „initializer-list ctors“](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0702r1.html)|Nein|
|__C++20-Kernsprachfunktionen__|__Unterstützt__|
|&nbsp;&nbsp;[P0306R4 Hinzufügen von &#95;&#95;VA_OPT&#95;&#95; für das Auslassen und Löschen von Kommas](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0306r4.pdf)|Nein|
|&nbsp;&nbsp;[P0329R4 Designierte Initialisierung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0329r4.pdf)|Nein|
|&nbsp;&nbsp;[P0409R2 Zulassen von „lambda-capture [=, this]“](http://open-std.org/JTC1/SC22/WG21/docs/papers/2017/p0409r2.html)|Nein|
|&nbsp;&nbsp;[P0428R2 Bekannte Vorlagensyntax für generische Lambdas](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0428r2.pdf)|Nein|
|&nbsp;&nbsp;[P0683R1 Standardmemberinitialisierer für „bit-fields“](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0683r1.html)|Nein|
|&nbsp;&nbsp;[P0704R1 Beheben von „const lvalue ref“-qualifizierten Zeigern auf Member](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0704r1.html)|Nein|
|&nbsp;&nbsp;[P0734R0 Konzepte](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0734r0.pdf)|Nein|


## <a name="standard-library-features"></a>Standardbibliotheksfeatures

|Bereich „Funktionen“| |
|---|---|
|__C++20-Standardbibliotheksfunktionen__|__Unterstützt__|
|&nbsp;&nbsp;[P0463R1 Endian](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0463r1.html)|Nein|
|&nbsp;&nbsp;[P0674R1 „make_shared()“ für Arrays](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0674r1.html)|Nein|
|__C++17 Standardbibliotheksfunktionen__|__Unterstützt__|
|&nbsp;&nbsp;[P0433R2 Integrieren der Vorlagenableitung für Klassenvorlagen in die Standardbibliothek](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0433r2.html)<br />&nbsp;&nbsp;[P0739R0 Verbessern der Integration der Argumentableitung für Klassenvorlagen in die Standardbibliothek](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0739r0.html)|Nein|
|&nbsp;&nbsp;[P0426R1 constexpr für char_traits](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0426r1.html)|Nein|
|&nbsp;&nbsp;[P0030R1 hypot(x, y, z)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0030r1.pdf)|Nein|
|&nbsp;&nbsp;[P0220R1 Bibliotheksgrundlagen V1](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0220r1.html)|Teilweise <sup>[J](#note_J)</sup>|
|&nbsp;&nbsp;[P0067R5 Elementare Zeichenfolgenkonvertierungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0067r5.html)|Nein|
|&nbsp;&nbsp;[N4562 Bibliotheksgrundlagen: \<memory_resource >](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#memory.resource.synop)<br />&nbsp;&nbsp;[P0337R0 Löschen der polymorphic_allocator-Zuweisung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0337r0.html)|Nein|
|&nbsp;&nbsp;[P0024R2 Parallele Algorithmen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0024r2.html)<br />&nbsp;&nbsp;[P0336R1 Umbenennen der Richtlinien für parallele Ausführung](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0336r1.pdf)<br />&nbsp;&nbsp;[P0394R4 Parallele Algorithmen müssen bei Ausnahmefehlern „terminate()“ aufrufen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0394r4.html)<br />&nbsp;&nbsp;[P0452R1 Vereinheitlichen von parallelen \<numeric>-Algorithmen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0452r1.html)|Nein|
|&nbsp;&nbsp;[P0226R1 Mathematische spezielle Funktionen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0226r1.pdf)|Nein|
|&nbsp;&nbsp;[P0218R1 \<filesystem>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0218r1.html)<br />&nbsp;&nbsp;[P0219R1 Relative Pfade für Dateisystem](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0219r1.html)<br />&nbsp;&nbsp;[P0317R1 Zwischenspeichern von Verzeichniseinträgen für Dateisystem](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p03179r1.html)<br />&nbsp;&nbsp;[P0392R0 Unterstützung von string_view in Dateisystempfaden](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0392r0.pdf)<br />&nbsp;&nbsp;[P0430R2 Unterstützung von Nicht-POSIX-Dateisystemen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0430r2.pdf)<br />&nbsp;&nbsp;[P0492R2 Auflösen von NB-Kommentaren für Dateisystem](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0492r2.html)|Nein <sup>[K](#note_K)</sup>|
|&nbsp;&nbsp;[P0003R5 Entfernen von dynamischen Ausnahmespezifikationen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0003r5.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0005R4 not_fn()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0005r4.html)<br />&nbsp;&nbsp;[P0358R1 Korrekturen für not_fn()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0358r1.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0033R1 enable_shared_from_this umformulieren](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0033r1.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0083R3 Zusammenführen von Zuordnungen und Festlegungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0083r3.pdf)<br />&nbsp;&nbsp;[P0508R0 insert_return_type klarstellen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0508r0.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0174R2 Veraltete rudimentäre Bibliotheksteile](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0174r2.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0302R1 Entfernen der Unterstützung für Zuweisung in std::function](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0302r1.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0414R2 shared_ptr\<T[]>, shared_ptr\<T[N]>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0414r2.html)<br />&nbsp;&nbsp;[P0497R0 Beheben von shared_ptr für Arrays](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0497r0.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0521R0 Veraltete shared_ptr::unique()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0521r0.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0607R0 Inlinevariablen für die Standardbibliothek](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0607r0.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0618R0 Kennzeichnen von „\<codecvt>“ als veraltet](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0618r0.html)|VS 2017 15.5 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N4562 Bibliotheksgrundlagen: Boyer-Moore-Suche()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#func.searchers.boyer_moore)<br/>&nbsp;&nbsp;[P0253R1 Beheben der Suchprogramm-Rückgabetypen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0253r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0031R0 constexpr für \<array> (erneut) und \<iterator>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0031r0.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0040R3 Erweitern von Speicher-Verwaltungstools](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0040r3.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0084R2 Emplace-Rückgabetyp](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0084r2.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0152R1 atomic::is_always_lock_free](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0152r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0154R1 hardware_destructive_interference_size, usw.](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0154r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0156R2 Umbenennen von „Variadic lock\_guard“ in „scoped\_lock“](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0156r2.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0258R2 has_unique_object_representations](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0258r2.html)|VS 2017 15.3 <sup>[L](#note_L)</sup>|
|&nbsp;&nbsp;[P0295R0 gcd(), lcm()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0295r0.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0298R3 std::byte](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0298r3.pdf)|VS 2017 15.3 <sup>[17](#note_17), [byte](#note_byte)</sup>|
|&nbsp;&nbsp;[P0403R1 UDLs für \<string_view> ("meow"sv, usw.)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0403r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0418R2 atomic compare_exchange memory_order-Anforderungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0418r2.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0435R1 common_type überholen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0435r1.pdf)<br />&nbsp;&nbsp;[P0548R1 Anpassung von „common\_type“ und „duration“](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0548r1.pdf)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0505R0 constexpr für \<chrono> (erneut)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0505r0.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0513R0 Hashwerte verfälschen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0513r0.pdf)<br />&nbsp;&nbsp;[P0599R1 noexcept-Hash](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0599r1.pdf)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0516R0 Kopieren von shared_future als noexcept markieren](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0516r0.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0517R0 future_error aus future_errc erstellen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0517r0.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0558R1 Auflösen von Inkonsistenzen in benannten atomic<T>-Basisklassen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0558r1.pdf)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0604R0 Ändern von „is\_callable/result\_of“ in „invoke\_result“, „is\_invocable“, „is\_nothrow\_invocable“](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0604r0.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N4562 Bibliotheksgrundlagen: \<algorithm> sample()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#alg.random.sample)|VS 2017|
|&nbsp;&nbsp;[N4562 Bibliotheksgrundlagen: \<any>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#any)|VS 2017|
|&nbsp;&nbsp;[N4562 Bibliotheksgrundlagen: \<optional>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#optional)|VS 2017|
|&nbsp;&nbsp;[N4562 Bibliotheksgrundlagen: \<string_view>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#string.view)|VS 2017|
|&nbsp;&nbsp;[N4562 Bibliotheksgrundlagen: \<tuple> apply()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#tuple)|VS 2017|
|&nbsp;&nbsp;[P0032R3 Homogene Schnittstelle für variant/any/optional](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0032r3.pdf)|VS 2017|
|&nbsp;&nbsp;[P0077R2 is_callable, is_nothrow_callable](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0077r2.html)|VS 2017|
|&nbsp;&nbsp;[P0088R3 \<variant>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0088r3.html)|VS 2017|
|&nbsp;&nbsp;[P0163R0 shared_ptr::weak_type](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0163r0.html)|VS 2017|
|&nbsp;&nbsp;[P0209R2 make_from_tuple()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0209r2.pdf)|VS 2017|
|&nbsp;&nbsp;[P0254R2 string_view und std::string integrieren](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0254r2.pdf)|VS 2017|
|&nbsp;&nbsp;[P0307R2 Optional wieder größer gleich machen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0307r2.pdf)|VS 2017|
|&nbsp;&nbsp;[P0393R3 Variant größer gleich machen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0393r3.html)|VS 2017|
|&nbsp;&nbsp;[P0504R0 Erneute Betrachtung von in_place_t/in_place_type_t\<T>/in_place_index_t\<I>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0504r0.html)|VS 2017|
|&nbsp;&nbsp;[P0510R0 Ablehnen von Varianten von Nothing, Arrays, Verweisen und unvollständigen Typen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0510r0.html)|VS 2017|
|&nbsp;&nbsp;[P0025R1 clamp()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0025r1.html)|VS 2015.3|
|&nbsp;&nbsp;[P0185R1 is_swappable, is_nothrow_swappable](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0185r1.html)|VS 2015.3|
|&nbsp;&nbsp;[P0272R1 Non-const basic_string::data()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0272r1.html)|VS 2015.3|
|&nbsp;&nbsp;[N4387 Verbessern von pair und tuple](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4387.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4508 shared_mutex (nicht zeitgesteuert)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4508.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0004R1 Veraltete Iostreams-Aliase entfernen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0004r1.html)|VS 2015.2 <sup>[rem](#note_rem)</sup>|
|&nbsp;&nbsp;[P0006R0 Variable Vorlagen für Typmerkmale (is_same_v, usw.).](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0006r0.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0007R1 as_const()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0007r1.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0013R1 Typmerkmale von logischen Operatoren (conjunction, usw.).](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0013r1.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0074R0 owner_less\<>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0074r0.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0092R1 \<chrono> floor(), ceil(), round(), abs()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0092r1.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0156R0 Variadic lock_guard](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0156r0.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N3911 void_t](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3911.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4089 Sichere Konvertierungen in unique_ptr\<T[]>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4089.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4169 invoke()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4169.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4190 Entfernen von auto_ptr, random_shuffle(), und altem \<functional> Stuff](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4190.htm)|VS 2015 <sup>[rem](#note_rem)</sup>|
|&nbsp;&nbsp;[N4258 noexcept-Bereinigungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4258.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4259 uncaught_exceptions()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4259.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4277 Einfach kopierbare reference_wrapper](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4277.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4279 insert_or_assign()/try_emplace() für map/unordered_map](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4279.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4280 size(), empty(), data()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4280.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4366 Exakt eingeschränkte unique_ptr-Zuweisungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4366.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4389 bool_constant](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4389.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0063R3 C11-Standardbibliothek](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0063r3.html)|VS 2015 <sup>[C11](#note_C11), [14](#note_14)</sup>|
|&nbsp;&nbsp;[N4510 Unterstützung von unvollständigen Typen in vector/list/forward_list](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4510.html)|VS 2013 <sup>[14](#note_14)</sup>|
|__C++14 Standardbibliotheksfunktionen__|__Unterstützt__|
|&nbsp;&nbsp;[N3462 SFINAE-freundliche result_of](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3462.html)|VS 2015.2|
|&nbsp;&nbsp;[N3302 constexpr für \<complex>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2011/n3302.html)|VS 2015|
|&nbsp;&nbsp;[N3469 constexpr für \<chrono>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3469.html)|VS 2015|
|&nbsp;&nbsp;[N3470 constexpr für \<array>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3470.html)|VS 2015|
|&nbsp;&nbsp;[N3471 constexpr für \<initializer_list>, \<tuple>, \<utility>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3471.html)|VS 2015|
|&nbsp;&nbsp;[N3545 integral_constant::operator()()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3545.pdf)|VS 2015|
|&nbsp;&nbsp;[N3642 UDLs für \<chrono>, \<string> (1729ms, „meow“s, usw.)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3642.pdf)|VS 2015|
|&nbsp;&nbsp;[N3644 NULL-Forward-Iteratoren](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3644.pdf)|VS 2015|
|&nbsp;&nbsp;[N3654 quoted()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3654.html)|VS 2015|
|&nbsp;&nbsp;[N3657 Heterogenes assoziatives Nachschlagen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3657.htm)|VS 2015|
|&nbsp;&nbsp;[N3658 integer_sequence](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3658.html)|VS 2015|
|&nbsp;&nbsp;[N3659 shared_mutex (zeitgesteuert)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3659.html)|VS 2015|
|&nbsp;&nbsp;[N3668 exchange()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3668.html)|VS 2015|
|&nbsp;&nbsp;[N3669 constexpr-Memberfunktionen ohne const beheben](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3669.pdf)|VS 2015|
|&nbsp;&nbsp;[N3670 get\<T>()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3670.html)|VS 2015|
|&nbsp;&nbsp;[N3671 Zweibereich equal(), is_permutation(), mismatch()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3671.html)|VS 2015|
|&nbsp;&nbsp;[N3778 Zuordnungsaufhebung mit Größenangabe](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3778.html)|VS 2015|
|&nbsp;&nbsp;[N3779 UDLs für \<complex> (3.14i, usw.)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3779.pdf)|VS 2015|
|&nbsp;&nbsp;[N3789 constexpr für \<functional>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3789.htm)|VS 2015|
|&nbsp;&nbsp;[N3887 tuple_element_t](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3887.pdf)|VS 2015|
|&nbsp;&nbsp;[N3891 Umbenennen von shared_mutex (zeitgesteuert) in shared_timed_mutex](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3891.htm)|VS 2015|
|&nbsp;&nbsp;[N3346 Minimale Containerelement-Anforderungen](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3346.pdf)|VS 2013|
|&nbsp;&nbsp;[N3421 Transparente Operatorfunktionselemente (less\<>, usw.)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3421.htm)|VS 2013|
|&nbsp;&nbsp;[N3655 Alias-Vorlagen für \<type_traits> (decay_t, usw.)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3655.pdf)|VS 2013|
|&nbsp;&nbsp;[N3656 make_unique()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3656.htm)|VS 2013|
|&nbsp;&nbsp;[N3924 Abschreckendes rand()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3924.pdf)|Nicht zutreffend|

Eine Gruppe von Dokumenten in einer Liste gibt an, dass eine Funktion in den Standard gewählt wurde, und anschließend wurden auch ein oder mehrere Dokumente zum Verbessern oder Erweitern dieser Funktion gewählt. Diese Funktionen werden zusammen implementiert.

### <a name="supported-values"></a>Unterstützte Werte

__Nein__bedeutet noch nicht implementiert.  
__Teilweise__ bedeutet, dass die Implementierung in Visual Studio 2017 unvollständig ist. Weitere Informationen finden Sie im Abschnitt „Hinweise“  
__Nicht zutreffend__ bedeutet, dass die Entwicklunsvorschläge keine Funktionen beschreiben. Diese Dokumente haben die Standardsprache geändert, aber keine Arbeit für die Implementierung erstellt. Sie werden hier nur aus Gründen der Vollständigkeit aufgeführt.  
__VS 2010__ gibt Funktionen an, die in Visual Studio 2010 unterstützt werden.  
__VS 2013__ gibt Funktionen an, die in Visual Studio 2013 unterstützt werden.  
__VS 2015__ gibt Funktionen an, die in Visual Studio 2015 RTM unterstützt werden.  
__VS 2015.2__ und __VS 2015.3__ geben Funktionen an, die in Visual Studio 2015 Update 2 und Visual Studio 2015 Update 3 unterstützt werden.  
__VS 2017__ gibt Funktionen an, die in Visual Studio 2017 RTM unterstützt werden.  
__VS 2017 15.3__ gibt Features an, die in Visual Studio 2017 15.3 unterstützt werden.  
__VS 2017 15.5__ gibt Features an, die in Visual Studio 2017 Version 15.5 unterstützt werden.

### <a name="notes"></a>Hinweise

<a name="note_A"></a>__A__ Hierbei werden die dynamischen Ausnahmespezifikationen von C++03 ignoriert, die in C++11 als veraltet gekennzeichnet wurden. Es ist nicht geplant diese zu implementieren, da erwartet wird, dass sie aus einem zukünftigen C++-Standard entfernt werden.  
<a name="note_B"></a>__B__ Die Compilerunterstützung für die Zweiphasen-Namenssuche wurde verbessert, bleibt jedoch unvollständig.  
<a name="note_C"></a>__C__ Die Compilerunterstützung für den SFINAE-Ausdruck ist seit Visual Studio 2015 Update 2 für die Standardbibliothek ausreichend, bleibt jedoch unvollständig.  
<a name="note_D"></a>__D__ Die Compilerunterstützung für C99-Präprozessorregeln ist in Visual Studio 2017 unvollständig. Variadic-Makros werden unterstützt, aber es treten viele Fehler im Verhalten des Präprozessors auf.  
<a name="note_E"></a>__E__ Dies ist als „Nicht zutreffend“ markiert, da Compiler erlaubt, aber nicht erforderlich sind, um erweiterte integer-Typen zu unterstützen.  Wie GCC und Clang haben wir uns entschieden, diese nicht zu unterstützen.  
<a name="note_F"></a>__F__ Dies ist ebenfalls als „Nicht zutreffend“ markiert, da Compiler erlaubt, aber nicht erforderlich sind, um diese Optimierung zu implementieren.  
<a name="note_G"></a>__G__ Unterstützt unter [/std:c++14](./build/reference/std-specify-language-standard-version.md), mit einer unterdrückbaren Warnung.  
<a name="note_H"></a>__H__ Dieses Feature war in der Vorschau von Visual Studio 2017 Version 15.3 verfügbar, wurde aber aus dem Release entfernt, weil Fehler gefunden wurden.  
<a name="note_J"></a>__J__ Features, die in Visual Studio 2015 noch nicht abgeschlossen waren, werden an anderer Stelle in dieser Tabelle aufgeführt.  
<a name="note_K"></a>__K__ Das TS-Dateisystem ist aus historischen Gründen sowohl in „\<experimental/filesystem>“ als auch in „\<filesystem>“ implementiert, aber die Implementierung muss korrigiert werden, bevor der Namespace verschoben wird. Bis dies abgeschlossen ist, wird die Funktion als „noch nicht implementiert“ markiert.  
<a name="note_L"></a>__L__ Unterstützt durch eine intrinsische Compilerfunktion. Diese ist in Clang noch nicht verfügbar. In IntelliSense ist das Feature verfügbar, aber noch nicht aktiviert.   
<a name="note_14"></a>__14__ Diese C++17-Features sind immer aktiviert, auch wenn [/std:c++14](./build/reference/std-specify-language-standard-version.md) (Standard) angegeben ist. Dies kann daran liegen, dass das Feature vor der Einführung der **/std**-Optionen implementiert wurde, oder daran, dass die bedingte Implementierung unerwünscht komplex war.  
<a name="note_17"></a>__17__ Diese Features werden durch die Compileroption [/std:c++17](./build/reference/std-specify-language-standard-version.md) (oder [/std:c++latest](./build/reference/std-specify-language-standard-version.md)) aktiviert.  
<a name="note_byte"></a>__byte__ `std::byte` wird durch [/std:c++17](./build/reference/std-specify-language-standard-version.md) (oder [/std:c++latest](./build/reference/std-specify-language-standard-version.md)) aktiviert, da jedoch in einigen Fällen Konflikte mit den Windows SDK-Headern auftreten können, ist ein differenziertes Makro für die Abwahl vorhanden. Die Deaktivierung erfolgt durch Definieren von `_HAS_STD_BYTE` als `0`.  
<a name="note_C11"></a>__C11__ Die Universal CRT implementierte die Teile der C11-Standardbibliothek, die für C++17 erforderlich sind, mit Ausnahme der `strftime()`-Bezeichner in C99 für die alternative E/O-Konvertierung, dem exklusiven `fopen()`-Modus in C11 und der `aligned_alloc()`-Funktion in C11. Die Implementierung der letztgenannten Funktion ist unwahrscheinlich, da C11 `aligned_alloc()` auf eine Weise angibt, die mit der Microsoft-Implementierung von `free()` nicht kompatibel ist. Insbesondere muss `free()` in der Lage sein, hochgradig ausgerichtete Zuweisungen zu verarbeiten.  
<a name="note_rem"></a>__rem__ Diese Features wurden entfernt, als die Compileroption [/std:c++17](./build/reference/std-specify-language-standard-version.md) (oder [/std:c++latest](./build/reference/std-specify-language-standard-version.md)) angegeben wurde. Diese Features verfügen über Abwahlmakros: `_HAS_AUTO_PTR_ETC`, `_HAS_FUNCTION_ALLOCATOR_SUPPORT`, `_HAS_OLD_IOSTREAMS_MEMBERS` und `_HAS_UNEXPECTED`.
  
## <a name="see-also"></a>Siehe auch

[C++-Programmiersprachenreferenz](cpp/cpp-language-reference.md)  
[C++-Standardbibliothek](standard-library/cpp-standard-library-reference.md)   
[Verbesserungen bei der Übereinstimmung mit C++-Standards in Visual C++ 2017](cpp-conformance-improvements-2017.md)  
[Neues bei Visual C++ in Visual Studio 2017](what-s-new-for-visual-cpp-in-visual-studio.md)  
[Änderungsverlauf von Visual C++ von 2003 bis 2015](porting/visual-cpp-change-history-2003-2015.md)  
[Visual C++: Neuerungen von 2003 bis 2015](porting/visual-cpp-what-s-new-2003-through-2015.md)  
[Blog des Visual C++-Teams](https://blogs.msdn.microsoft.com/vcblog/)  
