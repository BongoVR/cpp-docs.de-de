---
title: '&lt;filesystem&gt;-Operatoren | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- FILESYSTEM/std::experimental::filesystem::operator==
- FILESYSTEM/std::experimental::filesystem::operator!=
- FILESYSTEM/std::experimental::filesystem::operator<
- FILESYSTEM/std::experimental::filesystem::operator<=
- FILESYSTEM/std::experimental::filesystem::operator>
- FILESYSTEM/std::experimental::filesystem::operator>=
- FILESYSTEM/std::experimental::filesystem::operator/
- FILESYSTEM/std::experimental::filesystem::operator<<
- FILESYSTEM/std::experimental::filesystem::operator>>
dev_langs:
- C++
ms.assetid: 102c4833-aa3b-41a8-8998-f5003c546bfd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 546e601afeb05e0347dba8bf792611f20068c69b
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="ltfilesystemgt-operators"></a>&lt;filesystem&gt;-Operatoren

Die Operatoren führen einen lexikalischen Vergleich von zwei Pfaden als Zeichenfolgen aus. Verwenden Sie die **equivalent** -Funktion, um zu bestimmen, ob zwei Pfade (beispielsweise ein relativer Pfad und ein absoluter Pfad) auf dieselbe Datei oder dasselbe Verzeichnis auf dem Datenträger verweisen.

Weitere Informationen finden Sie unter [Dateisystemnavigation](../standard-library/file-system-navigation.md).

## <a name="operator"></a>operator==

```cpp
bool operator==(const path& left, const path& right) noexcept;
```

Die Funktion gibt „left.native() == right.native()“ zurück.

## <a name="operator"></a>Operator!=

```cpp
bool operator!=(const path& left, const path& right) noexcept;
```

Die Funktion gibt „!(left == right)“ zurück.

## <a name="operator"></a>Operator <

```cpp
bool operator<(const path& left, const path& right) noexcept;
```

Die Funktion gibt „left.native() < right.native()“ zurück.

## <a name="operator"></a>Operator <=

```cpp
bool operator<=(const path& left, const path& right) noexcept;
```

Die Funktion gibt „!(right \< left)“ zurück.

## <a name="operator"></a>Operator >

```cpp
bool operator>(const path& left, const path& right) noexcept;
```

Die Funktion gibt „right \< left“ zurück.

## <a name="operator"></a>Operator >=

```cpp
bool operator>=(const path& left, const path& right) noexcept;
```

Die Funktion gibt „!(left < right)“ zurück.

## <a name="operator"></a>operator/

```cpp
path operator/(const path& left, const path& right);
```

Die Funktion führt Folgendes aus:

```cpp
basic_string<Elem, Traits> str;
path ans = left;
return (ans /= right);
```

## <a name="operator"></a>Operator <<

```cpp
template <class Elem, class Traits>
basic_ostream<Elem, Traits>& operator<<(basic_ostream<Elem, Traits>& os, const path& pval);
```

Die Funktion gibt „os << pval.string\<Elem, Traits>()“ zurück.

## <a name="operator"></a>Operator >>

```cpp
template <class Elem, class Traits>
basic_istream<Elem, Traits>& operator<<(basic_istream<Elem, Traits>& is, const path& pval);
```

Die Funktion führt Folgendes aus:

```cpp
basic_string<Elem, Traits> str;
is>> str;
pval = str;
return (is);
```

## <a name="see-also"></a>Siehe auch

[Path-Klasse (C++-Standardbibliothek)](../standard-library/path-class.md)<br/>
[Dateisystemnavigation (C++)](../standard-library/file-system-navigation.md)<br/>
[\<filesystem>](../standard-library/filesystem.md)<br/>
