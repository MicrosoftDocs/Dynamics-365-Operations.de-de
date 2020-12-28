---
title: Fortschrittlicher Mitarbeitereintrag und ‑Navigation
description: Dateneingabe für Arbeitskräfte in Dynamics 365 Talent wurde verbessert, um eine schnelle Eingabe für alle Mitarbeiter zu ermöglichen, und zwar für ehemalige, aktive und künftige Mitarbeiter. Vereinfachtes/konsolidiertes Navigationsmodell wurde aktualisiert, um zugehörige Informationen und Anzeigen rasch zu finden und erforderliche Aktualisierungen vornehmen zu können.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: b73b420c2eb75077814fbfeb6cd17404c7efc11e
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2020
ms.locfileid: "4461342"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Fortschrittlicher Mitarbeitereintrag und ‑Navigation

Dynamics 365 Talent ermöglicht effiziente Eingabe des Mitarbeiters sowie Beschäftigungsdaten. Sie können die Arbeitsverlaufinformationen für vergangene, aktive und künftige Mitarbeiter und Auftragnehmer aktualisieren.

Sie können auch eine vereinfachte Navigationserfahrung aktivieren, um zugehörige Informationen schnell zu finden und erforderliche Änderungen vorzunehmen. Diese Funktionalität ist in allen Umgebungen verfügbar. Navigieren Sie zum Aktivieren dieser Funktion zu **Systemverwaltung> Funktionsvewaltung > Neu> Fortschrittlicher Mitarbeitereintrag > Aktivieren**. Dies aktiviert diese Änderungen für alle Benutzer. Sie können diese Option jederzeit deaktivieren.

## <a name="view-options"></a>Optionen anzeigen

Sie können **Ansichtsoptionen** im Arbeitskraftformular verwenden, um beliebige Kombination aus Mitarbeitern von Auftragnehmern und von einer Einheitsliste auszuwählen. Diese Optionen ermöglichen Ihnen, die Arbeitskräfte über juristischen Personen oder für die juristische Person anzuzeigen, für die Sie aktuell angemeldet sind. Sie können auch die aktiven, ausstehenden und abgeschlossenen Arbeitskräfte anzeigen und Sie können Ergebnisse basierend auf dem Arbeitskrafttyp einschränken (Mitarbeiter oder Auftragnehmer). Wenn die erweiterte Sicherheit aktiviert ist, werden nur die Mitarbeiter und Auftragnehmer in den juristischen Personen angezeigt, auf die Sie Zugriff haben.

Spalten in der Listenansicht ändern basierend auf der getroffenen Auswahl. Zum Beispiel wenn Sie ausgetretene Mitarbeiter anzeigen, wird das Kündigungsdatum und die erstellten Ursachencodes als zusätzliche Spalten in der Liste angezeigt. 

[![Optionen anzeigen](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Navigation und Banner

Ein Banner zeigt die wichtigsten Informationen für jede Arbeitskraft an. Das aktive Banner für Arbeitskräfte zeigt die folgenden Felder an:

- **Titel**
- **Abteilung**
- **Positionstyp**
- **Arbeitskrafttyp**
- **Vorgesetzter**
- **Juristische Person**

Das Banner für ausgetretene Arbeitskräfte zeigt die folgenden Felder an:

- **Austrittsdatum**
- **Ursache**

Das Banner für mögliche Arbeitskräfte zeigt die folgenden Felder an:

- **Titel**
- **Abteilung**
- **Positionstyp**
- **Vorgesetzter**
- **Startdatum**
- **Juristische Person**

Der Aktivitätsbereich auf der Arbeitskraftseite wurde neu organisiert, um weniger Optionen einzubeziehen. Informationen stehen nun in den folgenden Kategorien bereit: 

- Arbeit
- Person
- Verlassen
- Kompensation
- Leistungen
- Compliance

Zudem gibt es eine neue Registerkarte **Links** auf der Hauptarbeitskraftseite, die Benutzern einen zentralen Ort gibt, um auf alle zugehörigen Informationen für eine Arbeitskraft zuzugreifen.

Aufgrund dieser Änderungen erscheinen Informationen möglicherweise an einem anderen Speicherort, als Sie ihn verwendet haben. Beispielsweise werden Lohndaten, die zuvor im Feld Arbeitskraftformular angezeigt wurden, nun im Aktivitätsbereich unter **Kompensation > Lohn** in der Registerkarte **Persönliche Daten** angezeigt, wo es nun eine Schaltfläche **Weitere Informationen** gibt, um Felder auszublenden, auf die häufig zugegriffen wird.

[![Banner](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Arbeitshistorie

Die Registerkarte **Arbeitsverlauf** zeigt den Verlauf für alle juristischen Personen und ist für ausgetretene, aktive und mögliche Mitarbeiter und Auftragnehmer verfügbar. Sie können nun der Verlauf der Arbeit auf einmal für die juristische Personen anzeigen, auf die Sie Zugriff haben. Zudem können Sie Informationen für jeden der Arbeitsverlaufeinträge bearbeiten, ohne den Datenenkontext zu ändern. Sie können alle Informationen direkt auf der Seite aktualisieren. 

[![Arbeitshistorie](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Positionsverlauf

Die Registerkarte **Positionen** auf der Hauptarbeitskraftseite enthält eine Vollansicht aller Positionen, die innerhalb der Organisation durch Personal besetzt werden, mit ausgetretenen, aktuellen und künftigen Zuweisungen. Sie können direkt in den Positionsverlauf der Arbeitskraft im Aktivitätsbereich navigieren.

[![Positionen](./media/Worker-position-history.png)](./media/Worker-position-history.png)

