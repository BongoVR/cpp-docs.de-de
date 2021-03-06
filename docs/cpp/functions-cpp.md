---
title: Funktionen (C++) | Microsoft Docs
ms.custom: ''
ms.date: 01/25/2018
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- defaults, arguments
- function definitions
- function definitions, about function definitions
- default arguments
- declarators, functions
ms.assetid: 33ba01d5-75b5-48d2-8eab-5483ac7d2274
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 720147992540b53c51e731db361cd9946a7a5313
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="functions-c"></a>Funktionen (C++)

Eine Funktion ist ein Codeblock, der einige Vorgänge ausführt. Eine Funktion kann optional Eingabeparameter definieren, die Aufrufern ermöglichen, Argumente in die Funktion weiterzugeben. Eine Funktion kann einen Wert optional als Ausgabe zurückgeben. Funktionen sind für das Kapseln allgemeiner Vorgänge in einem einzelnen wiederverwendbaren Block nützlich, und zwar ideal unter Verwendung eines Namens, der deutlich das beschreibt, was die Funktion vornimmt. Die folgende Funktion akzeptiert zwei Ganzzahlen von einem Aufrufer und gibt deren Summe zurück; `a` und `b` sind *Parameter* des Typs **Int**.

```cpp
int sum(int a, int b)
{
    return a + b;
}
```

Die Funktion aufgerufen werden kann, oder *aufgerufen*, von einer beliebigen Anzahl von Stellen in der Anwendung. Die Werte, die an die Funktion übergeben werden, sind die *Argumente*, deren Typen mit den Parametertypen in der Funktionsdefinition kompatibel sein müssen.

```cpp
int main()
{
    int i = sum(10, 32);
    int j = sum(i, 66);
    cout << "The value of j is" << j << endl; // 108
}
```

Es gibt keine praktische Begrenzung für die Funktionslänge, jedoch angemessene Entwurfsziele für Funktionen, die eine einzelne klar definierte Aufgabe ausführen. Komplexe Algorithmen sollten möglichst in leicht verständliche einfachere Funktionen aufgeschlüsselt werden.

Im Klassenbereich definierte Funktionen werden als Memberfunktionen bezeichnet. In C++ kann eine Funktion im Gegensatz zu anderen Sprachen auch im Namespacebereich (einschließlich des impliziten globalen Namespace) definiert werden. Solche Funktionen heißen *freien Funktionen* oder *nicht-Memberfunktionen*; sie werden umfassend in der Standardbibliothek verwendet.

Funktionen werden möglicherweise *überladen*, was bedeutet, dass unterschiedliche Versionen einer Funktion kann den gleichen Namen freigeben, wenn sich die Anzahl und/oder den Typ des formalen Parameter unterscheidet. Weitere Informationen finden Sie unter [Funktionsüberladung](../cpp/function-overloading.md).

## <a name="parts-of-a-function-declaration"></a>Bestandteile einer Funktionsdeklaration

Eine minimale Funktion *Deklaration* besteht aus den Rückgabetyp, den Funktionsnamen und die Parameterliste (die leer sein kann) sowie optionalen Schlüsselwörtern, die dem Compiler zusätzliche Anweisungen bereitstellen. Im folgende Beispiel wird die Deklaration einer Funktion:

```cpp
int sum(int a, int b);
```

Eine Funktionsdefinition besteht aus einer Deklaration plus dem *Text*, dem wird der gesamte Code zwischen den geschweiften Klammern:

```cpp
int sum(int a, int b)
{
    return a + b;
}
```

Eine Funktionsdeklaration, auf die ein Semikolon folgt, wird möglicherweise an mehreren Stellen in einem Programm angezeigt. Sie muss vor dem Aufrufen dieser Funktion in jeder Übersetzungseinheit angezeigt werden. Die Funktionsdefinition darf gemäß der Regel mit einer Definition (One Definition Rule, ODR) nur einmal im Programm angezeigt werden.

Die erforderlichen Bestandteile einer Funktionsdeklaration lauten:

1. Der Rückgabetyp, der den Typ des Werts, die die Funktion zurückgibt angibt, oder **"void"** , wenn kein Wert zurückgegeben wird. In C ++ 11 **Auto** ist ein gültiger Rückgabetyp, die den Compiler anweist, den Typ aus der rückgabeanweisung abgeleitet werden. In C++14 ist „decltype(auto)“ ebenfalls zulässig. Weitere Informationen finden Sie unten unter „Typableitung in Rückgabetypen“.

1. Der Funktionsname, der mit einem Buchstaben oder Unterstrich beginnen muss, darf keine Leerzeichen enthalten. Im Allgemeinen weisen führende Unterstriche in Standardbibliothek-Funktionsnamen auf private Memberfunktionen oder Nicht-Memberfunktionen, die nicht für die Verwendung durch Ihren Code vorgesehen sind, hin.

1. Die Parameterliste, ein durch geschweifte Klammern getrennter, kommagetrennter Satz von mindestens null Parametern, die den Typ und optional einen lokalen Namen angeben, anhand dessen die Werte im Funktionsrumpf möglicherweise aufgerufen werden.

Optionale Bestandteile einer Funktionsdeklaration sind:

1. **Constexpr**, was bedeutet, dass der Rückgabewert der Funktion einen konstanten Wert wird zur Kompilierzeit berechnet werden kann.

    ```cpp
    constexpr float exp(float x, int n)
    {
        return n == 0 ? 1 :
            n % 2 == 0 ? exp(x * x, n / 2) :
            exp(x * x, (n - 1) / 2) * x;
    };
    ```

1. Der Verknüpfungsspezifikation **"extern"** oder **statische**.

    ```cpp
    //Declare printf with C linkage.
    extern "C" int printf( const char *fmt, ... );

    ```

     Weitere Informationen finden Sie unter [Programm und Verknüpfung](../cpp/program-and-linkage-cpp.md).

1. **Inline**, weist den Compiler an, ersetzen Sie jeden Aufruf an die Funktion mit des Funktionscodes. Durch den Inlinevorgang kann die Leistung in Szenarien verbessert werden, in denen eine Funktion schnell ausgeführt und wiederholt in einem leistungskritischen Codeabschnitt aufgerufen wird.

    ```cpp
    inline double Account::GetBalance()
    {
        return balance;
    }
    ```

     Weitere Informationen finden Sie unter [Inlinefunktionen](../cpp/inline-functions-cpp.md).

1. Ein **Noexcept** Ausdruck, der angibt, und zwar unabhängig davon, ob die Funktion eine Ausnahme auslösen kann. Im folgenden Beispiel die Funktion löst keine Ausnahme ab, wenn die `is_pod` Ausdruck wird zu **"true"**.

    ```cpp
    #include <type_traits>

    template <typename T>
    T copy_object(T& obj) noexcept(std::is_pod<T>) {...}
    ```

     Weitere Informationen finden Sie unter [Noexcept](../cpp/noexcept-cpp.md).

1. (Nur Memberfunktionen) Cv-Qualifizierer, die angeben, ob die Funktion **const** oder **volatile**.

1. (Nur Memberfunktionen) **virtuellen**, **überschreiben**, oder **endgültigen**. **virtuelle** gibt an, dass eine Funktion in einer abgeleiteten Klasse überschrieben werden kann. **Überschreiben Sie** bedeutet, dass eine Funktion in einer abgeleiteten Klasse eine virtuelle Funktion außer Kraft gesetzt wird. **endgültige** bedeutet, dass eine Funktion kann nicht in einem weiteren überschrieben werden abgeleitete Klasse. Weitere Informationen finden Sie unter [virtuelle Funktionen](../cpp/virtual-functions.md).

1. (nur Memberfunktionen) **statische** angewendet auf einen Member Funktion bedeutet, dass die Funktion nicht mit Objektinstanzen der Klasse verknüpft ist.

1. (Gilt nur für nicht statische Memberfunktionen) Ref-Qualifizierer, der für den Compiler, welche Überladung einer Funktion angibt, um auszuwählen, wann der implizite Objektparameter (\*dies) ein Rvalue-Verweis oder ein Lvalue-Verweis ist. Weitere Informationen finden Sie unter [Funktionsüberladung](function-overloading.md#ref-qualifiers).

Die folgende Abbildung zeigt die Teile einer Funktionsdefinition. Der schattierte Bereich ist der Funktionsrumpf.

 ![Teile einer Funktionsdefinition](../cpp/media/vc38ru1.gif "vc38RU1") Teile einer Funktionsdefinition

## <a name="function-definitions"></a>Funktionsdefinitionen

Ein *Funktion Definition* besteht aus der Deklaration und der Hauptteil der Funktion in der geschweiften Klammern eingeschlossen die Variablendeklarationen, Anweisungen und Ausdrücke enthält. Das folgende Beispiel zeigt eine vollständige Funktionsdefinition:

```cpp
    int foo(int i, std::string s)
    {
       int value {i};
       MyClass mc;
       if(strcmp(s, "default") != 0)
       {
            value = mc.do_something(i);
       }
       return value;
    }
```

Im Textteil deklarierte Variablen werden als lokale Variablen bezeichnet. Sie verlassen den Gültigkeitsbereich, wenn die Funktion beendet wird. Daher sollte eine Funktion niemals einen Verweis zu einer lokalen Variable zurückgeben!

```cpp
    MyClass& boom(int i, std::string s)
    {
       int value {i};
       MyClass mc;
       mc.Initialize(i,s);
       return mc;
    }
```

## <a name="const-and-constexpr-functions"></a>const- und Constexpr-Funktionen

Sie können deklarieren eine Memberfunktion als **const** um anzugeben, dass die Funktion nicht zulässig ist, um die Werte von Datenmembern in der Klasse ändern. Durch die Deklaration einer Memberfunktion als **const**, lassen sich den Compiler erzwingen *Const-Richtigkeit*. Wenn jemand versehentlich versucht, so ändern Sie das Objekt mithilfe einer Funktion deklariert als **const**, wird ein Compilerfehler ausgelöst. Weitere Informationen finden Sie unter [const](const-cpp.md).

Deklarieren Sie eine Funktion als **Constexpr** Wenn der Wert, der es erzeugt möglicherweise kann zur Kompilierzeit bestimmt werden. Eine Constexpr-Funktion führt im Allgemeinen schneller als eine reguläre Funktion. Weitere Informationen finden Sie unter [Constexpr](constexpr-cpp.md).

## <a name="function-templates"></a>Funktionsvorlagen

Eine Funktionsvorlage ähnelt einer Klassenvorlage. Sie generiert auf Grundlage der Vorlagenargumente konkrete Funktionen. In vielen Fällen kann die Vorlage die Typargumente ableiten. Daher ist es nicht erforderlich, sie explizit anzugeben.

```cpp
template<typename Lhs, typename Rhs>
auto Add2(const Lhs& lhs, const Rhs& rhs)
{
    return lhs + rhs;
}

auto a = Add2(3.13, 2.895); // a is a double
auto b = Add2(string{ "Hello" }, string{ " World" }); // b is a std::string
```

Weitere Informationen finden Sie unter [Funktionsvorlagen](../cpp/function-templates.md)

## <a name="function-parameters-and-arguments"></a>Funktionsparameter und Argumente

Eine Funktion weist eine durch Kommas getrennte Liste von mindestens null Typen auf. Jede davon verfügt über einen Namen, unter dem es im Funktionsrumpf aufgerufen werden kann. Eine Funktionsvorlage kann den zusätzliche Typ- oder Wertparameter angeben. Der Aufrufer gibt Argumente weiter, bei denen es sich um konkrete Werte handelt, deren Typen mit der Parameterliste kompatibel sind.

Argumente werden standardmäßig zur Funktion nach Wert weitergegeben. Die Funktion empfängt demnach eine Kopie des weiterzugebenden Objekts. Für große Objekte kann das Erstellen einer Kopie aufwändig und nicht immer erforderlich sein. Damit Argumente nach Verweis (insbesondere Lvalue-Verweis) weitergegeben werden, fügen Sie einen Verweis Quantifizierer an den Parameter aus:

```cpp
void DoSomething(std::string& input){...}
```

Wenn eine Funktion ein Argument ändert, das nach Verweis weitergegeben wird, ändert sie das ursprüngliche Objekt und nicht eine lokale Kopie. Qualifizieren Sie den Parameter als „const&“, um zu verhindern, dass eine Funktion ein derartiges Argument ändert:

```cpp
void DoSomething(const std::string& input){...}
```

 **C++ 11:** verwenden Sie zum expliziten Verarbeiten von Argumenten, die nach Rvalue-Verweis oder Lvalue-Verweis übergeben werden, ein doppeltes kaufmännisches und-Zeichen im Parameter um einen universellen Verweis anzugeben:

```cpp
void DoSomething(const std::string&& input){...}
```

Eine Funktion deklariert, mit dem einzelnen Schlüsselwort **"void"** in der Parameterdeklaration Liste akzeptiert keine Argumente, solange das Schlüsselwort **"void"** das erste und einzige Member der argumentdeklarationsliste ist. Argumente des Typs **"void"** an anderer Stelle in der Liste erzeugen Fehler. Zum Beispiel:

```cpp

// OK same as GetTickCount()
long GetTickCount( void );
```

Beachten Sie, dass es ist zwar nicht zulässig, geben Sie einen **"void"** Argument außer wie grundsätzliche hier abgeleitete Typen vom Typ **"void"** (z. B. Zeiger auf **"void"** und Arrays von **"void"**) können an beliebiger Stelle der argumentdeklarationsliste vorkommen.

### <a name="default-arguments"></a>Standardargumente

Der oder die letzten Parameter in einer Funktionssignatur werden möglicherweise einem Standardargument zugewiesen. Der Aufrufer kann demnach das Argument auslassen, wenn die Funktion aufgerufen wird, es sei denn, es soll ein anderer Wert angegeben werden.

```cpp
int DoSomething(int num,
    string str,
    Allocator& alloc = defaultAllocator)
{ ... }

// OK both parameters are at end
int DoSomethingElse(int num,
    string str = string{ "Working" },
    Allocator& alloc = defaultAllocator)
{ ... }

// C2548: 'DoMore': missing default parameter for parameter 2
int DoMore(int num = 5, // Not a trailing parameter!
    string str,
    Allocator& = defaultAllocator)
{...}
```

Weitere Informationen finden Sie unter [Standardargumente](../cpp/default-arguments.md).

## <a name="function-return-types"></a>Funktionsrückgabetypen

Eine Funktion kann nicht einer anderen Funktion oder ein integriertes Array zurückgeben; jedoch Zeiger auf diese Typen zurückgegeben werden kann oder ein *Lambda*, der ein Funktionsobjekt generiert. Außer in diesen Fällen kann eine Funktion zurückgeben, einen Wert eines beliebigen Typs, die im Gültigkeitsbereich befindet oder sie gibt keinen Wert zurück, in diesem Fall der Rückgabetyp ist **"void"**.

### <a name="trailing-return-types"></a>Nachstehende Rückgabetypen

Ein „gewöhnlicher“ Rückgabetyp befindet sich auf der linken Seite der Funktionssignatur. Ein *nachstehendem Rückgabetyp* befindet sich rechts von der Signatur und vorangestellt ist der Operator ->. Nachstehende Rückgabetypen sind insbesondere in Funktionsvorlagen nützlich, wenn der Typ des Rückgabewerts auf Vorlagenparametern beruht.

```cpp
template<typename Lhs, typename Rhs>
auto Add(const Lhs& lhs, const Rhs& rhs) -> decltype(lhs + rhs)
{
    return lhs + rhs;
}
```

Wenn **Auto** dient in Verbindung mit einem nachstehenden Rückgabetyp, fungiert es als Platzhalter für das, was der Decltype-Ausdruck generiert, und führt keine eigene typableitung aus.


## <a name="function-local-variables"></a>Lokale Funktionsvariablen

Eine in einem Funktionsrumpf deklarierte Variable wird aufgerufen, eine *lokale Variable* oder einfach als *lokale*. Nicht statische lokale Variablen sind nur innerhalb des Funktionsrumpfs sichtbar, wenn sie auf dem Stapel deklariert werden, wenn den Bereich verlässt, wenn die Funktion vorhanden ist. Wenn Sie eine lokale Variable erstellen und nach Wert zurückgeben, kann der Compiler für gewöhnlich die Rückgabewertoptimierung vornehmen, um nicht erforderliche Kopiervorgänge zu vermeiden. Wenn Sie eine lokale Variable nach Verweis zurückgeben, stellt eine Compiler eine Warnung aus, da jeder Versuch durch den Aufrufer, diesen Verweis zu verwenden, erst nach der Zerstörung der lokalen Variablen auftritt.

In C++ kann eine lokale Variable als statisch deklariert werden. Die Variable ist nur innerhalb des Funktionsrumpfs sichtbar. Es ist jedoch eine einzelne Kopie der Variable für alle Instanzen der Funktion vorhanden. Lokale statische Objekte werden während der Beendigung von angegebenen zerstört **Atexit**. Wenn kein statisches Objekt erstellt wurde, da die Ablaufsteuerung des Programms seine Deklaration umgangen ist, wird nicht versucht, das Objekt zu zerstören.

##  <a name="type_deduction"></a> Typableitung in Rückgabetypen (C ++ 14)

In C ++ 14 können Sie **Auto** an den Compiler anzuweisen, den Rückgabetyp aus dem Funktionsrumpf abzuleiten, ohne einen nachstehenden Rückgabetyp anzugeben. Beachten Sie, dass **Auto** immer eine Rückgabe per Wert ableitet. Verwendung **Auto & &** an den Compiler anzuweisen, einen Verweis abzuleiten.

In diesem Beispiel **Auto** wird als eine nicht Konstante wertkopie der Summe von Lhs und Rhs abgeleitet werden.

```cpp
template<typename Lhs, typename Rhs>
auto Add2(const Lhs& lhs, const Rhs& rhs)
{
    return lhs + rhs; //returns a non-const object by value
}
```

Beachten Sie, dass **Auto** nicht die Konstanz der abzuleitenden beibehalten. Bei Weiterleitungsfunktionen, deren Rückgabetyp die Konstanz oder verweisbarkeit der entsprechenden Argumente beibehalten muss, können Sie die **"decltype(Auto)" "** Schlüsselwort, das verwendet die **" decltype "** geben Rückschlussregeln und behält alle Typinformationen. **"decltype(Auto)" "** kann als ein gewöhnlicher Rückgabewert auf der linken Seite oder als ein nachstehender Rückgabewert verwendet werden.

Im folgenden Beispiel wird (basierend auf Code aus [N3493](http://www.open-std.org/JTC1/SC22/WG21/docs/papers/2013/n3493.html)), zeigt **"decltype(Auto)" "** verwendet wird, um die optimale Weiterleitung von Funktionsargumenten in einem Rückgabetyp zu ermöglichen, bis die Vorlage ist instanziiert.

```cpp
template<typename F, typename Tuple = tuple<T...>, int... I>
decltype(auto) apply_(F&& f, Tuple&& args, index_sequence<I...>)
{
    return std::forward<F>(f)(std::get<I>(std::forward<Tuple>(args))...);
}

template<typename F, typename Tuple = tuple<T...>,
    typename Indices = make_index_sequence<tuple_size<Tuple>::value >>
   decltype( auto)
    apply(F&& f, Tuple&& args)
{
    return apply_(std::forward<F>(f), std::forward<Tuple>(args), Indices());
}
}
```

## <a name="returning-multiple-values-from-a-function"></a>Zurückgeben von mehreren Werten aus einer Funktion

Es gibt verschiedene Möglichkeiten, das mehr als einen Wert aus einer Funktion zurückgegeben:

1. Die Werte in ein benanntes Objekt der Klasse oder Struktur gekapselt werden. Erfordert die Definition Klasse oder Struktur an den Aufrufer sichtbar sein sollen:

    ```cpp
    #include <string>
    #include <iostream>
    
    using namespace std;
    
    struct S
    {
        string name;
        int num;
    };
    
    S g()
    {
        string t{ "hello" };
        int u{ 42 };
        return { t, u };
    }
    
    int main()
    {
        S s = g();
        cout << s.name << " " << s.num << endl;
        return 0;
    }
    ```
    
1. Geben Sie ein Std:: Tuple oder Std:: Pair-Objekt zurück:

    ```cpp
    #include <tuple>
    #include <string>
    #include <iostream>
    
    using namespace std;
        
    tuple<int, string, double> f()
    {
        int i{ 108 };
        string s{ "Some text" };
        double d{ .01 };
        return { i,s,d };
    }
    
    int main()
    {
        auto t = f();
        cout << get<0>(t) << " " << get<1>(t) << " " << get<2>(t) << endl;
     
        // --or--
    
        int myval;
        string myname;
        double mydecimal;
        tie(myval, myname, mydecimal) = f();
        cout << myval << " " << myname << " " << mydecimal << endl;
    
        return 0;
    }
    ```

1. **Visual Studio 2017 15,3 und höher** (verfügbar mit [/std:c ++ 17](../build/reference/std-specify-language-standard-version.md)): Verwenden Sie die strukturierte Bindungen. Der Vorteil der strukturierten Bindungen ist, dass die Variablen, die die Rückgabewerte speichern initialisiert werden zur gleichen Zeit, in die sie deklariert werden, die was in einigen Fällen kann deutlich effizienter sein. In dieser Anweisung--`auto[x, y, z] = f();`--die Klammern einführen und initialisieren Sie Namen, die im Bereich für die gesamte Funktionsblock befinden.

    ```cpp
    #include <tuple>
    #include <string>
    #include <iostream>
    
    using namespace std;
    
    tuple<int, string, double> f()
    {
        int i{ 108 };
        string s{ "Some text" };
        double d{ .01 };
        return { i,s,d };
    }
    struct S
    {
        string name;
        int num;
    };
    
    S g()
    {
        string t{ "hello" };
        int u{ 42 };
        return { t, u };
    }
    
    int main()
    {
        auto[x, y, z] = f(); // init from tuple
        cout << x << " " << y << " " << z << endl;
    
        auto[a, b] = g(); // init from POD struct
        cout << a << " " << b << endl;
        return 0;
    }
    ```
    
1. Zusätzlich zur Verwendung des Rückgabewert selbst, können Sie "return" Werte definieren Sie eine beliebige Anzahl von Parametern zum Übergeben als Verweis verwendet werden, damit die Funktion zu ändern, oder initialisieren die Werte der Objekte, die der Aufrufer enthält. Weitere Informationen finden Sie unter [Verweistyp Funktionsargumente](reference-type-function-arguments.md).

## <a name="function-pointers"></a>Funktionszeiger

C++ unterstützt Funktionszeiger auf die gleiche Weise wie die C-Sprache. Eine typsichere Alternative besteht jedoch darin, ein Funktionsobjekt zu verwenden.

Es wird empfohlen, **Typedef** verwendet werden, um einen Alias für den Funktionszeigertyp zu deklarieren, wenn eine Funktion deklariert wird, die einen Funktionszeigertyp zurückgibt.  Beispiel:

```cpp
typedef int (*fp)(int);
fp myFunction(char* s); // function returning function pointer
```

Wenn dies nicht erfolgt, kann die korrekte Syntax für die Funktionsdeklaration aus der Deklaratorsyntax für den Funktionszeiger abgeleitet werden, und zwar wie folgt durch Ersetzen des Bezeichners (`fp` im obigen Beispiel) durch den Namen und die Argumentliste der Funktion:

```cpp
int (*myFunction(char* s))(int);
```

Die vorhergehende Deklaration gleicht der Deklaration oben, die "typedef" verwendet.

## <a name="see-also"></a>Siehe auch

- [Funktionsüberladung](../cpp/function-overloading.md)
- [Funktionen mit Variablenargumentlisten](../cpp/functions-with-variable-argument-lists-cpp.md)
- [Explizit vorgegebene und gelöschte Funktionen](../cpp/explicitly-defaulted-and-deleted-functions.md)
- [Argumentbezogene Namenssuche (Koenig) in Funktionen](../cpp/argument-dependent-name-koenig-lookup-on-functions.md)
- [Standardargumente](../cpp/default-arguments.md)
- [Inlinefunktionen](../cpp/inline-functions-cpp.md)
