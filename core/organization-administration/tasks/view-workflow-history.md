--- 
title: Workflowhistorie anzeigen
description: "Verwenden Sie diese Schritte, um den Status eines Dokuments anzuzeigen, das an das Workflowsystem zur Verarbeitung und Genehmigung übermittelt wurde."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a0e16467972596ad6d8b0d9785e68b487150781c
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="view-workflow-history"></a>Workflowhistorie anzeigen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Verwenden Sie diese Schritte, um den Status eines Dokuments anzuzeigen, das an das Workflowsystem zur Verarbeitung und Genehmigung übermittelt wurde. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Navigieren Sie zu „Gemeinsam” > „Abfragen” > „Workflow” > „Workflowhistorie”.
    * Mithilfe dieses Formulars können Sie den Status eines Dokuments anzeigen, das zur Verarbeitung und Genehmigung an das Workflowsystem übermittelt wurde.  
    * Die Insranz-ID ist der Kennungscode der Workflowinstanz, mit dem das Dokument verarbeitet wird oder verarbeitet wurde.  
    * Der Status ist der Workflowstatus des Dokuments.  
    * Die Workflow-ID ist der Kennungscode des Workflows, mit dem das Dokument verarbeitet wird oder verarbeitet wurde.  
    * Das „Dokument” ist der Kennungscode des Dokuments.  
    * Der Dokumenttyp ist der Typ von Dokument, der zur Verabeitung übermittelt wurde.  
    * Der Workflow ist der Name des Workflows, mit dem das Dokument verarbeitet wird oder wurde.  
    * Die Version ist die Versionsnummer des Workflows, mit dem das Dokument verarbeitet wird oder verarbeitet wurde.  
    * Das Erstellungsdatum und -uhrzeit ist das Datum und die Uhrzeit, an dem das Dokument übermittelt wurde.  
    * Die „Verstrichene Zeit” ist die seit der Übermittlung des Dokuments verstrichene Zeit.  
    * Mit der Schaltfläche „Fortsetzen” können Sie den Workflowprozess für das ausgewählte Dokument fortsetzen.  
    * Mit der Schaltfläche „Rückruf” könne Sie das ausgewälte Dokument zurückrufen, sodass es nicht verarbeitet wird.   
2. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Stellen Sie sicher, dass der Bereich „Arbeitsaufgaben” erweitert ist.    In diesem Abschnitt können Sie die Arbeitsaufgaben anzeigen, die dem ausgewählten Dokument zugeordnet sind. So muss eine Aufgabe möglicherweise abgeschlossen werden oder das Dokument muss möglicherweise genehmigt werden.  
    * Durch die Schaltfläche „Neu zuweisen” wird ein Dialogfeld geöffnet, in dem Sie eine Arbeitsaufgabe einem anderen Benutzer neu zuordnen können.  
    * Überprüfen Sie, ob der Bereich „Details nachverfolgen” erweitert ist.    In diesem Abschnitt können Sie die Workflowhistorie des ausgewählten Dokuments angezeigt.  


