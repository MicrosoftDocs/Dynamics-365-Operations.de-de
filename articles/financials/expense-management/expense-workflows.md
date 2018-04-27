---
title: "Workflows für Ausgaben einrichten"
description: "Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cf35406b43c1ec40a7c248b970559b65fcd8a6c6
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-workflows-for-expense"></a>Workflows für Ausgaben einrichten

[!INCLUDE [banner](../includes/banner.md)]

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


