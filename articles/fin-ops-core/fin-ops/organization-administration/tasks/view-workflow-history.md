---
title: Anzeigen der Workflowhistorie
description: In diesem Thema werden die Schritte beschrieben, um den Status eines Dokuments anzuzeigen, das zur Verarbeitung und Genehmigung an das Workflowsystem übermittelt wurde.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351f9c80eab8e9810fa6a4538f003eaef1a4a4fd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747224"
---
# <a name="view-workflow-history"></a>Anzeigen der Workflowhistorie

[!include [banner](../../includes/banner.md)]

In diesem Thema werden die Schritte beschrieben, um den Status eines Dokuments anzuzeigen, das zur Verarbeitung und Genehmigung an das Workflowsystem übermittelt wurde. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Wechseln Sie zu **Navigationsbereich > Module > Allgemein > Abfragen > Workflow > Workflowhistorie**.
    - Mithilfe dieses Formulars können Sie den Status eines Dokuments anzeigen, das zur Verarbeitung und Genehmigung an das Workflowsystem übermittelt wurde.  
    - Die **Instanzkennung** ist der Kennungscode der Workflowinstanz, mit der das Dokument verarbeitet wird oder verarbeitet wurde.  
    - Der **Status** ist der Workflowstatus des Dokuments.  
    - Die **Workflowkennung** ist der Kennungscode des Workflows, mit dem das Dokument verarbeitet wird oder verarbeitet wurde.  
    - Das **Dokument** ist der Kennungscode des Dokuments.  
    - Der **Dokumenttyp** ist der Typ des Dokuments, das zur Verarbeitung übermittelt wurde.  
    - Der **Workflow** ist der Name des Workflows, mit dem das Dokument verarbeitet wird oder wurde.  
    - Die **Version** ist die Versionsnummer des Workflows, mit dem das Dokument verarbeitet wird oder verarbeitet wurde.  
    - Das **Erstellungsdatum und -uhrzeit** ist das Datum und die Uhrzeit, an dem das Dokument übermittelt wurde.  
    - Die **Verstrichene Zeit** ist die seit der Übermittlung des Dokuments verstrichene Zeit.  
    - Mit der Schaltfläche **Fortsetzen** können Sie den Workflowprozess für das ausgewählte Dokument fortsetzen.  
    - Mit der Schaltfläche **Rückruf** können Sie das ausgewählte Dokument zurückrufen, sodass es nicht verarbeitet wird.   
2. Wählen Sie in der Liste den Link in der gewünschten Zeile aus.
    - Stellen Sie sicher, dass der Bereich **Arbeitsaufgaben** erweitert ist. In diesem Abschnitt können Sie die Arbeitsaufgaben anzeigen, die dem ausgewählten Dokument zugeordnet sind. So muss eine Aufgabe möglicherweise abgeschlossen werden oder das Dokument muss möglicherweise genehmigt werden.  
    - Durch die Schaltfläche **Neu zuweisen** wird ein Dialogfeld geöffnet, in dem Sie eine Arbeitsaufgabe einem anderen Benutzer neu zuordnen können.  
    - Überprüfen Sie, ob der Bereich **Verfolgungsdetails** erweitert ist. In diesem Abschnitt können Sie die Workflowhistorie des ausgewählten Dokuments angezeigt.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]