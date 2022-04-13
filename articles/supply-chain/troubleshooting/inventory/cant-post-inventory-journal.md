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
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488966"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Bestandserfassungs-Workflow wird nie abgeschlossen und die Erfassung kann nicht verarbeitet werden

## <a name="symptoms"></a>Symptome

Nachdem Sie einen Workflow zur Genehmigung übermittelt haben, reagiert die Workflowverarbeitung nicht mehr und Sie können Ihre Erfassungen nicht mehr bearbeiten oder verarbeiten.

## <a name="resolution"></a>Lösung

Es gibt mehrere Gründe, warum die Workflowverarbeitung möglicherweise nicht abgeschlossen wird. Überprüfen Sie, ob folgende Probleme vorliegen:

- Wechseln Sie zu **Bestandsverwaltung &gt; Einrichten &gt; Bestandsverwaltungsworkflows** und überprüfen Sie die Konfiguration des betroffenen Workflows. Weitere Informationen finden Sie unter [Workflows zur Genehmigung von Lagererfassungen](../../inventory/inventory-journal-workflow.md).
- Im Workflow ist möglicherweise eine Ausnahme oder ein Fehler aufgetreten. Überprüfen Sie für den betroffenen Workflow den Verlauf des Arbeitselements, um festzustellen, ob er einen Anwendungsfehler enthält, der den Workflow beendet.
- Die Bestandserfassung kann nur aktualisiert oder bearbeitet werden, wenn sie genehmigt wurde. Wenn ein Rückruf aktiv ist, können Sie versuchen, die Erfassung zurückzurufen. Die Ausführung des Stapelauftrags für den Workflow kann aus mehreren Gründen ausgesetzt werden. Einige dieser Gründe können durch das Problem mit dem Workflowframework verursacht werden.
