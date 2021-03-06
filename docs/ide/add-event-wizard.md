---
title: Ereignis-Assistent zum Hinzufügen von | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
f1_keywords:
- vc.codewiz.event.overview
dev_langs:
- C++
helpviewer_keywords:
- Add Event Wizard [C++]
ms.assetid: bdd2a7bb-13d5-44d7-abc9-e785ba4e05ce
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: f92f871f22fb01f3f0f37677c393fcd481c08120
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="add-event-wizard"></a>Assistent zum Hinzufügen von Ereignissen
Dieser Assistent fügt ein Ereignis zu einem MFC-ActiveX-Steuerelement-Projekt. Können Sie ein eigenes Ereignis angeben, können Sie in der Regel Basisereignis anpassen oder Sie können aus einer Liste von vordefinierten Ereignissen auswählen.  
  
 **Ereignisname**  
 Legt den Namen von-Clients verwendet wird, um ein Ereignis von der Klasse anzufordern. Geben Sie einen Namen ein, oder wählen Sie aus der Liste.  
  
 **Ereignistyp**  
 Gibt den Typ des Ereignisses hinzugefügt. Nur verfügbar, wenn Sie wählen die **Ereignisname** Liste.  
  
|Option|Beschreibung|  
|------------|-----------------|  
|**Stock**|Gibt an, dass ein vordefiniertes Ereignis, z. B. eine Schaltfläche klicken, für diese Klasse implementiert werden. Vordefinierte Ereignisse werden in der Microsoft Foundation Class (MFC)-Bibliothek definiert.|  
|**Benutzerdefiniert**|Gibt an, dass Sie Ihre eigene Implementierung des Ereignisses bereitstellen.|  
  
 **Interner name**  
 Legt den Namen der Memberfunktion, die das Ereignis sendet. Verfügbar nur für benutzerdefinierte Ereignisse. Der Name basiert auf **Ereignisname**. Sie können den internen Namen ändern, wenn Sie einen anderen als Namen angeben möchten **Ereignisname**.  
  
 **Parametertyp**  
 Legt den Typ für die **Parametername**. Wählen Sie den Typ aus der Liste aus.  
  
 **Parametername**  
 Legt den Namen eines Parameters für die Weiterleitung über das Ereignis. Klicken Sie nach Eingabe des Namens, Sie müssen auf **hinzufügen** die Liste der Parameter hinzufügen.  
  
 Nach dem Klicken auf **hinzufügen**, der Name des Parameters angezeigt wird, im **Parameterliste**.  
  
> [!NOTE]
>  Wenn Sie einen Parameternamen angeben, und klicken Sie dann auf **Fertig stellen** klicken Sie erst **hinzufügen**, und klicken Sie dann der Parameter nicht auf das Ereignis hinzugefügt wird. Sie müssen suchen Sie die Methode, und fügen Sie den Parameter manuell. **Parameterliste**  
  
 **Add**  
 Fügt die Parameter, die Sie, in angeben **Parametername**, und dessen Typ auf **Parameterliste**. Klicken Sie auf **hinzufügen** der Liste einen Parameter hinzu.  
  
 **Entfernen**  
 Entfernt den Parameter, die Sie, in auswählen **Parameterliste** aus der Liste.  
  
 **Parameterliste**  
 Zeigt alle Parameter und ihre Typen, die derzeit für die Methode hinzugefügt. Wenn Sie Parameter hinzufügen, wird der Assistent aktualisiert **Parameterliste** mit seinem Typ jedes Parameters angezeigt.  
  
## <a name="see-also"></a>Siehe auch  
 [Hinzufügen eines Ereignisses](../ide/adding-an-event-visual-cpp.md)