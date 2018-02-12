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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a>Workflows für Ausgaben einrichten

[!include[banner](../includes/banner.md)] Sie können einen Workflowprozess zum Prüfen und Genehmigen von Reisekosten- und Ausgabendokumenten einrichten. Zu den Dokumenten, für die Workflows definiert werden können, gehören Spesenabrechnungen, Reiseanforderungen, Kreditkartenstreitigkeiten und Barvorschussanforderungen.

Ein Workflow stellt einen Geschäftsprozess dar. Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss. Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:

-   **Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen. Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.

-   Prozesssichtbarkeit – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen. So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.

-   Zentralisierte Arbeitsliste – Benutzer können eine zentralisierte Arbeitsliste öffnen, um die ihnen zugeordneten Workflowaufgaben und -genehmigungen anzuzeigen. 

**Erstellbare Workflowtypen**

In der folgenden Tabelle sind die Workflowtypen aufgeführt, die unter **Ausgaben** erstellt werden können.

| **Typ**                           | **Mit diesem Typ können Sie folgende Aufgaben ausführen:**                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| **Spesenabrechnung**                 | Erstellen von Genehmigungsworkflows für Spesenabrechnungen                       |      
| **Automatische Buchung von Spesenabrechnung**    | Erstellen automatischer Buchungsworkflows für Spesenabrechnungen              |     
| **Ausgabenposition**              | Erstellen von Genehmigungsworkflows für Positionsartikel in Spesenabrechnungen         |     
| **Automatische Buchung von Ausgabenpositionen** | Erstellen von Workflows zum automatischen Buchen von Positionsartikeln in Spesenabrechnungen|
| **Reiseanforderung**             | Erstellen von Workflows für die Genehmigung von Reiseanforderungen                   |    
| **Barvorschussanforderung**           | Erstellen von Genehmigungsworkflows für Barvorschussanforderungen                 |     
| **USt.-Beitreibung**               | Erstellen von Genehmigungsworkflows für die Beitreibung der Mehrwertsteuer (MwSt.) |       

