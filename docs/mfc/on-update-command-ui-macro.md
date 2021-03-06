---
title: ON_UPDATE_COMMAND_UI-Makro | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- ON_UPDATE_COMMAND_UI
dev_langs:
- C++
helpviewer_keywords:
- ON_UPDATE_COMMAND_UI macro [MFC]
- update handlers [MFC]
- command-handler macros
- updating user-interface objects [MFC]
ms.assetid: 3e72b50f-4119-4c82-81cf-6e09b132de05
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 726eba2edbb857784a3a23ddcfb2d69fd8e30a72
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="onupdatecommandui-macro"></a>ON_UPDATE_COMMAND_UI Macro
Verwenden der **Eigenschaften** Fenster aus, um ein Objekt für die Benutzeroberfläche ein Befehl / Update-Ereignishandler in einem Befehlszielobjekt verbinden. Es wird automatisch verbinden, die Benutzeroberflächen-Objekt-ID, die `ON_UPDATE_COMMAND_UI` Makro und erstellen Sie einen Ereignishandler, in dem Objekt, das Update behandelt wird. Finden Sie unter [Zuordnen von Meldungen zu Funktionen](../mfc/reference/mapping-messages-to-functions.md) für Weitere Informationen.  
  
 Verwenden Sie z. B. um einen Befehl alle Löschen Ihres Programms Bearbeitungsmenü zu aktualisieren, die **Eigenschaften** Fenster hinzuzufügende eine Meldungszuordnungseintrags in der ausgewählten Klasse ist die Deklaration einer Funktion für einen Befehl / Update-Handler mit der Bezeichnung `OnUpdateEditClearAll` in der Klasse Deklaration, und eine leere Funktionsvorlage in der Klassenimplementierungsdatei. Der Funktionsprototyp sieht wie folgt:  
  
 [!code-cpp[NVC_MFCDocView#2](../mfc/codesnippet/cpp/on-update-command-ui-macro_1.h)]  
  
 Wie alle Handler, der Funktion zeigt den **Afx_msg** Schlüsselwort. Wie alle Handler aktualisieren, dauert es ein Argument, ein Zeiger auf eine `CCmdUI` Objekt.  
  
## <a name="see-also"></a>Siehe auch  
 [Vorgehensweise: Aktualisieren von Benutzeroberflächenobjekten](../mfc/how-to-update-user-interface-objects.md)

