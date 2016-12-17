---
title: "ptr::operator!"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "ptr::operator!"
  - "msclr::com::ptr::operator!"
  - "ptr.operator!"
  - "msclr.com.ptr.operator!"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ptr::operator!"
ms.assetid: 7f4101dc-2045-42e7-abb1-6a30e17147f2
caps.latest.revision: 9
caps.handback.revision: "7"
ms.author: "mblome"
manager: "ghogen"
---
# ptr::operator!
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

So bestimmen Sie, Operator, wenn das Besitze COM\-Objekt ungültig ist.  
  
## Syntax  
  
```  
bool operator!();  
```  
  
## Rückgabewert  
 `true`, wenn das Besitze COM\-Objekt ist ungültig; andernfalls `false`.  
  
## Hinweise  
 Das Besitze COM\-Objekt ist gültig, wenn er nicht `nullptr` ist.  
  
## Beispiel  
 Dieses Beispiel implementiert eine CLR\-Klasse, die `com::ptr` verwendet, um sein `IXMLDOMDocument`\-Objekt des privaten Members zu umschließen.  Die `CreateInstance`\-Memberfunktion verwendet `operator!`, um zu bestimmen, ob ein Document\-Objekt bereits verwendet wird, und erstellt nur eine neue Instanz, wenn das Objekt nicht gültig ist.  
  
```  
// comptr_op_not.cpp  
// compile with: /clr /link msxml2.lib  
#include <msxml2.h>  
#include <msclr\com\ptr.h>  
  
#import <msxml3.dll> raw_interfaces_only  
  
using namespace System;  
using namespace System::Runtime::InteropServices;  
using namespace msclr;  
  
// a ref class that uses a com::ptr to contain an   
// IXMLDOMDocument object  
ref class XmlDocument {  
public:  
   void CreateInstance(String^ progid) {  
      if (!m_ptrDoc) {  
         m_ptrDoc.CreateInstance(progid);     
         if (m_ptrDoc) {  
            Console::WriteLine("DOM Document created.");  
         }  
      }  
   }  
  
   // note that the destructor will call the com::ptr destructor  
   // and automatically release the reference to the COM object  
  
private:  
   com::ptr<IXMLDOMDocument> m_ptrDoc;  
};  
  
// use the ref class to handle an XML DOM Document object  
int main() {  
   try {  
      XmlDocument doc;  
      // create the instance from a progid string  
      doc.CreateInstance("Msxml2.DOMDocument.3.0");  
   }  
   catch (Exception^ e) {  
      Console::WriteLine(e);     
   }  
}  
```  
  
  **DOM\-Dokument erstellt.**   
## Anforderungen  
 **Headerdatei** \<msclr\\com\\ptr.h\>  
  
 **Namespace** msclr::com  
  
## Siehe auch  
 [ptr\-Member](../dotnet/ptr-members.md)   
 [ptr::operator bool](../dotnet/ptr-operator-bool.md)