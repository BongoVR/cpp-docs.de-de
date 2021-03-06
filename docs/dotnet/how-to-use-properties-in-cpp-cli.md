---
title: 'Vorgehensweise: Verwenden von Eigenschaften in c++ / CLI | Microsoft Docs'
ms.custom: ''
ms.date: 07/21/2017
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- simple properties
- properties [C++], simple
ms.assetid: f5d82547-e214-4f05-9e1b-ddb6d0dc5e4c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 4873b7d37ef55c050ef074323c4644e4277f593d
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-use-properties-in-ccli"></a>Gewusst wie: Verwenden von Eigenschaften in C++/CLI
Dieser Artikel zeigt, wie Eigenschaften in C + c++ / CLI.  
  
## <a name="basic-properties"></a>Basiseigenschaften  
 Für grundlegende Eigenschaften – diejenigen, die lediglich zuweisen und Abrufen ein privaten Datenmember – müssen Sie nicht explizit definieren Get und Accessorfunktionen festgelegt werden, da der Compiler automatisch stellt, sobald nur der Datentyp der Eigenschaft zugewiesen. Dieser Code veranschaulicht eine einfache Eigenschaft:  
  
```cpp  
// SimpleProperties.cpp  
// compile with: /clr  
using namespace System;  
  
ref class C {  
public:  
   property int Size;  
};  
  
int main() {  
   C^ c = gcnew C;  
   c->Size = 111;  
   Console::WriteLine("c->Size = {0}", c->Size);  
}  
```  
  
```Output  
c->Size = 111  
```  
  
## <a name="static-properties"></a>Statische Eigenschaften  
 Dieses Codebeispiel zeigt, wie deklariert und verwendet eine statische Eigenschaft.  Eine statische Eigenschaft kann nur statische Member der Klasse zugreifen.  
  
```cpp  
// mcppv2_property_3.cpp  
// compile with: /clr  
using namespace System;  
  
ref class StaticProperties {  
   static int MyInt;  
   static int MyInt2;  
  
public:  
   static property int Static_Data_Member_Property;  
  
   static property int Static_Block_Property {  
      int get() {  
         return MyInt;  
      }  
  
      void set(int value) {  
         MyInt = value;  
      }        
   }  
};  
  
int main() {  
   StaticProperties::Static_Data_Member_Property = 96;  
   Console::WriteLine(StaticProperties::Static_Data_Member_Property);  
  
   StaticProperties::Static_Block_Property = 47;  
   Console::WriteLine(StaticProperties::Static_Block_Property);  
}  
```  
  
```Output  
96  
47  
```  
  
## <a name="indexed-properties"></a>Indizierte Eigenschaften  
 Eine indizierte Eigenschaft macht in der Regel eine Datenstruktur, die mithilfe einen Indexoperator zugegriffen wird.  
  
 Bei Verwendung eine indizierte Standardeigenschaft, können Sie die Datenstruktur zugreifen, nur durch einen Verweis auf den Klassennamen, aber wenn Sie eine benutzerdefinierte indizierte Eigenschaft verwenden, müssen Sie zum Angeben des Namens der Eigenschaft auf die Datenstruktur zuzugreifen.  
  
 Weitere Informationen dazu, wie nach einen Indexer zu nutzen, die in c# geschrieben ist, finden Sie unter [wie: Verwenden eines C#-Indexers (C + c++ / CLI)](../dotnet/how-to-consume-a-csharp-indexer-cpp-cli.md).  
  
 Dieses Codebeispiel zeigt, wie Standard- und benutzerdefinierten indizierte Eigenschaften verwenden:  
  
```cpp  
// mcppv2_property_2.cpp  
// compile with: /clr  
using namespace System;  
public ref class C {  
   array<int>^ MyArr;  
  
public:  
   C() {  
      MyArr = gcnew array<int>(5);  
   }  
  
   // default indexer  
   property int default[int] {  
      int get(int index) {  
         return MyArr[index];  
      }  
      void set(int index, int value) {  
         MyArr[index] = value;  
      }  
   }  
  
   // user-defined indexer  
   property int indexer1[int] {  
      int get(int index) {  
         return MyArr[index];  
      }  
      void set(int index, int value) {  
         MyArr[index] = value;  
      }  
   }  
};  
  
int main() {  
   C ^ MyC = gcnew C();  
  
   // use the default indexer  
   Console::Write("[ ");  
   for (int i = 0 ; i < 5 ; i++) {  
      MyC[i] = i;  
      Console::Write("{0} ", MyC[i]);  
   }  
  
   Console::WriteLine("]");  
  
   // use the user-defined indexer  
   Console::Write("[ ");  
   for (int i = 0 ; i < 5 ; i++) {  
      MyC->indexer1[i] = i * 2;  
      Console::Write("{0} ", MyC->indexer1[i]);  
   }  
  
   Console::WriteLine("]");  
}  
```  
  
```Output  
[ 0 1 2 3 4 ]  
[ 0 2 4 6 8 ]  
```  
  
 Im folgenden Beispiel wird gezeigt, wie mithilfe der Standardindexer Aufrufen der `this` Zeiger.  
  
```cpp  
// call_default_indexer_through_this_pointer.cpp  
// compile with: /clr /c  
value class Position {  
public:  
   Position(int x, int y) : position(gcnew array<int, 2>(100, 100)) {  
      this->default[x, y] = 1;  
   }  
  
   property int default[int, int] {  
      int get(int x, int y) {  
         return position[x, y];  
      }  
  
      void set(int x, int y, int value) {}  
   }  
  
private:  
   array<int, 2> ^ position;  
};  
```  
  
 Dieses Beispiel zeigt, wie <xref:System.Reflection.DefaultMemberAttribute> der Standardindexer angeben:  
  
```cpp  
// specify_default_indexer.cpp  
// compile with: /LD /clr  
using namespace System;  
[Reflection::DefaultMember("XXX")]  
public ref struct Squares {  
   property Double XXX[Double] {  
      Double get(Double data) {  
         return data*data;  
      }  
   }  
};  
```  
  
 Im nächste Beispiel nutzt die Metadaten, die im vorherigen Beispiel erstellt wird.  
  
```cpp  
// consume_default_indexer.cpp  
// compile with: /clr  
#using "specify_default_indexer.dll"  
int main() {  
   Squares ^ square = gcnew Squares();  
   System::Console::WriteLine("{0}", square[3]);  
}  
```  
  
```Output  
9  
```  
  
## <a name="virtual-properties"></a>Virtuelle Eigenschaften  
 Dieses Codebeispiel zeigt, wie zu deklarieren und Verwenden virtueller Eigenschaften:  
  
```cpp  
// mcppv2_property_4.cpp  
// compile with: /clr  
using namespace System;  
interface struct IEFace {  
public:  
   property int VirtualProperty1;  
   property int VirtualProperty2 {  
      int get();  
      void set(int i);  
   }  
};  
  
// implement virtual events  
ref class PropImpl : public IEFace {  
   int MyInt;  
public:  
   virtual property int VirtualProperty1;  
  
   virtual property int VirtualProperty2 {  
      int get() {  
         return MyInt;  
      }  
      void set(int i) {  
         MyInt = i;  
      }  
   }  
};  
  
int main() {  
   PropImpl ^ MyPI = gcnew PropImpl();  
   MyPI->VirtualProperty1 = 93;  
   Console::WriteLine(MyPI->VirtualProperty1);  
  
   MyPI->VirtualProperty2 = 43;  
   Console::WriteLine(MyPI->VirtualProperty2);  
}  
```  
  
```Output  
93  
43  
```  
  
## <a name="abstract-and-sealed-properties"></a>Abstrakte und versiegelte-Eigenschaften  
 Obwohl die [abstrakte](../windows/abstract-cpp-component-extensions.md) und [versiegelten](../windows/sealed-cpp-component-extensions.md) Schlüsselwörter werden als gültig in der ECMA C# + angegeben c++ / CLI-Spezifikation für den Visual C++-Compiler kann nicht angegeben werden sie für einfache Eigenschaften noch in der Eigenschaft die Deklaration einer nicht triviale Eigenschaft.  
  
 Um eine versiegelte oder abstrakte Eigenschaft deklarieren, müssen Sie eine nicht triviale Eigenschaft definieren und geben Sie dann die `abstract` oder `sealed` Schlüsselwort für die Get- und set Accessorfunktionen.  
  
```cpp  
// properties_abstract_sealed.cpp  
// compile with: /clr  
ref struct A {  
protected:  
   int m_i;  
  
public:  
   A() { m_i = 87; }  
  
   // define abstract property  
   property int Prop_1 {  
      virtual int get() abstract;  
      virtual void set(int i) abstract;  
   }  
};  
  
ref struct B : A {  
private:  
   int m_i;  
  
public:  
   B() { m_i = 86; }  
  
   // implement abstract property  
   property int Prop_1 {  
      virtual int get() override { return m_i; }  
      virtual void set(int i) override { m_i = i; }  
   }  
};  
  
ref struct C {  
private:  
   int m_i;  
  
public:  
   C() { m_i = 87; }  
  
   // define sealed property  
   property int Prop_2 {  
      virtual int get() sealed { return m_i; }  
      virtual void set(int i) sealed { m_i = i; };  
   }  
};  
  
int main() {  
   B b1;  
   // call implementation of abstract property  
   System::Console::WriteLine(b1.Prop_1);  
  
   C c1;  
   // call sealed property  
   System::Console::WriteLine(c1.Prop_2);  
}  
```  
  
```Output  
86  
87  
```  
  
## <a name="multidimensional-properties"></a>Mehrdimensionale Eigenschaften  
 Mehrdimensionale Eigenschaften können Sie die Methoden des Eigenschaftenaccessors definieren, die eine nicht standardmäßige Anzahl von Parametern.  
  
```cpp  
// mcppv2_property_5.cpp  
// compile with: /clr  
ref class X {  
   double d;  
public:  
   X() : d(0) {}  
   property double MultiDimProp[int, int, int] {  
      double get(int, int, int) {  
         return d;  
      }  
      void set(int i, int j, int k, double l) {  
         // do something with those ints  
         d = l;  
      }  
   }  
  
   property double MultiDimProp2[int] {  
      double get(int) {  
         return d;  
      }  
      void set(int i, double l) {  
         // do something with those ints  
         d = l;  
      }  
   }  
  
};  
  
int main() {  
   X ^ MyX = gcnew X();  
   MyX->MultiDimProp[0,0,0] = 1.1;  
   System::Console::WriteLine(MyX->MultiDimProp[0, 0, 0]);  
}  
```  
  
```Output  
1.1  
```  
  
## <a name="overloading-property-accessors"></a>Überladen von eigenschaftenzugriffsmethoden  
 Im folgende Beispiel wird gezeigt, wie indizierte Eigenschaften überladen werden.  
  
```cpp  
// mcppv2_property_6.cpp  
// compile with: /clr  
ref class X {  
   double d;  
public:  
   X() : d(0.0) {}  
   property double MyProp[int] {  
      double get(int i) {  
         return d;  
      }  
  
      double get(System::String ^ i) {  
         return 2*d;  
      }  
  
      void set(int i, double l) {  
         d = i * l;  
      }  
   }   // end MyProp definition  
};  
  
int main() {  
   X ^ MyX = gcnew X();  
   MyX->MyProp[2] = 1.7;  
   System::Console::WriteLine(MyX->MyProp[1]);  
   System::Console::WriteLine(MyX->MyProp["test"]);  
}  
```  
  
```Output  
3.4  
6.8  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Eigenschaft](../windows/property-cpp-component-extensions.md)