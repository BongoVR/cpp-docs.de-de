---
title: IDL-Attribute, Assistent zum Hinzufügen Methoden | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
f1_keywords:
- vc.codewiz.method.idlattrib
dev_langs:
- C++
helpviewer_keywords:
- Add Method Wizard [C++]
- IDL attributes, Add Method Wizard
ms.assetid: f80c3bc1-b515-4d6c-83ee-98c2c21ba902
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4a7a1e8fe89f64ad5909e7c1415545e3b3d80196
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="idl-attributes-add-method-wizard"></a>IDL-Attribute, Assistent zum Hinzufügen von Methoden
Verwenden Sie diese Seite des Assistenten zum Hinzufügen einer Methode, um alle Interface Definition Language (IDL)-Einstellungen für die Methode anzugeben.  
  
 **ID**  
 Legt fest, die numerische ID, die die Methode identifiziert. Finden Sie unter [Id](http://msdn.microsoft.com/library/windows/desktop/aa367040) in der *"MIDL" Referenz*.  
  
 Dieses Feld ist für benutzerdefinierte Schnittstellen nicht verfügbar und ist für MFC-Dispatchschnittstellen nicht verfügbar.  
  
 **call_as**  
 Gibt den Namen einer remote-Methode, dem diese lokale Methode zugeordnet werden kann. Finden Sie unter [Aufruf als](http://msdn.microsoft.com/library/windows/desktop/aa366748) in der *"MIDL" Referenz*.  
  
 Für MFC-Dispatchschnittstellen nicht verfügbar.  
  
 **helpcontext**  
 Gibt eine Kontext-ID, mit dem die Benutzerinformationen zu dieser Methode in der Hilfedatei. Finden Sie unter [Helpcontext](http://msdn.microsoft.com/library/windows/desktop/aa366851) in der *"MIDL" Referenz*.  
  
 Für MFC-Dispatchschnittstellen nicht verfügbar.  
  
 **helpstring**  
 Gibt eine Zeichenfolge, die verwendet wird, um das Element zu beschreiben, auf dem es angewendet. Standardmäßig wird es auf festgelegt "-Methode *Methodennamen*." Finden Sie unter [Helpstring](http://msdn.microsoft.com/library/windows/desktop/aa366856) in der *"MIDL" Referenz*.  
  
 Für MFC-Dispatchschnittstellen nicht verfügbar.  
  
 **Zusätzliche Attribute**  
 Für MFC-Dispatchschnittstellen nicht verfügbar.  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|**hidden**|Gibt an, dass die Methode vorhanden ist, aber nicht in einem Browser benutzerorientierte angezeigt werden soll. Finden Sie unter [ausgeblendete](http://msdn.microsoft.com/library/windows/desktop/aa366861) in der *"MIDL" Referenz*.|  
|**Datenquelle**|Gibt an, dass die Methode eine Quelle von Ereignissen angehört. Finden Sie unter [Quelle](http://msdn.microsoft.com/library/windows/desktop/aa367166) in der *"MIDL" Referenz*.|  
|`local`|Gibt die MIDL-Compiler, dass die Methode nicht remote ist. Finden Sie unter [lokale](http://msdn.microsoft.com/library/windows/desktop/aa367071) in der *"MIDL" Referenz*.|  
|**restricted**|Gibt an, dass die Methode nach dem Zufallsprinzip aufgerufen werden kann. Finden Sie unter [eingeschränkte](http://msdn.microsoft.com/library/windows/desktop/aa367157) in der *"MIDL" Referenz*.|  
|**vararg**|Gibt an, dass die Methode eine Variable Anzahl von Argumenten akzeptiert. Um dies zu erreichen, muss das letzte Argument ein sicheres Array von **VARIANT** Typ, der die übrigen Argumente enthält. Finden Sie unter [Vararg](http://msdn.microsoft.com/library/windows/desktop/aa367304) in der *"MIDL" Referenz*.|  
  
## <a name="see-also"></a>Siehe auch  
 [Hinzufügen einer Methode](../ide/adding-a-method-visual-cpp.md)   
 [Assistent zum Hinzufügen von Methoden](../ide/add-method-wizard.md)