---
title: Von der Planungsoptimierung nicht verwendete Parameter
description: In diesem Thema werden die Parameter aufgelistet, welche die Planungsoptimierung derzeit während des Betriebs nicht berücksichtigt.
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1992523ae10f30196ebe55d7c7fe6a2549a3a12853da261bd4a129523b8e4ea2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714282"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Von der Planungsoptimierung nicht verwendete Parameter

[!include [banner](../../includes/banner.md)]

In diesem Thema werden die Parameter aufgelistet, welche die Planungsoptimierung derzeit während des Betriebs nicht berücksichtigt. Der Planungsdienst kann einen Parameter überspringen, weil beispielsweise die zugehörige Funktionalität noch nicht unterstützt wird. Es kann auch sein, dass der Parameter aufgrund von Funktionsänderungen veraltet ist.

In den folgenden Abschnitten sind die Parameter aufgeführt, welche die Planungsoptimierung auf bestimmten Seiten nicht verwendet. Es wird auch erklärt, warum nicht jeder Parameter verwendet wird.

## <a name="master-planning-parameters-page"></a>Seite „Produktprogrammplanungsparameter“

Die Planungsoptimierung verwendet die folgenden Parameter oder Optionen auf der Seite **Produktprogrammplanungsparameter** nicht:

- Registerkarte **Allgemein**:

    - **Aktueller Absatzplan** – Unterstützung der *Planung* steht aus.
    - **Aktueller statischer Produktprogrammplan** – Unterstützung *Statischen in dynamischen Plan kopieren* steht aus.
    - **Aktueller dynamischer Produktprogrammplan** – Unterstützung *Statischen in dynamischen Plan kopieren* steht aus.
    - **Vollständigen und aktualisierten statischen Produktprogrammplan in den dynamischen Produktprogrammplan kopieren** – Unterstützung *Statischen in dynamischen Plan kopieren* steht aus.
    - **Startzeit für berechnete Verzögerungen** – Unterstützung für *berechnete Verzögerungen* steht aus.
    - **Dynamische negative Tage verwenden** – Planungsoptimierung verwendet immer den Ansatz mit *dynamischen negativen Tagen*.
    - **Kalender des heutigen Tages** – Unterstützung *Terminplanung* steht aus.
    - **Cacheverwendung** – Die Konfiguration des Microsoft Azure-Abonnement verarbeitet Leistungspunkte.
    - **Anzahl der Aufgaben im Hilfsaufgabenpaket** – Die Azure-Abonnementkonfiguration verarbeitet Leistungspunkte.
    - **Vorverarbeitung: Automatisch nach Artikeln mit direktem Bedarf filtern** – Die Azure-Abonnementkonfiguration verarbeitet Leistungspunkte.
    - **Nachbearbeitung: Automatisch nach Artikeln mit direktem Bedarf filtern** – Die Azure-Abonnementkonfiguration verarbeitet Leistungspunkte.
    - **Zahl der Produktionsaufträge im Anlagebündel** – Die Azure-Abonnementkonfiguration verarbeitet Leistungspunkte.
    - **Anzahl der Threads** – Die Azure-Abonnementkonfiguration verarbeitet Leistungspunkte.
    - **Zeitüberschreitung Planungsprozess in Minuten** – Die Azure-Abonnementkonfiguration verarbeitet Leistungspunkte.
    - **Startzeit planen** – Unterstützung *Terminplanung* steht aus.

- Registerkarte **Bestellvorschläge**:

    - **Zugangszeit** – Unterstützung *Terminplanung* steht aus.
    - **Produktion** – Unterstützung *Terminplanung* steht aus.
    - Felder im Abschnitt **Projekt** – Unterstützung *Terminplanung* steht aus.

- Registerkarte **Standardaktualisierung**:

    - **Markierung aktualisieren** – Unterstützung *Umwandeln* steht aus.
    - **Umwandlung bei Fehler abbrechen** – Unterstützung *Umwandeln* steht aus.
    - **Nach Kreditor gruppieren** – Unterstützung *Umwandeln* steht aus.
    - **Nach Einkäufergruppe gruppieren** – Unterstützung *Umwandeln* steht aus.
    - **Nach Kaufvertrag gruppieren** – Unterstützung *Umwandeln* steht aus.
    - **Nach Zeitraum gruppieren** – Unterstützung *Umwandeln* steht aus.
    - **Kaufvertrag finden** – Unterstützung *Umwandeln* steht aus.
    - **Nach Planungspriorität gruppieren** – Unterstützung *Umwandeln* steht aus.
    - **Nach Zeitraum gruppieren** – Unterstützung *Umwandeln* steht aus.

## <a name="coverage-groups-page"></a>Seite „Dispositionssteuerungsgruppen“

Die Planungsoptimierung verwendet die folgenden Parameter oder Optionen auf der Seite **Dispositionssteuerungsgruppen** nicht:

- **Allgemein**-Inforegister:

    - **Positive Tage** – Unterstützung *Positive Tage* steht aus.
    - **Verbrauch von Lagerbeständen** – Unterstützung *Verbrauch von Lagerbeständen* steht aus.
    - **Angegebene Stücklisten- oder Formelversion verwenden** – Unterstützung *Formelversionen mit Co-/Nebenprodukt* steht aus.
    - **Angegebenen Arbeitsplanversion verwenden** – Unterstützung *Bedarf mit bestimmten definierten Stücklisten- oder Arbeitsplananforderungen* steht aus.

- Inforegister **Aktivität**:

    - **Aktivitätsmeldung** – Unterstützung *Aktivitäten* steht aus.
    - **Aktivitätsplanungszeitraum** – Unterstützung *Aktivitäten* steht aus.
    - **Verschiebungsgrenze** – Unterstützung *Aktivitäten* steht aus.
    - **Vorverlegungsgrenze** – Unterstützung *Aktivitäten* steht aus.
    - **Basisdatum** – Unterstützung *Aktivitäten* steht aus.
    - **Termin vorziehen** – Unterstützung *Aktivitäten* steht aus.
    - **Termin verschieben** – Unterstützung *Aktivitäten* steht aus.
    - **Menge reduzieren** – Unterstützung *Aktivitäten* steht aus.
    - **Menge erhöhen** – Unterstützung *Aktivitäten* steht aus.
    - **Abgeleitete Aktivitäten** – Unterstützung *Aktivitäten* steht aus.

- Inforegister **Sonstige**:

    - **Nichtplanungszeitraum (Tage)** – Unterstützung für *Nichtplanungszeitraum* ist in der Planungsoptimierung nicht vorgesehen.
    - **Planungszeitraum Stücklistenauflösung (Tage)** – Unterstützung *Terminplanung* steht aus.
    - **Kapazitätsplanungszeitraum (Tage)** – Unterstützung *Terminplanung* steht aus.
    - **Planungszeitraum genehmigte Anforderungen (Tage)** – Unterstützung *Anforderung* steht aus.
    - **Zeitraum für Absatzplanung** – Unterstützung der *Planung* steht aus.

- Inforegister **Verzögerungen**:

    - **Berechnete Verzögerungen** – Unterstützung für *berechnete Verzögerungen* steht aus.
    - **Planungszeitraum für berechnete Verzögerungen (Tage)** – Unterstützung für *berechnete Verzögerungen* steht aus.

## <a name="item-coverage-page"></a>Seite „Artikelabdeckung“

Die Planungsoptimierung verwendet die folgenden Parameter oder Optionen auf der Seite **Artikelabdeckung** nicht:

- Registerkarte **Allgemein**:

    - **Typ des Bestellvorschlags** – die Planungsoptimierung unterstützt die Option *Kanban* nicht, Unterstützung *Kanban* steht aus.
    - **Nichtplanungszeitraum (Tage)** – Unterstützung für *Nichtplanungszeitraum* ist in der Planungsoptimierung nicht vorgesehen.
    - **Planungszeitraum Stücklistenauflösung (Tage)** – Unterstützung *Terminplanung* steht aus.
    - **Kapazitätsplanungszeitraum (Tage)** – Unterstützung *Terminplanung* steht aus.
    - **Planungszeitraum genehmigte Anforderungen (Tage)** – Unterstützung *Anforderung* steht aus.
    - **Mindestbestand auffüllen** – die Planungsoptimierung unterstützt die Optionen *Heutiges Datum*, *Erster Abgang* und *Planungszeitraum* nicht. Sie verwendet immer die Option *Heutiges Datum + Beschaffungszeit*.
    - **Mindestzeitraum** – Unterstützung *Mindestlagerbestand* steht aus.
    - **Planungsformel** – Unterstützung *Formelversionen mit Co-/Nebenprodukten* steht aus.
    - **Standardpriorität** – Unterstützung *Formelversionen mit Co-/Nebenprodukten* steht aus.
    - **Aktuelle Priorität** – Unterstützung *Formelversionen mit Co-/Nebenprodukten* steht aus.
    - **Änderungsdatum** – Unterstützung *Formelversionen mit Co-/Nebenprodukten* steht aus.
    - **Verbrauch von Lagerbeständen** – Unterstützung *Verbrauch von Lagerbeständen* steht aus.

## <a name="master-plans-page"></a>Seite „Produktprogrammpläne“

Die Planungsoptimierung verwendet die folgenden Parameter oder Optionen auf der Seite **Produktprogrammpläne** nicht:

- **Allgemein**-Inforegister:

    - **Verfügbaren Lagerbestand einbeziehen** – Unterstützung *Verbrauch von Lagerbeständen* steht aus.
    - **Verfügbaren Lagerbestand überschreiben** – Unterstützung *Verbrauch von Lagerbeständen* steht aus.
    - **Verbrauch von Lagerbeständen** – Unterstützung *Verbrauch von Lagerbeständen* steht aus.
    - **Lagerbuchungen einbeziehen** – Unterstützung *Verbrauch von Lagerbeständen* steht aus.
    - **Verkaufsangebote einbeziehen** – Unterstützung *Verkaufsangebote* steht aus.
    - **Angebotsanforderungen einbeziehen** – Unterstützung *Angebotsanforderungen* steht aus.
    - **Haltbarkeitsdaten verwenden** – Unterstützung *Haltbarkeitsdatum* steht aus.
    - **Anschlussplan einbeziehen** – Unterstützung *Anschlussplanung* steht aus.
    - **Planungsmethode** – Unterstützung *Terminplanung* steht aus.
    - **Begrenzte Eigenschaft** – Unterstützung *Terminplanung* steht aus.
    - **Rückwärtsplanung des Kapazitätsplanungszeitraums (Tage)** – Unterstützung *Terminplanung* steht aus.
    - **Begrenzte Kapazität** – Unterstützung *Terminplanung* steht aus.
    - **Planungszeitraum für begrenzte Kapazität** – Unterstützung *Terminplanung* steht aus.
    - **Begrenzte Kapazität für Engpassressourcen** – Unterstützung *Terminplanung* steht aus.
    - **Kapazitätsplanungszeitraum für Engpassressourcen** – Unterstützung *Terminplanung* steht aus.
    - **Bestellvorgänge** – Die Planungsoptimierung verwendet feste Nummernkreise.
    - **Sitzung** – Die Planungsoptimierung verwendet feste Nummernkreise.
    - **Anschlussplan** – Die Planungsoptimierung verwendet feste Nummernkreise.

- Inforegister **Planungszeitraum in Tagen**:

    - **Nichtplanungszeitraum** – Unterstützung für *Nichtplanungszeitraum* ist in der Planungsoptimierung nicht vorgesehen.
    - **Auflösung** – Unterstützung *Terminplanung* steht aus.
    - **Zeitraum für Absatzplanung** – zusätzliche Unterstützung der *Planung* steht aus.
    - **Kapazität** – Unterstützung *Terminplanung* steht aus.
    - **Anschlussplan** – Unterstützung *Anschlussplanung* steht aus.
    - **Aktivitätsmeldung** – Unterstützung *Aktivitäten* steht aus.
    - **Berechnete Verzögerungen** – zusätzliche Unterstützung für *berechnete Verzögerungen* steht aus.
    - **Abfolge** – Unterstützung *Produktion* steht aus.

- Inforegister **Berechnete Verzögerungen**:

    - **Sicherstellen, dass geplante Bestellung nicht vor dem Ausführungsdatum des Produktprogrammplans erstellt werden** – Unterstützung für *Berechnete Verzögerungen* steht aus.
    - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplante Einkaufsbestellungen**) – Unterstützung *Berechnete Verzögerungen* steht aus.
    - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplante Produktionsauftrag**) – Unterstützung *Berechnete Verzögerungen* steht aus.
    - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplante Umlagerung**) – Unterstützung *Berechnete Verzögerungen* steht aus.
    - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplanter Kanban**) – Unterstützung *Berechnete Verzögerungen* steht aus.

- Inforegister **Abfolge**:

    - **Sequenzierte Bestellvorschläge nach Produktprogrammplanung** – Unterstützung *Abfolge* steht aus.
    - **Zeitraumtyp** – Unterstützung *Abfolge* steht aus.
    - **Periodentyp** – Unterstützung *Abfolge* steht aus.
    - **Anzahl der Buckets im Kampagnenzyklus** – Unterstützung *Abfolge* steht aus.

## <a name="released-product-details-page"></a>Seite für freigegebene Produkte

Die Planungsoptimierung verwendet die folgenden Parameteroption auf der Seite **Details für freigegebene Produkte** nicht:

- Inforegister **Entwickler**:

    - **Produktionstyp** – Die Planungsoptimierung unterstützt die Option *Planungselement* nicht, Unterstützung *Planungselemente* ausstehend.

## <a name="default-order-settings-page"></a>Seite „Standardauftragseinstellungen“

Die Planungsoptimierung verwendet die folgenden Parameteroption auf der Seite **Standardauftragseinstellungen** nicht:

- Inforegister **Bestand**:

    - **Lieferdatumskontrolle** – Die Planungsoptimierung unterstützt die Option *CTP* nicht, Unterstützung *CTP* steht aus.

## <a name="working-time-calendars-page"></a>Seite „Arbeitszeitkalender“

Die Planungsoptimierung verwendet den folgenden Parameter auf der Seite **Arbeitszeitkalender** nicht:

- **Basiskalender** – Unterstützung *Basiskalender* steht aus.

## <a name="batch-disposition-master-page"></a>Seite „Chargendisposition Einstellungen“

Die Planungsoptimierung verwendet den folgenden Parameter auf der Seite **Chargendisposition Einstellungen** nicht:

- Inforegister **Einrichten**:

    - **Dispositionscode einbezogen** – Unterstützung *Chargendispositionscodes* steht aus.
