---
title: Interior_ptr (C + c++ / CLI) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- stdcli::language::interior_ptr
- interior_ptr_cpp
- interior_ptr
dev_langs:
- C++
helpviewer_keywords:
- interior_ptr keyword [C++]
ms.assetid: 25160f74-569e-492d-9e3c-67ece7486baa
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: a83182151ccb85b920a37713b70df53b383b8919
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="interiorptr-ccli"></a>interior_ptr (C++/CLI)
Ein *innerer Zeiger* deklariert einen Zeiger auf in einen Verweistyp handelt, aber nicht auf das Objekt selbst. Ein innerer Zeiger kann auf eine Verweis-Handle, der Werttyp, der mittels Boxing gepackter Typhandle, Member eines verwalteten Typs oder auf ein Element eines verwalteten Arrays zeigen.  
  
## <a name="all-runtimes"></a>Alle Laufzeiten  
 (Es gibt keine Hinweise für diese Sprachfunktion, die für alle Laufzeiten gültig sind.)  
  
## <a name="windows-runtime"></a>Windows-Runtime  
 (Es gibt keine Hinweise für diese Sprachfunktion, die nur für Windows-Runtime gelten.)  
  
### <a name="requirements"></a>Anforderungen  
 Compileroption: **/ZW**  
  
## <a name="common-language-runtime"></a>Common Language Runtime  
 Die folgende Syntax veranschaulicht, eines inneren Zeigers.  
  
### <a name="syntax"></a>Syntax  
  
```cpp  
cli::interior_ptr<cv_qualifier type> var = &initializer;  
```  
  
### <a name="parameters"></a>Parameter  
 *cv_qualifier*  
 **const** oder `volatile` Qualifizierer.  
  
 *Typ*  
 Der Typ des *Initialisierer*.  
  
 *var*  
 Der Name des der `interior_ptr` Variable.  
  
 *initializer*  
 Ein Element ein Verweistyp, ein Element ein verwaltetes Array oder ein anderes Objekt, das einen systemeigenen Zeiger zugewiesen werden können.  
  
### <a name="remarks"></a>Hinweise  
 Ein systemeigenen Zeiger kann sich nicht um ein Element als seine Änderungen am Speicherort auf dem verwalteten Heap nachzuverfolgen, die durch den Garbage Collector Verschieben von Instanzen eines Objekts führt. Damit für einen Zeiger auf das ordnungsgemäß auf die Instanz verweisen, muss die Common Language Runtime zum Aktualisieren des Zeigers auf das Objekt neu positioniert.  
  
 Ein `interior_ptr` eine Obermenge der Funktionen der systemeigenen Zeiger darstellt.  Aus diesem Grund kann Elemente, die einen systemeigenen Zeiger zugewiesen werden kann auch zum zugewiesen ein `interior_ptr`.  Ein innerer Zeiger ist zulässig, um den gleichen Satz von Vorgängen wie systemeigene Zeiger, einschließlich Vergleich und Zeigerarithmetik auszuführen.  
  
 Ein innerer Zeiger kann nur auf dem Stapel deklariert werden.  Ein innerer Zeiger kann nicht als Member einer Klasse deklariert werden.  
  
 Da innere Zeigern nur auf dem Stapel vorhanden sind, ergibt die Übernahme der Adresse eines inneren Zeigers einen nicht verwalteten Zeiger.  
  
 `interior_ptr` verfügt über eine implizite Konvertierung in `bool`, die für die Verwendung in bedingten Anweisungen ermöglicht.  
  
 Informationen, wie einen inneren Zeiger deklariert, die in ein Objekt verweist, die auf dem Heap der Garbage Collection verschoben werden kann, finden Sie unter [Pin_ptr](../windows/pin-ptr-cpp-cli.md).  
  
 `interior_ptr` befindet sich im cli-Namespace.  Finden Sie unter [Plattform, Default- und Cli-Namespaces](../windows/platform-default-and-cli-namespaces-cpp-component-extensions.md) für Weitere Informationen.  
  
 Weitere Informationen zu inneren Zeigern finden Sie unter  
  
-   [Vorgehensweise: Deklarieren und Verwenden von inneren Zeigern und verwalteten Arrays (C++/CLI)](../windows/how-to-declare-and-use-interior-pointers-and-managed-arrays-cpp-cli.md)  
  
-   [Vorgehensweise: Deklarieren von Werttypen mit dem interior_ptr-Schlüsselwort (C++/CLI)](../windows/how-to-declare-value-types-with-the-interior-ptr-keyword-cpp-cli.md)  
  
-   [Vorgehensweise: Überladen von Funktionen mit inneren und nativen Zeigern (C++/CLI)](../windows/how-to-overload-functions-with-interior-pointers-and-native-pointers-cpp-cli.md)  
  
-   [Vorgehensweise: Deklarieren von inneren Zeigern mit dem const-Schlüsselwort (C++/CLI)](../windows/how-to-declare-interior-pointers-with-the-const-keyword-cpp-cli.md)  
  
### <a name="requirements"></a>Anforderungen  
 Compileroption: **/clr**  
  
### <a name="examples"></a>Beispiele  
 **Beispiel**  
  
 Das folgende Beispiel zeigt, wie deklarieren und Verwenden eines inneren Zeigers in einen Referenztyp darstellt.  
  
```cpp  
// interior_ptr.cpp  
// compile with: /clr  
using namespace System;  
  
ref class MyClass {  
public:  
   int data;  
};  
  
int main() {  
   MyClass ^ h_MyClass = gcnew MyClass;  
   h_MyClass->data = 1;  
   Console::WriteLine(h_MyClass->data);  
  
   interior_ptr<int> p = &(h_MyClass->data);  
   *p = 2;  
   Console::WriteLine(h_MyClass->data);  
  
   // alternatively  
   interior_ptr<MyClass ^> p2 = &h_MyClass;  
   (*p2)->data = 3;  
   Console::WriteLine((*p2)->data);  
}  
```  
  
 **Ausgabe**  
  
```Output  
1  
2  
3  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Komponentenerweiterungen für Laufzeitplattformen](../windows/component-extensions-for-runtime-platforms.md)