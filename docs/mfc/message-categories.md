---
title: Nachricht Kategorien | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- messages [MFC], categories
- control-notification messages [MFC]
- Windows messages [MFC], categories
- controls [MFC], notifications
- command messages [MFC]
- messages [MFC], Windows
- message handling [MFC], message types
ms.assetid: 68e1db75-9da6-4a4d-b2c2-dc4d59f8d87b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7d0e4710c74c12bf62cd19df6a053aea9ac35eaf
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="message-categories"></a>Meldungskategorien
Welche Arten von Nachrichten Sie Handler schreiben, es sind drei Hauptkategorien unterteilt:  
  
1.  Windows-Meldungen  
  
     Dazu gehören in erster Linie diese Meldungen, die mit Beginn der **WM_** Präfix, mit Ausnahme von **WM_COMMAND**. Durch Windows und Ansichten werden Windows-Meldungen verarbeitet. Diese Nachrichten haben oft Parameter, die verwendet werden, bestimmen, wie die Nachricht verarbeitet.  
  
2.  Steuerelementbenachrichtigungen  
  
     Dies schließt **WM_COMMAND** benachrichtigungsmeldungen aus den Steuerelementen und anderen untergeordneten Fenster an übergeordneten Fenster. Beispielsweise sendet ein Bearbeitungssteuerelement seinem übergeordneten Element ein **WM_COMMAND** Nachricht mit der **EN_CHANGE** steuerelementebenachrichtigung Code, wenn der Benutzer eine Aktion ausgeführt hat möglicherweise Text im Bearbeitungssteuerelement geändert haben. Handler für das Fenster für die Nachricht antwortet auf die Nachricht in einer geeigneten Weise, wie z. B. den Text im Steuerelement abruft.  
  
     Das Framework leitet wie andere Steuerelemente-benachrichtigungsmeldungen **WM_** Nachrichten. Eine Ausnahme ist jedoch die **BN_CLICKED** Steuerelement-Benachrichtigung, die von Schaltflächen gesendet werden, wenn der Benutzer darauf klickt. Diese Meldung dient speziell als Befehlsnachricht behandelt und wie andere Befehle weitergeleitet.  
  
3.  Befehlsmeldungen  
  
     Dies schließt **WM_COMMAND** Benachrichtigungen von Benutzeroberflächenobjekten: Menüs, Symbolleisten-Schaltflächen und Zugriffstasten. Das Framework verarbeitet Befehle anders als andere Meldungen, und können vom von Objekten, für verschiedene Arten behandelt werden, wie in beschrieben [Befehlsziele](../mfc/command-targets.md).  
  
##  <a name="_core_windows_messages_and_control.2d.notification_messages"></a> Windows-Meldungen und Steuerelemente-Benachrichtigungsmeldungen  
 Nachrichten in die Kategorien 1 und 2 – Windows-Meldungen und steuerelementbenachrichtigungen – werden von Windows gehandhabt: Objekte der Klassen, die von Klasse abgeleitet `CWnd`. Dies schließt `CFrameWnd`, `CMDIFrameWnd`, `CMDIChildWnd`, `CView`, `CDialog`, und Ihren eigenen Klassen aus dieser Basisklassen abgeleitet. Solche Objekte kapseln einer `HWND`, ein Handle für ein Windows-Fenster.  
  
##  <a name="_core_command_messages"></a> Befehlsmeldungen  
 Nachrichten in der Kategorie 3 – Befehle – kann durch eine größere Bandbreite von Objekten behandelt werden: Dokumente, Dokumentvorlagen und der Application-Objekt selbst, zusätzlich zu den Windows- und Ansichten. Wenn Sie ein Befehl direkt auf ein bestimmtes Objekt auswirkt, ist es sinnvoll, dieses Objekt den Befehl behandelt haben. Z. B. der Befehl Öffnen im Menü Datei der Anwendung logisch zugeordnet ist: die Anwendung öffnet ein angegebenes Dokument nach dem Empfang des Befehls. Daher wird der Handler für den Befehl zum Öffnen eine Memberfunktion der Anwendungsklasse. Weitere Informationen zu Befehlen und wie diese Objekte weitergeleitet werden, finden Sie unter [wie das Framework einen Handler aufruft](../mfc/how-the-framework-calls-a-handler.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Meldungen und Befehle im Framework](../mfc/messages-and-commands-in-the-framework.md)

