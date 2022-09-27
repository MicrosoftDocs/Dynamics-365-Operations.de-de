---
title: In der Planungsoptimierung nicht verwendete Parameter
description: In diesem Artikel werden die Parameter aufgelistet, welche die Planungsoptimierung derzeit während des Betriebs nicht berücksichtigt.
author: t-benebo
ms.date: 09/02/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6c7469692aac24a5ae554973325a128c787363ba
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542279"
---
# <a name="parameters-not-used-by-planning-optimization"></a>In der Planungsoptimierung nicht verwendete Parameter

[!include [banner](../../includes/banner.md)]

In diesem Artikel werden die Parameter aufgelistet, welche die Planungsoptimierung derzeit während des Betriebs nicht berücksichtigt. Der Planungsdienst kann einen Parameter überspringen, weil beispielsweise die zugehörige Funktionalität noch nicht unterstützt wird. Es kann auch sein, dass der Parameter aufgrund von Funktionsänderungen veraltet ist.

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

## <a name="coverage-groups-page"></a>Seite „Dispositionssteuerungsgruppen“

Die Planungsoptimierung verwendet die folgenden Parameter oder Optionen auf der Seite **Dispositionssteuerungsgruppen** nicht:

- **Allgemein**-Inforegister:

  - **Positive Tage** – Der Wert *Positive Tage* wird nicht verwendet. Bei der Planungsoptimierung gelten positive Tage als unendlich.
  - **Verbrauch von Lagerbeständen** – Unterstützung *Verbrauch von Lagerbeständen* steht aus.
  - **Angegebene Stücklisten- oder Formelversion verwenden** – Unterstützung *Formelversionen mit Co-/Nebenprodukt* steht aus.
  - **Angegebenen Arbeitsplanversion verwenden** – Unterstützung *Bedarf mit bestimmten definierten Stücklisten- oder Arbeitsplananforderungen* steht aus.


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

- **Vorlaufzeit**-Registerkarte:

  - **Kaufzeit** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.
  - **Produktionszeit** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.
  - **Übertragungszeit** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.
  - **Arbeitstage** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.

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
  - **Berechnete Verzögerungen** – zusätzliche Unterstützung für *berechnete Verzögerungen* steht aus.
  - **Abfolge** – Unterstützung *Produktion* steht aus.

- Inforegister **Berechnete Verzögerungen**:

  - **Sicherstellen, dass geplante Bestellung nicht vor dem Ausführungsdatum des Produktprogrammplans erstellt werden** – Unterstützung für *Berechnete Verzögerungen* steht aus.
  - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplante Einkaufsbestellungen**) – Unterstützung *Berechnete Verzögerungen* steht aus.
  - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplante Produktionsauftrag**) – Unterstützung *Berechnete Verzögerungen* steht aus.
  - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplante Umlagerung**) – Unterstützung *Berechnete Verzögerungen* steht aus.
  - **Die berechnete Verzögerung zum Bedarfsdatum hinzufügen** (im Abschnitt **Geplanter Kanban**) – Unterstützung *Berechnete Verzögerungen* steht aus.

- **Aktionsnachricht** Inforegister:

  - **Aktualisierung des verschobenen Datums als Bedarfstermin** - Dieser Parameter wird bei der Planungsoptimierung nicht mehr verwendet.

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

- **Bestellung**-Inforegister:

  - **Kaufvorlaufzeit** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.
  - **Arbeitstage** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.

- Inforegister **Bestand**:

  - **Lieferdatumskontrolle** – Die Planungsoptimierung unterstützt die Option *CTP* nicht, Unterstützung *CTP* steht aus.
  - **Inventarvorlaufzeit** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.
  - **Arbeitstage** – In Versionen des Planungsoptimierungsdienstes, die älter als die Version vom 6. August 2021 sind, verwendet Planungsoptimierung diesen Parameter, um die korrekten Bestell- und Liefertermine zu berechnen, speichert jedoch nicht die berechnete Vorlaufzeit selbst im Planauftrag. In späteren Versionen verwendet der Dienst auch die berechnete Vorlaufzeit, um das **Vorlaufzeit**-Feld und die **Arbeitstage**-Option nach Bedarf für den jeweiligen Planauftrag festzulegen.

## <a name="batch-disposition-master-page"></a>Seite „Chargendisposition Einstellungen“

Die Planungsoptimierung verwendet den folgenden Parameter auf der Seite **Chargendisposition Einstellungen** nicht:

- Inforegister **Einrichten**:

  - **Dispositionscode einbezogen** – Unterstützung *Chargendispositionscodes* steht aus.
 
<!-- KFM: Now available? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> 