---
title: Bestandserfassungs-Workflow wird nie abgeschlossen und die Erfassung kann nicht verarbeitet werden
description: Nachdem Sie einen Workflow zur Genehmigung übermittelt haben, reagiert die Workflowverarbeitung nicht mehr und Sie können Ihre Erfassungen nicht mehr bearbeiten oder verarbeiten.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476406"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Bestandserfassungs-Workflow wird nie abgeschlossen und die Erfassung kann nicht verarbeitet werden

## <a name="symptoms"></a>Symptome

Nachdem Sie einen Workflow zur Genehmigung übermittelt haben, reagiert die Workflowverarbeitung nicht mehr und Sie können Ihre Erfassungen nicht mehr bearbeiten oder verarbeiten.

## <a name="resolution"></a>Lösung

Es gibt mehrere Gründe, warum die Workflowverarbeitung möglicherweise nicht abgeschlossen wird. Überprüfen Sie, ob folgende Probleme vorliegen:

- Wechseln Sie zu **Bestandsverwaltung &gt; Einrichten &gt; Bestandsverwaltungsworkflows** und überprüfen Sie die Konfiguration des betroffenen Workflows. Weitere Informationen finden Sie unter [Workflows zur Genehmigung von Lagererfassungen](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- Im Workflow ist möglicherweise eine Ausnahme oder ein Fehler aufgetreten. Überprüfen Sie für den betroffenen Workflow den Verlauf des Arbeitselements, um festzustellen, ob er einen Anwendungsfehler enthält, der den Workflow beendet.
- Die Bestandserfassung kann nur aktualisiert oder bearbeitet werden, wenn sie genehmigt wurde. Wenn ein Rückruf aktiv ist, können Sie versuchen, die Erfassung zurückzurufen. Die Ausführung des Stapelauftrags für den Workflow kann aus mehreren Gründen ausgesetzt werden. Einige dieser Gründe können durch das Problem mit dem Workflowframework verursacht werden.
