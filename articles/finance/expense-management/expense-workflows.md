---
title: Workflows für die Ausgabenverwaltung einrichten
description: Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153993"
---
# <a name="set-up-workflows-for-expense-management"></a>Workflows für die Ausgabenverwaltung einrichten

[!include [banner](../includes/banner.md)]

Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten. Zu den Dokumenten, für die Workflows definiert werden können, gehören Spesenabrechnungen, Reiseanforderungen, Kreditkartenstreitigkeiten und Barvorschussanforderungen.

Ein Workflow stellt einen Geschäftsprozess dar. Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss. Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:

-   **Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen. Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.

-   Prozesssichtbarkeit – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen. So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.

-   Zentralisierte Arbeitsliste – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen. 

**Erstellbare Workflowtypen**

In der folgenden Tabelle sind die Workflowtypen aufgeführt, die unter **Ausgaben** erstellt werden können.


|              <strong>Typ</strong>              |                   <strong>Mit diesem Typ können Sie folgende Aufgaben ausführen:</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Spesenabrechnung</strong>         |            Erstellen von Genehmigungsworkflows für Spesenabrechnungen             |
|  <strong>Automatische Buchung von Spesenabrechnung</strong>   |        Erstellen automatischer Buchungsworkflows für Spesenabrechnungen        |
|       <strong>Ausgabenposition</strong>        |     Erstellen von Genehmigungsworkflows für Positionsartikel in Spesenabrechnungen      |
| <strong>Automatische Buchung von Ausgabenpositionen</strong> | Erstellen von Workflows zum automatischen Buchen von Positionsartikeln in Spesenabrechnungen |
|       <strong>Reiseanforderung</strong>       |          Erstellen von Workflows für die Genehmigung von Reiseanforderungen           |
|      <strong>Barvorschussanforderung</strong>      |         Erstellen von Genehmigungsworkflows für Barvorschussanforderungen          |
|        <strong>USt.-Beitreibung</strong>        | Erstellen von Genehmigungsworkflows für die Beitreibung der Mehrwertsteuer (MwSt.)  |

