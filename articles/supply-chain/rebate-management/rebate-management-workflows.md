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
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0fe5bc5af953ee7cbbda3477d75a38261bb2bb10
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687411"
---
# <a name="rebate-management-deal-workflows"></a>Workflows für Rückvergütungsverwaltungsdeals

[!include [banner](../includes/banner.md)]

Um Rückvergütungsdeals zu genehmigen, verwendet die Rückvergütungsverwaltung dieselbe Workflow-Plattform wie andere Finanz- und Betriebs-Apps. Jedem Workflow sind zwei Auftragsprozesse zugeordnet:

- Ein Element des Workflows genehmigt den Deal.
- Ein Element des Workflows aktiviert den Deal, sodass der Benutzer oder der Workflowprozess die Transaktionen genehmigen kann.

Bevor Sie einen Rückvergütungsdeal verwenden können, muss der im Modul **Rückvergütungsverwaltung** aktiviert werden. Um einen Deal zu aktivieren, müssen Sie zuerst einen *Workflow für Rückvergütungsverwaltungsdeals* erstellen und konfigurieren.

Benutzer können Geschäfte nicht manuell genehmigen. Es muss immer der Workflow verwendet werden.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Workflows für Rückvergütungsverwaltungsdeals erstellen und verwalten

Um mit Ihren Workflows für Rückvergütungsverwaltungsdeals zu arbeiten, gehen Sie zu **Rückvergütungsverwaltung \> Einstellungen \> Workflows für Rückvergütungsverwaltung**. Dort können Sie Workflows nach Bedarf anzeigen, erstellen und aktualisieren. Nur jeweils ein Workflow dieses Typs kann aktiv sein. Weitere Informationen zu Workflows, zum Arbeiten mit der Seite **Workflows für Rückvergütungsverwaltungsdeals** und zum Erstellen von Workflows finden Sie unter [Workflowsystem – Übersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) und den dazugehörigen Themen.

## <a name="use-a-workflow-to-activate-a-deal"></a>Einen Workflow zum Aktivieren eines Deals verwenden

Um einen Deal über einen Workflow zu aktivieren, öffnen Sie den Deal (z. B. auf der Seite **Alle Rückvergütungsverwaltungsdeals**). Wählen Sie im Aktivitätsbereich **Workflow \> Senden**. Nachdem der neue Deal über den Workflow verarbeitet und genehmigt wurde, ist es aktiv und einsatzbereit.

Nachdem ein Geschäft aktiviert wurde, können Sie die meisten seiner Einstellungen nicht mehr ändern. Wenn Sie ein aktives Geschäft ändern müssen, inaktivieren Sie es zuerst und erstellen Sie dann ein neues Geschäft. Wenn der neue Deal dem alten ähnelt, können Sie ihn erstellen, indem Sie den alten Deal kopieren.

Sie können die folgenden Einstellungen für ein Geschäft ändern, nachdem es aktiviert wurde:

- Abstimmen nach
- Kumulative Garantie
- Buchungsprofil
- Buchungsprofil für Garantie
- Dokumentnotizen
- Währung
- Anfangsdatum
- Bis-Datum

Darüber hinaus können Bonuszeilen entfernt werden.
