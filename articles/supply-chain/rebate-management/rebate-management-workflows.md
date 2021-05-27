---
title: Workflows für Rückvergütungsverwaltungsdeals
description: In diesem Thema wird erläutert, wie Sie einen Workflow für Rückvergütungsverwaltungsdeals einrichten, um Deals zu genehmigen und zu aktivieren.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020385"
---
# <a name="rebate-management-deal-workflows"></a>Workflows für Rückvergütungsverwaltungsdeals

[!include [banner](../includes/banner.md)]

Um Rückvergütungsdeals zu genehmigen, verwendet die Rückvergütungsverwaltung dieselbe Workflow-Plattform wie andere Finance and Operations-Apps. Jedem Workflow sind zwei Auftragsprozesse zugeordnet:

- Ein Element des Workflows aktiviert den Deal, sodass der Benutzer oder der Workflowprozess die Transaktionen genehmigen kann.
- Ein Element des Workflows genehmigt den Deal.

Bevor Sie einen Rückvergütungsdeal verwenden können, muss der im Modul **Rückvergütungsverwaltung** aktiviert werden. Um einen Deal zu aktivieren, müssen Sie zuerst einen *Workflow für Rückvergütungsverwaltungsdeals* erstellen und konfigurieren.

Nachdem ein Workflow für die Rückvergütungsverwaltung aktiviert wurde, können Benutzer Deals nicht manuell genehmigen. Der Workflow muss immer verwendet werden.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Workflows für Rückvergütungsverwaltungsdeals erstellen und verwalten

Um mit Ihren Workflows für Rückvergütungsverwaltungsdeals zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Einstellungen \> Workflows für Rückvergütungsverwaltung**. Dort können Sie Workflows nach Bedarf anzeigen, erstellen und aktualisieren. Nur jeweils ein Workflow dieses Typs kann aktiv sein. Weitere Informationen zu Workflows, zum Arbeiten mit der Seite **Workflows für Rückvergütungsverwaltungsdeals** und zum Erstellen von Workflows finden Sie unter [Workflowsystem – Übersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) und den dazugehörigen Themen.

## <a name="use-a-workflow-to-activate-a-deal"></a>Einen Workflow zum Aktivieren eines Deals verwenden

Um einen Deal über einen Workflow zu aktivieren, öffnen Sie den Deal (z. B. auf der Seite **Alle Rückvergütungsverwaltungsdeals**). Wählen Sie im Aktivitätsbereich **Workflow \> Senden**. Nachdem der neue Deal über den Workflow verarbeitet und genehmigt wurde, ist es aktiv und einsatzbereit.

Nachdem ein Deal aktiviert wurde, können Sie dessen Einstellungen nicht mehr ändern. Wenn Sie einen aktiven Deal ändern müssen, deaktivieren Sie ihn und erstellen Sie einen neuen. Wenn der neue Deal dem alten ähnelt, können Sie ihn erstellen, indem Sie den alten Deal kopieren.
