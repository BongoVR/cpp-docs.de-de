---
title: Dialogfeld "Ressource" hinzufügen | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- vc.editors.insertresource
dev_langs:
- C++
helpviewer_keywords:
- resources [Visual Studio], adding
- Add Resource dialog box
ms.assetid: e9fb6967-738f-47e8-ab58-728cf35b3af0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: c420a1d72aa4ceca7d71840fcccb451b6e0aba0f
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="add-resource-dialog-box"></a>Ressource hinzufügen (Dialogfeld)
Verwenden Sie dieses Dialogfeld zum Hinzufügen von Ressourcen zu einem C++-Windows-Desktopanwendungs-Projekt.  
  
> [!NOTE]
>  Diese Informationen gelten nicht für Ressourcen in Uwp-apps. Weitere Informationen finden Sie unter [App-Ressourcen und die Ressourcenverwaltungssystem](/windows/uwp/app-resources/).  
  
 **Ressourcentyp**  
 Gibt die Art der zu erstellenden Ressource an.  
  
 Der Cursor und die Kategorien der Dialogfeldressourcen können zum Anzeigen zusätzlicher Ressourcen erweitert werden. Diese Ressourcen befinden sich im Visual Studio-...\Microsoft `version`\VC\VCResourceTemplates\\< LCID\>\mfc.rct. Wenn Sie RCT-Dateien hinzufügen, sie in diesem Verzeichnis abgelegt werden müssen, oder Sie geben eine [Includepfad](../windows/how-to-specify-include-directories-for-resources.md) für sie. Die Ressourcen in diesen Dateien werden dann auf der zweiten Ebene der entsprechenden Kategorie angezeigt. Die Anzahl von RCT-Dateien, die hinzugefügt werden können, ist nicht beschränkt.  
  
 Die auf der obersten Ebene der Strukturansicht angezeigten Ressourcen sind die von Visual Studio bereitgestellten Standardressourcen.  
  
 **Neu**  
 Erstellt eine Ressource, auf Grundlage des Typs, die Sie, in ausgewählt haben der **Ressourcentyp** Feld. Die Ressource wird im geeigneten Editor geöffnet. Z. B. Erstellen einer Dialogfeldressource Öffnen der [Dialog-Editor](../windows/dialog-editor.md).  
  
 **Importieren**  
 Öffnet die **importieren** (Dialogfeld), in dem Sie können auf eine Ressource Sie navigieren, in Ihrem aktuellen Projekt importieren möchten. Sie können eine Bitmap, ein Symbol, einen Cursor, eine HTML-Ressourcendatei, eine Sound-Ressourcendatei (.WAV) oder eine benutzerdefinierte Ressourcendatei importieren.  
  
 **Benutzerdefiniert**  
 Öffnet die [Dialogfeld "neue benutzerdefinierte Ressource"](../windows/new-custom-resource-dialog-box.md) in dem Sie eine benutzerdefinierte Ressource erstellen können. Benutzerdefinierte Ressourcen können nur im Binär-Editor bearbeitet werden.  
  
## <a name="requirements"></a>Anforderungen  
 Keiner  
  
## <a name="see-also"></a>Siehe auch  
 [Vorgehensweise: Erstellen einer Ressource](../windows/how-to-create-a-resource.md)