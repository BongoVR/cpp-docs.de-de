---
title: Ereignis (Komponentenerweiterungen für C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event
- event_cpp
dev_langs:
- C++
helpviewer_keywords:
- event keyword [C++]
ms.assetid: c4998e42-883c-4419-bbf4-36cdc979dd27
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 7859b8b58bbd8765c38daea46efea5859ba61d67
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="event--c-component-extensions"></a>event (Komponentenerweiterungen für C++)
Die `event` -Schlüsselwort deklariert eine *Ereignis*, d. h. eine Benachrichtigung an die registrierten Abonnenten (*Ereignishandler*), die Aktionen von Interesse ist aufgetreten.  
  
## <a name="all-runtimes"></a>Alle Laufzeiten  
 C + c++ / CX unterstützt das Deklarieren einer *Ereignismember* oder ein *Event-Block*. Ein Ereignismember ist die Kurzschreibweise für das Deklarieren eines Event-Blocks. Standardmäßig deklariert ein Ereignismember die Funktionen `add()`, `remove()` und `raise()`, die explizit in einem Event-Block deklariert werden. Um die Funktionen in einem Ereignismember anzupassen, deklarieren Sie stattdessen einen Event-Block und überschreiben Sie dann die Funktionen, die Sie benötigen.  
  
 **Syntax**  
  
```  
  
// event data member  
modifiereventdelegate^ event_name;     
  
// event block  
modifiereventdelegate^ event_name   
{  
   modifierreturn_valueadd(delegate^ name);  
   modifier void remove(delegate^ name);  
   modifier void raise(parameters);  
}  
```  
  
 **Parameter**  
  
 *Modifizierer*  
 Ein Modifizierer, der entweder für die Ereignisdeklaration oder eine Ereigniszugriffsmethode verwendet werden kann.  Mögliche Werte sind `static` und `virtual`.  
  
 *delegate*  
 Die [Delegieren](../windows/delegate-cpp-component-extensions.md), deren Signatur der Ereignishandler übereinstimmen muss.  
  
 *event_name*  
 Der Name des Ereignisses.  
  
 *Rückgabewert*  
 Der Rückgabewert der Ereigniszugriffsmethode.  Um überprüfbar zu sein, muss der Rückgabetyp `void` sein.  
  
 *Parameter*  
 (optional) Parameter für die `raise` -Methode, die der Signatur des übereinstimmen der *Delegieren* Parameter.  
  
 **Hinweise**  
  
 Ein Ereignis ist eine Zuordnung zwischen einem Delegaten und einer Memberfunktion (Ereignishandler), die auf das Auslösen des Ereignisses reagiert und es Clients beliebiger Klassen ermöglicht, Methoden zu registrieren, die mit der Signatur und dem Rückgabetyp des zugrundeliegenden Delegaten übereinstimmen.  
  
 Es gibt zwei Arten von Ereignisdeklarationen:  
  
 *Ereignis-Datenmember*  
 Der Compiler erstellt automatisch Speicherplatz für das Ereignis in Form eines Members des Delegattyps und erstellt interne Memberfunktionen `add()`, `remove()` und `raise()`. Ein Ereignisdatenmember muss innerhalb einer Klasse deklariert werden. Der Rückgabetyp des Rückgabetyps des Delegaten muss dem Rückgabetyp des Ereignishandlers entsprechen.  
  
 *Event-block*  
 Ein Event-Block ermöglicht es Ihnen, das Verhalten der Methoden `add()`, `remove()` und `raise()` explizit zu deklarieren und anzupassen.  
  
 Sie können mithilfe von `operators+=` und `operator-=` einen Ereignishandler hinzufügen und entfernen oder die Methoden `add()` und `remove()` explizit aufrufen.  
  
 `event` ist ein kontextbezogenes Schlüsselwort. finden Sie unter [Kontextbezogene Schlüsselwörter](../windows/context-sensitive-keywords-cpp-component-extensions.md) für Weitere Informationen.  
  
## <a name="windows-runtime"></a>Windows-Runtime  
  
### <a name="remarks"></a>Hinweise  
 Weitere Informationen finden Sie unter [Ereignisse (C + c++ / CX)](http://msdn.microsoft.com/library/windows/apps/hh755799.aspx).  
  
 Wenn Sie beabsichtigen, einen Ereignishandler hinzuzufügen und dann zu entfernen, müssen Sie die EventRegistrationToken-Struktur speichern, die durch den Vorgang des Hinzufügens zurückgegeben wird. Dann müssen Sie im Entfernungsvorgang die gespeicherte EventRegistrationToken-Struktur verwenden, um den zu entfernenden Ereignishandler zu identifizieren.  
  
### <a name="requirements"></a>Anforderungen  
 Compileroption: **/ZW**  
  
## <a name="common-language-runtime"></a>Common Language Runtime 
 Mit dem `event`-Schlüsselwort können Sie ein Ereignis deklarieren. Ein Ereignis ist eine Methode, anhand derer eine Klasse Benachrichtigungen übermitteln kann, wenn etwas von Interesse geschieht.  
  
 **Syntax**  
  
```  
  
// event data member  
modifiereventdelegate^ event_name;   
  
// event block  
modifiereventdelegate^ event_name   
{  
   modifierreturn_valueadd(delegate^ name);  
   modifier void remove(delegate^ name);  
   modifier void raise(parameters);  
}  
```  
  
 **Parameter**  
  
 *Modifizierer*  
 Ein Modifizierer, der entweder für die Ereignisdeklaration oder eine Ereigniszugriffsmethode verwendet werden kann.  Mögliche Werte sind `static` und `virtual`.  
  
 *delegate*  
 Die [Delegieren](../windows/delegate-cpp-component-extensions.md), deren Signatur der Ereignishandler übereinstimmen muss.  
  
 *event_name*  
 Der Name des Ereignisses.  
  
 *Rückgabewert*  
 Der Rückgabewert der Ereigniszugriffsmethode.  Um überprüfbar zu sein, muss der Rückgabetyp `void` sein.  
  
 *Parameter*  
 (optional) Parameter für die `raise` -Methode, die der Signatur des übereinstimmen der *Delegieren* Parameter.  
  
 **Hinweise**  
  
 Ein Ereignis ist eine Zuordnung zwischen einem Delegaten und einer Memberfunktion (Ereignishandler), die auf das Auslösen des Ereignisses reagiert und es Clients beliebiger Klassen ermöglicht, Methoden zu registrieren, die mit der Signatur und dem Rückgabetyp des zugrundeliegenden Delegaten übereinstimmen.  
  
 Der Delegat kann eine oder mehrere zugeordnete Methoden haben, die aufgerufen werden, wenn der Code angibt, dass das Ereignis aufgetreten ist. Ein Ereignis in einem Programm kann für andere Programme verfügbar gemacht werden, die auf die .NET Framework Common Language Runtime abzielen.  
  
 Es gibt zwei Arten von Ereignisdeklarationen:  
  
 *Ereignis-Datenmember*  
 Speicher für das Ereignis in der Form eines Members des Delegattyps wird vom Compiler für Datenmemberereignisse erstellt.  Ein Ereignisdatenmember muss innerhalb einer Klasse deklariert werden. Dies wird auch als triviales Ereignis bezeichnet (siehe untenstehendes Codebeispiel).  
  
 *Ereignis-Blöcke*  
 Über Ereignis-Blöcke können Sie das Verhalten der Add-, Remove- und Raise-Methoden anpassen, indem Sie Add-, Remove- und Raise-Methoden implementieren. Die Signatur der Add-, Remove- und Raise-Methoden muss mit der Signatur des Delegaten übereinstimmen.  Event-Block-Ereignisse sind keine Datenmember und jede Verwendung als Datenmember führt zu einem Compilerfehler. 
  
 Der Rückgabetyp des Ereignishandlers muss dem Rückgabetyp des Delegaten entsprechen.  
  
 In .NET Framework können Sie einen Datenmember behandeln, als wäre er eine Methode selbst (d. h. die `Invoke`-Methode des entsprechenden Delegaten). Sie müssen den Delegattyp vordefinieren, um einen verwalteten Ereignisdatenmember zu deklarieren. Im Gegensatz dazu definiert eine verwaltete Ereignismethode implizit den entsprechenden verwalteten Delegaten, sofern er noch nicht definiert ist.  Ein Codebeispiel finden Sie am Ende dieses Themas.  
  
 Wenn Sie ein verwaltetes Ereignis deklarieren, können Sie add- und remove-Accessoren angeben, die aufgerufen werden, wenn Ereignishandler über die Operatoren += und -= hinzugefügt oder entfernt werden. Die Add-, Remove- und Raise-Methoden können explizit aufgerufen werden.  
  
 Die folgenden Schritte müssen durchgeführt werden, um Ereignisse in Visual C++ zu erstellen und zu verwenden:  
  
1.  Erstellen oder Identifizieren eines Delegaten. Wenn Sie ein eigenes Ereignis definieren, müssen Sie auch sicherstellen, dass es einen Delegaten für die Verwendung mit dem `event`-Schlüsselwort gibt. Wenn das Ereignis vordefiniert ist, beispielsweise in .NET Framework, müssen die Consumer des Ereignisses lediglich den Namen des Delegaten kennen.  
  
2.  Erstellen Sie eine Klasse, die Folgendes enthält:  
  
    -   Ein aus dem Delegaten erstelltes Ereignis.  
  
    -   (optional) Eine Methode, die überprüft, dass eine Instanz des mit dem `event`-Schlüsselwort deklarierten Delegaten vorhanden ist. Andernfalls muss diese Logik im Code eingefügt werden, durch den das Ereignis ausgelöst wird.  
  
    -   Methoden, die das Ereignis aufrufen. Diese Methoden können Überschreibungen von Funktionen der Basisklasse sein.  
  
     Diese Klasse definiert das Ereignis.  
  
3.  Definieren Sie eine oder mehrere Klassen, die Methoden mit dem Ereignis verbinden. Jede dieser Klassen ordnet dem Ereignis in der Basisklasse eine oder mehrere Methoden zu.  
  
4.  Verwenden Sie das Ereignis:  
  
    -   Erstellen Sie ein Objekt der Klasse, die die Ereignisdeklaration enthält.  
  
    -   Erstellen Sie ein Objekt der Klasse, die die Ereignisdefinition enthält.  
  
 Weitere Informationen zu C + c++ / CLI-Ereignissen finden Sie unter  
  
-   [Ereignisse in einer Schnittstelle](../dotnet/how-to-use-events-in-cpp-cli.md)  
  
### <a name="requirements"></a>Anforderungen  
 Compileroption: **/clr**  
  
### <a name="examples"></a>Beispiele  
 **Beispiel**  
  
 Im folgenden Codebeispiel wird das Deklarieren von Paaren von Delegaten, Ereignissen und Ereignishandlers veranschaulicht, das Abonnieren (Hinzufügen) der Ereignishandler, das Aufrufen der Ereignishandler und dann das Kündigen des Abonnements (Entfernen) der Ereignishandler.  
  
```  
// mcppv2_events.cpp  
// compile with: /clr  
using namespace System;  
  
// declare delegates  
delegate void ClickEventHandler(int, double);  
delegate void DblClickEventHandler(String^);  
  
// class that defines events  
ref class EventSource {  
public:  
   event ClickEventHandler^ OnClick;   // declare the event OnClick  
   event DblClickEventHandler^ OnDblClick;   // declare OnDblClick  
  
   void FireEvents() {  
      // raises events  
      OnClick(7, 3.14159);  
      OnDblClick("Hello");  
   }  
};  
  
// class that defines methods that will called when event occurs  
ref class EventReceiver {  
public:  
   void OnMyClick(int i, double d) {  
      Console::WriteLine("OnClick: {0}, {1}", i, d);  
   }  
  
   void OnMyDblClick(String^ str) {  
      Console::WriteLine("OnDblClick: {0}", str);  
   }  
};  
  
int main() {  
   EventSource ^ MyEventSource = gcnew EventSource();  
   EventReceiver^ MyEventReceiver = gcnew EventReceiver();  
  
   // hook handler to event  
   MyEventSource->OnClick += gcnew ClickEventHandler(MyEventReceiver, &EventReceiver::OnMyClick);  
   MyEventSource->OnDblClick += gcnew DblClickEventHandler(MyEventReceiver, &EventReceiver::OnMyDblClick);  
  
   // invoke events  
   MyEventSource->FireEvents();  
  
   // unhook handler to event  
   MyEventSource->OnClick -= gcnew ClickEventHandler(MyEventReceiver, &EventReceiver::OnMyClick);  
   MyEventSource->OnDblClick -= gcnew DblClickEventHandler(MyEventReceiver, &EventReceiver::OnMyDblClick);  
}  
```  
  
 **Ausgabe**  
  
```Output  
OnClick: 7, 3.14159  
  
OnDblClick: Hello  
```  
  
 **Beispiel**  
  
 Im folgenden Codebeispiel wird die Logik zum Generieren der `raise`-Methode eines trivialen Ereignisses veranschaulicht: Wenn das Ereignis einen oder mehrere Abonnenten aufweist, wird beim impliziten oder expliziten Aufrufen der `raise`-Methode der Delegat aufgerufen. Wenn der Rückgabetyp des Delegattyps nicht `void` lautet und es keine Ereignisabonnenten gibt, gibt die `raise`-Methode den Standardwert für den Delegattyp zurück. Wenn keine Ereignisabonnenten vorhanden sind, wird beim Aufrufen der `raise`-Methode einfach zurückgegeben und keine Ausnahme ausgelöst. Wenn der Rückgabetyp des Delegaten nicht `void` lautet, wird der Delegattyp zurückgegeben.  
  
```  
// trivial_events.cpp  
// compile with: /clr /c  
using namespace System;  
public delegate int Del();  
public ref struct C {  
   int i;  
   event Del^ MyEvent;  
  
   void FireEvent() {  
      i = MyEvent();  
   }  
};  
  
ref struct EventReceiver {  
   int OnMyClick() { return 0; }  
};  
  
int main() {  
   C c;  
   c.i = 687;  
  
   c.FireEvent();  
   Console::WriteLine(c.i);  
   c.i = 688;  
  
   EventReceiver^ MyEventReceiver = gcnew EventReceiver();  
   c.MyEvent += gcnew Del(MyEventReceiver, &EventReceiver::OnMyClick);  
   Console::WriteLine(c.i);     
}  
```  
  
 **Ausgabe**  
  
```Output  
0  
  
688  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Komponentenerweiterungen für Laufzeitplattformen](../windows/component-extensions-for-runtime-platforms.md)