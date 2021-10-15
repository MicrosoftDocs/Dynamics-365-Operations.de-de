---
title: Arbeitsbereich für Vorteilsverwaltung
description: Dieses Thema beschreibt den Arbeitsbereich Vergütungsverwaltung in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6cc1432e108c74706dea124a62024272e65b6c1
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512473"
---
# <a name="benefits-management-workspace"></a>Arbeitsbereich für Vorteilsverwaltung

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Dieses Thema beschreibt den Arbeitsbereich **Vergütungsverwaltung** in Dynamics 365 Human Resources.

> [!NOTE]
> Um den Arbeitsbereich **Vergütungsverwaltung** anzuzeigen, müssen Sie zuerst die Funktion **(Vorschau) Arbeitsbereich Vergütungsverwaltung** in der Funktionsverwaltung aktivieren. Weitere Informationen zur Aktivierung der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).<br><br>![Arbeitsbereich für Vorteilsverwaltung aktivieren.](./media/hr-benefits-management-workspace-enable.png)

Der Arbeitsbereich **Vergütungsverwaltung** gibt Ihnen einen schnellen Überblick über die Artikel, die Ihre Aufmerksamkeit erfordern. Auf dieser Seite können Sie sehen:

- Summen für Artikel, die auf eine Aktion warten
- Arbeitskräfte mit unbestätigten Auswahlen
- Arbeitskräfte, die sich kürzlich für Leistungen angemeldet haben
- Arbeitskräfte mit zukünftigen Lebensereignissen
- Neu eingestellte Mitarbeiter, die nicht angemeldet sind
- Arbeitskräfte mit aktiven Lebensereignissen
- Arbeitskräfte mit offenen Anmeldungen, die sich nicht für einen Plan entschieden haben

![Arbeitsbereich „Vorteilsverwaltung“.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Anzeigen von Aktionsartikeln

Sie können Ihre Aktionsartikel anzeigen, indem Sie entweder eine Kachel oder eine Registerkarte auswählen. Wenn Sie eine Registerkarte auswählen, können Sie Arbeitskräfte auf der Seite des Arbeitsbereichs anzeigen und auswählen.

![Aktionsartikel.](./media/hr-benefits-management-workspace-action-items.png)

Wenn Sie eine Kachel auswählen, gelangen Sie auf die Seite für diesen Bereich. Wenn Sie z. B. eine dieser Kacheln auswählen, wird die Seite **Vorteile für Arbeitskräfte** angezeigt, gefiltert nach Mitarbeitern, für die Sie Maßnahmen ergreifen müssen:

- **Nicht bestätigte Auswahl**
- **Registrierungen ohne ausgecheckte Pläne öffnen**
- **Für Vorteile registriert**
- **Neuer Mitarbeiter nicht registriert**

![Vergütungspläne für Arbeitskräfte.](./media/hr-benefits-management-workspace-plans.png)

Durch Auswahl der Kacheln **Aktive Lebensereignisse** oder **Zukünftige Lebensereignisse** gelangen Sie zu einer Liste aktiver oder künftiger Lebensereignisse.

![Lebensereignisse.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Bearbeitung

Um die Einschreibeberechtigung, Lebensereignisse oder Aktualisierungen von Sätzen zu bearbeiten, wählen Sie den entsprechenden Artikel in der Navigationsleiste.

![Bearbeitung.](./media/hr-benefits-management-workspace-processing.png)

Um die Bearbeitungsergebnisse anzuzeigen, wählen Sie **Bearbeitungsergebnisse** auf der Seite.

![Prozessergebnisse.](./media/hr-benefits-management-workspace-process-results.png)

Weitere Informationen zur Bearbeitung von Leistungen finden Sie unter:

- [Vergütungsberechtigung verarbeiten](hr-benefits-process-enrollment-eligibility.md)
- [Änderungen von Lebensereignissen verarbeiten](hr-benefits-process-life-event-changes.md)
- [Lebensereignisberechtigung verarbeiten](hr-benefits-process-life-event-eligibility.md)
- [Lebensereignisse verarbeiten](hr-benefits-process-life-events.md)
- [Satzänderungen verarbeiten](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Periode ändern

Um einen anderen Leistungszeitraum anzuzeigen, wählen Sie ihn aus der Dropdownliste **Periode**.

![Periode ändern.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Registerkarte „Registrierung“ öffnen

Sie können Aktionsartikel anzeigen, indem Sie entweder eine Kachel oder eine Registerkarte auswählen. Wenn Sie eine Registerkarte auswählen, können Sie Arbeitskräfte auf der Seite des Arbeitsbereichs anzeigen und auswählen.
Die Registerkarte **Registrierung öffnen** bietet wichtige Metriken für den offenen Registrierungsprozess. 

Informationen zur offenen Registrierung werden 30 Tage vor dem **Startdatum für Registrierung** angezeigt. Dies ist in der **Perioden**-Einrichtung unter **Leistungsmanagement** > **Links** > **Perioden** im Feld **Startdatum der Registrierung** definiert.  Wechseln Sie zum Ändern dieser Einstellung zu **Human Resources-Parameter konfigurieren** > **Leistungsmanagement** > **Optionen für die offene Registrierung**, und aktualisieren Sie das Feld **Anzahl**.  

Die folgenden Informationen finden Sie auf der Registerkarte **Registrierung öffnen**:
 - Mitarbeiter, die den offenen Registrierungsprozess noch nicht begonnen haben
 - Mitarbeiter, deren Wahl sich in Bearbeitung befindet
 - Mitarbeiter, die den Wahlprozess abgeschlossen haben
 - Nicht bestätigte Auswahl

**Zusammenfassungskacheln**

- **Nicht gestartet** – Die Kachel **Nicht gestartet** zeigt die Anzahl der Mitarbeiter an, die den Registrierungsprozess nicht gestartet haben. Die Kachel **Nicht gestartet** ist eine gefilterte Liste, die nur die Mitarbeiter anzeigt, für die für den Zeitraum des offenen Registrierungsplans keine Pläne ausgewählt, erlassen oder ausgecheckt wurden. Obligatorische Pläne werden ignoriert und nicht berücksichtigt, da sie standardmäßig für den Mitarbeiter ausgewählt sind.  Sie können auf dieser Kachel einen Drillback durchführen, um eine Liste der Mitarbeiter anzuzeigen, die den offenen Registrierungsprozess auf der Seite **Leistungsplan für Arbeitnehmer** noch nicht gestartet haben.

  > [!NOTE]
  > Wenn Sie den Fortschritt der offenen Registrierung für einen **Plantyp** nicht verfolgen möchten, Sie können ihn ausschließen, indem Sie zu **Vergütungsverwaltung** > **Links** > **Mitarbeiter-Self-Service-Parameter** > **Vorteilsplan-Kachel einrichten** wechseln und das Feld **Fortschritt der offenen Registrierung verfolgen** aktualisieren.  Sie haben beispielsweise Pläne erstellt, für die Folgendes gilt: **Plantyp** = **Sonstiges**. Bei diesen Plänen kann es sich um optionale Pläne handeln, für die Sie den Registrierungsfortschritt nicht verfolgen möchten. Wenn Sie diesen Plantyp nicht auswählen, werden Pläne dieser Typen beim Verfolgen des Registrierungsfortschritts oder -Abschlusses auf der Registerkarte **Registrierung öffnen** ignoriert. Diese Einstellung gilt für den Plantyp, der für alle Perioden und juristischen Personen ausgewählt wird.

- **In Bearbeitung** – Die Kachel **In Bearbeitung** zeigt die Anzahl der Mitarbeiter mit in Bearbeitung befindlichen Wahlen an. Die Kachel **In Bearbeitung** ist eine gefilterte Liste, die nur Mitarbeiter anzeigt, für die mindestens ein Plan aufgehoben oder ausgewählt wurde. Obligatorische Pläne werden ignoriert und nicht berücksichtigt, da sie standardmäßig für den Mitarbeiter ausgewählt sind. Sie können von dieser Kachel aus einen Drillback ausführen, um die ausgewählten und aufgegebenen Pläne auf der Seite **Massenaktualisierung für Arbeitnehmerleistungspläne** anzuzeigen.

- **Eingeschriebene Leistungen** – Die Kachel **Für Vergütungen registriert** gibt die Anzahl der Mitarbeiter an, die vollständig für Vergütungen sind. Die Kachel **Für Vergütungen registriert** ist eine gefilterte Liste, die Mitarbeiter an, die alle Pläne ausgewählt oder aufgehoben haben. Die Abfrage schließt Pläne aus, die nicht für die offene Registrierung auf der Seite **Mitarbeiter-Self-Service-Parameter** verfolgt werden. Sie können von dieser Kachel aus einen Drillback ausführen, um eine Liste der Mitarbeiter auf der Seite **Vergütungspläne für Arbeitskräfte** anzuzeigen.

- **Unbestätigte Auswahl** – Die Kachel **Unbestätigte Auswahl** zeigt die Anzahl der Mitarbeiter mit ausgewählten oder aufgehobenen Plänen, die bestätigt werden müssen. Sie können von dieser Kachel aus einen Drillback ausführen, um die Seite **Massenaktualisierung für Arbeitnehmerleistungspläne** anzuzeigen.

**Aktivität**

- **Nicht gestartet** – Die Registerkarte **Nicht gestartet** zeigt eine Liste der Mitarbeiter an, die den Registrierungsprozess nicht gestartet haben. Die Kachel **Nicht gestartet** ist eine gefilterte Liste, die die Mitarbeiter anzeigt, für die für den Zeitraum des offenen Registrierungsplans keine Pläne ausgewählt, erlassen oder ausgecheckt wurden. Obligatorische Pläne werden ignoriert und nicht berücksichtigt, da sie standardmäßig für den Mitarbeiter ausgewählt sind. Sie können einen Drilldown zur Arbeitskraft durchführen, um die Seite **Vergütungsplandetail für Arbeitskräfte**.

- **Wahlen in Bearbeitung** – Die Registerkarte **Wahlen in Bearbeitung** zeigt eine Liste der Mitarbeiter mit in Bearbeitung befindlichen Wahlen an. **Wahlen in Bearbeitung** ist eine gefilterte Liste, die Mitarbeiter anzeigt, für die mindestens ein Plan aufgehoben oder ausgewählt wurde. Obligatorische Pläne werden ignoriert und nicht berücksichtigt, da sie standardmäßig für den Mitarbeiter ausgewählt sind. Sie können einen Drilldown zur Arbeitskraft durchführen, um die Seite **Vergütungsplandetail für Arbeitskräfte**.

## <a name="view-more-options"></a>Weitere Optionen anzeigen

Wählen Sie **Links** aus, um weitere Informationen und Aktionen anzuzeigen.

![Verknüpfungen.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Siehe auch

[Vorteilsverwaltung – Übersicht](hr-benefits-management-overview.md)
