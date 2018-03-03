---
title: Projektbuildwarnung prj0041 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- PRJ0041
dev_langs:
- C++
helpviewer_keywords:
- PRJ0041
ms.assetid: dc9f4cf9-6bd5-4222-89e8-7802a59bb96b
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 231b58cb0c13d1a3f87e010a5100da564b0be806
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="project-build-warning-prj0041"></a>Projektbuildwarnung PRJ0041
Kann nicht gefunden werden fehlende Abhängigkeit 'Abhängigkeit' für Datei "File". Das Projekt kann zwar erstellt, aber unter Umständen nicht mehr aktuell angezeigt werden, bis diese Datei gefunden wird.  
  
 Eine Datei (Ressourcendatei oder.idl/.odl-Datei, z. B. enthalten eine Include-Anweisung, die das Projektsystem nicht aufgelöst werden konnte.  
  
 Da das Projektsystem präprozessoranweisungen (z. B. #if) nicht verarbeitet werden, möglicherweise die problematische Anweisung nicht tatsächlich Teil des Builds.  
  
 Um diese Warnung zu beheben, löschen Sie alle nicht benötigten Code in der RC-Dateien oder fügen Sie Platzhalterdateien mit dem entsprechenden Namen hinzu.