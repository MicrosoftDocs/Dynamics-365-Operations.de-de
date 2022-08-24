---
title: Neuigkeiten oder Änderungen in Dynamics 365 Supply Chain Management 10.0.25 (April, 2022)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.25 neu oder geändert wurden.
author: kamaybac
ms.date: 03/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 89036920cc8738e2948ec1a78aafc4b35fff87fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219093"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10025-april-2022"></a>Neuigkeiten oder Änderungen in Dynamics 365 Supply Chain Management 10.0.25 (April, 2022)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.25 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1149 und ist wie folgt verfügbar:

- **Vorschauversion des Release:** Februar 2022
- **Allgemeine Verfügbarkeit des Release (Selbstaktualisierung):** März 2022
- **Allgemeine Verfügbarkeit des Release (Selbstaktualisierung):** April 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir diesen Artikel, um Funktionen einzubeziehen, die es in den Build geschafft haben, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---|---|---|---|
| Bestand&nbsp;und&nbsp;Logistik | [Erweiterungen zu Gefahrengütern](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | Demnächst | Funktionsverwaltung:<br>*Erweiterungen zu Gefahrengütern* |
| Bestand&nbsp;und&nbsp;Logistik | [Verpackungsarbeit für Verpackungsstationen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | [Packarbeiten zum Packen von ausgehenden Containern und Verarbeiten von Sendungen](../warehousing/packing-work.md) | Funktionsverwaltung:<br>*Verpackungsarbeit für Verpackungsstationen* |
| Bestand&nbsp;und&nbsp;Logistik | [Barcodes im Lagerort mit GS1-Formatstandards scannen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-Barcodes und QR-Codes](../warehousing/gs1-barcodes.md) | Funktionsverwaltung:<br>*GS1-Barcodes scannen* |
| Fertigung | [Materialverbrauch und Reservierungen in der Produktionsausführungsoberfläche](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte](../production-control/production-floor-execution-use.md) | Funktionsverwaltung:<br>*Materialverbrauch in der Produktionsausführungsoberfläche (nicht WMS) registrieren*<br><br>Und/oder:<br><br>Funktionsverwaltung:<br>*(Vorschauversion) Materialverbrauch in der Produktionsausführungsoberfläche registrieren (WMS-fähig)* |
| Planung | [Von Planungsoptimierung zentralisierte Kalenderpflege](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-centralized-calendar-maintenance) | [Kalender und Produktprogrammplanung](../master-planning/supply-chain-calendars-master-planning.md) | Standardmäßig aktiviert |
| Planung | [Vorschläge für die Planungsoptimierung zur Optimierung des bestehenden Vorrats](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Aktivitätsmeldungen](../master-planning/action-messages.md) | Standardmäßig aktiviert |
| Planung | Geplante Aufträge vereinfacht | [Geplante Aufträge vereinfacht](../master-planning/planning-optimization/planned-orders-simplified.md ) | Funktionsverwaltung:<br>*Geplante Aufträge vereinfacht* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein‑ oder ausschalten möchten, müssen Sie dies in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Lager- und Lagerortverwaltung | (Polen) Verknüpfung mehrerer SAD-Rechnungen mit einer Bestellposition in einer SAD zulassen | Mit dieser Funktion können Sie Bestellzeilen aufteilen und mit einem einzigen administrativen Beleg (SAD) verknüpfen, wenn diese Bestellzeilen für mehrere verschiedene Rechnungen gebucht wurden (z.B. für verschiedene Sendungen). |
| Beschaffung | Mehrere Bestellanforderungen nach Buchhaltungsdatum in einer einzelnen Bestellung bündeln | Diese Funktion lässt zu, dass mehrere Bestellanforderungen in einer einzigen Bestellung konsolidiert werden, wenn die verschiedenen Bestellanforderungen unterschiedliche Buchungsdaten haben. Regeln für die Erstellung von Bestellungen und die Konsolidierung des Bedarfs können festgelegt werden, um die Entscheidung für die Gruppierung von Bestellanforderungszeilen nach Buchungsdatum auf der Ebene der Bestellung zu automatisieren. Die Konsolidierung von Bestellungen nach Buchungsdatum wird nicht unterstützt, wenn das Steuerelement Budget aktiviert ist, da das Buchungsdatum für Budgetreservierungen und -belastungen verwendet wird. Daher sollte sie während des Übergangs von der Bestellanforderung zur Bestellung beibehalten werden. |
| Beschaffung | Veraltete Standardfeldeinstellungen für die Antwort auf Angebotsanforderungen anzeigen | Diese Funktion führt die veralteten Standardeinstellungen für die Antwortfelder von Anfragen (RFQ) wieder ein, die zuvor aus der Benutzeroberfläche entfernt worden waren. Diese Einstellungen bieten keine Standardfunktionalität, können aber angepasst werden, um sie bei Bedarf bereitzustellen. Aktivieren Sie diese Funktion, wenn Ihr Unternehmen bereits Funktionen für die Standardeinstellungen des RFQ-Antwortfelds festgelegt hat oder dies plant. Wenn diese Funktion aktiviert ist, können Sie auf die Einstellungen zugreifen, indem Sie auf die Seite **Beschaffungs- und Bezugsquellenfindungsparameter** gehen, die Registerkarte **Angebotsanfrage** öffnen und **Standardantwortfelder für Angebotsanfragen** auswählen. |
| Beschaffung | Finanzdimensionen des Kreditors mit Finanzdimension der aktiven Dimensionsverknüpfung in der Bestellung zusammenführen | Mit dieser Funktion können Sie Finanzdimensionen von Kreditor mit aktiver Dimensionsverknüpfung Finanzdimensionen nach der Genehmigung einer Bestellanforderung zusammenführen, wenn Sie eine Verknüpfung zwischen einer Finanzdimension und der Bestandsdimension des Standorts festgelegt haben. Regeln für die Erstellung von Bestellungen und die Bedarfskonsolidierung können so festgelegt werden, dass die Entscheidung für die Zusammenführung von finanziellen Dimensionen von Kreditoren mit aktiver Dimensionsverknüpfung auf der Ebene des Bestellkopfes automatisiert wird. |
| Produktionssteuerung | (Russland) Aktivieren Sie die Einrichtung von Standardstandorten für Produktionsformel/Stückliste und automatische GTD-Reservierung/Verbrauch in der Produktion. | Die Funktion ermöglicht zusätzliche Optionen für die Produktion aus importierten Rohstoffen (nur russische Lokalisierung):<ul><li>Sie haben die Möglichkeit, den automatischen Standardort für Produktionsformeln und Stücklisten sowohl für Ressourcengruppen als auch für Lager festzulegen.</li><li>Automatische Reservierung von Rohstoffen nach der Dimension *GTD-Nummer* in WMS-aktivierten Lagern gemäß dem Nicht-WMS-Reservierungsalgorithmus. Dies gilt für Fälle, in denen eine Richtlinie für *Rohstoffkommissionierung* existiert, bei der **Arbeitserstellungsmethode** auf *Niemals* festgelegt ist und die Einrichtung des Lagers, des Standorts und der Artikelnummer mit den Bestandstransaktionen des Produktionsauftrags (Batch) übereinstimmt.</li><li>Automatischer Verbrauch von Rohstoffen nach der Dimension *GTD-Nummer* bei der Buchung der Kommissionierliste, entsprechend der zuvor beschriebenen erworbenen Reservierung.</li></ul> |
| Lagerortverwaltung | (Vorschauversion) Unterstützung von Skalierungseinheiten bei ein- und ausgehenden Lagerortaufträgen | Diese Funktion veranlasst das System, ausgehende Lagerbestellungen während der Freigabe an das Lager zu erstellen und eingehende Lageraufträge zu erstellen, wenn Umlagerungsaufträge als versandt gebucht werden. Das System synchronisiert dann jeden eingehenden oder ausgehenden Lagerauftrag mit der Scale-Unit, die für den Versand oder den Empfang des Auftrags zuständig ist. Beachten Sie, dass Sie nach der Aktivierung dieser Funktion Ihre Workloads für die Lagerausführung aktualisieren müssen. Weitere Informationen finden Sie unter [Arbeitsauslastungen in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Diese Funktion setzt die Funktion *Einlagerung von ASNs entkoppeln* voraus und ermöglicht die Funktionalität des Empfangs von Umlagerungsaufträgen über den Ladungsträger-Empfangsprozess in der Warehouse Management Mobile-App. |

## <a name="feature-state-changes-in-this-release"></a>Änderungen am Status der Funktionen in dieser Version

In der folgenden Tabelle sind Funktionen aufgeführt, die ab 10.0.25 obligatorisch oder standardmäßig aktiviert wurden. Alle diese Funktionen werden automatisch für Ihr System aktiviert, sobald Sie auf 10.0.25 aktualisieren. Obligatorische Funktionen können nicht ausgeschaltet werden, aber Funktionen, die standardmäßig aktiviert sind, können unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ausgeschaltet werden.

In der Tabelle sind auch Funktionen aufgeführt, die zuvor in der öffentlichen Vorschauversion enthalten waren, die aber in 10.0.25 allgemein verfügbar geworden sind, was bedeutet, dass sie jetzt für die Verwendung in Produktionsumgebungen empfohlen werden. Diese Funktionen sind, sofern nicht anders angegeben, standardmäßig deaktiviert. Sie müssen also die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um sie zu aktivieren, wenn Sie sie nutzen möchten.

| Modul | Funktionsname | Status der Funktion |
| --- | --- | --- |
| Anlagenverwaltung | [Regeln zur Gruppierung von Arbeitsaufträgen bei Ausführung eines Wartungsplans anwenden](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Allgemein verfügbar |
| Anlagenverwaltung | [Zählerbasierte Wartungsverbesserungen](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Allgemein verfügbar |
| Kostenverwaltung | [Kostenberechnungsstufe](../cost-management/cost-calculation-level.md) | Allgemein verfügbar |
| Kostenverwaltung | Benutzerdefinierte Chargennummereinstellungen für die Stornierung des Lagerabschlusses aktivieren | Allgemein verfügbar |
| Kostenverwaltung | [Fortschrittdetails zum Lagerabschluss](whats-new-scm-10-0-21.md) | Allgemein verfügbar |
| Kostenverwaltung | [Optionen der standardmäßigen Finanzdimensionen für die Lagerstandardkosten-Neubewertung](../cost-management/manage-standard-cost-updates.md) | Allgemein verfügbar |
| Kostenverwaltung | Lagerwertbericht zur Datenbereinigung | Standardmäßig aktiviert |
| Kostenverwaltung | [Lagerwert-Berichtsspeicher](../cost-management/inventory-value-report-storage.md) | Standardmäßig aktiviert |
| Kostenverwaltung | Lagerabschlussprotokoll im Raster anzeigen | Standardmäßig aktiviert |
| Verwaltung für technische Änderung | [Änderungsmanagement für vorhandene Produkte aktivieren](../engineering-change-management/change-management-existing-products.md) | Standardmäßig aktiviert |
| Verwaltung für technische Änderung | [Verwaltung für technische Änderung](../engineering-change-management/product-engineering-overview.md) | Standardmäßig aktiviert |
| Verwaltung für technische Änderung | [Technische Benachrichtigungen für die Produktion](../engineering-change-management/engineering-change-management.md) | Standardmäßig aktiviert |
| Verwaltung für technische Änderung | [Verbesserte Attributvererbung für Konstruktionsänderungsmanagement](../engineering-change-management/engineering-attributes-and-search.md) | Standardmäßig aktiviert |
| Verwaltung für technische Änderung | [Änderungen an Formeln und ihren Substanzen verwalten](../engineering-change-management/manage-formula-changes.md) | Standardmäßig aktiviert |
| Verwaltung für technische Änderung | [Produktbereitschaftsprüfungen](../engineering-change-management/product-readiness.md) | Standardmäßig aktiviert |
| Verwaltung für technische Änderung | [Variantengenerierung für technische Produkte](../engineering-change-management/engineering-variants.md) | Standardmäßig aktiviert |
| Lager- und Lagerortverwaltung | Navigation zur Stücklistenversion aus Stücklistenpositionen | Obligatorisch |
| Produktprogrammplanung | [Chargenfähige Umwandlung und Konsolidierung für geplante Sammel- und Verpackungschargenaufträge](whats-new-scm-10-0-20.md) | Allgemein verfügbar |
| Produktprogrammplanung | Ressourcenplanung mit Wartung | Allgemein verfügbar |
| Produktprogrammplanung | Funktionen für den Assistenten zur Einrichtung des Masterplans aktivieren | Obligatorisch |
| Produktprogrammplanung | [Prognosemodellauswahl auf der Seite mit den Informationen zur Bedarfsplanung](../master-planning/manual-adjustments-baseline-forecast.md) | Obligatorisch |
| Produktprogrammplanung | [Visualisierung des Produktprogrammplanfortschritts](../master-planning/tasks/monitor-master-planning-run.md) | Obligatorisch |
| Produktprogrammplanung | [Parallele Umwandlung von Auftragsvorschlägen](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisch |
| Produktprogrammplanung | [Umwandlung von Bestellvorschlägen mit Filtern](../master-planning/planning-optimization/planned-order-firming.md) | Standardmäßig aktiviert |
| Produktprogrammplanung | [Gespeicherte Ansichten für Bestellvorschläge](saved-views-scm.md) | Standardmäßig aktiviert |
| Beschaffung | Schaltfläche zum Zurücksetzen der Bestellanforderungsverteilung deaktivieren | Allgemein verfügbar |
| Beschaffung | [Zurücksetzen beschaffungsbezogener Workflows aktivieren](whats-new-scm-10-0-20.md) | Allgemein verfügbar |
| Beschaffung | Möglichkeit, angenommene Bestellungen aus der Kreditor-Kooperationen als Stapel zu bestätigen | Obligatorisch |
| Beschaffung | Kaufvertrag „Geschlossen“ | Obligatorisch |
| Beschaffung | Positionen zu Rechnungen für Bestellungen hinzufügen, die einem Kaufvertrag zugeordnet sind | Standardmäßig aktiviert |
| Beschaffung | Feld „Bestellte Menge“ zur Seite „Buchen des Produktzugangs“ hinzufügen | Standardmäßig aktiviert |
| Beschaffung | [Kreditoren erlauben, sich über Kreditorenzusammenarbeit für Beschaffungskategorien zu bewerben](../procurement/category-requests-from-vendors.md) | Standardmäßig aktiviert |
| Beschaffung | Stellt Von- und Bis-Beträge bei Bestellungen in Rechnung | Standardmäßig aktiviert |
| Beschaffung | Einstellungen für Gebühren mit Standort und Lagerort | Standardmäßig aktiviert |
| Beschaffung | Einkaufssteuerberechnung basierend auf dem Jahrestarif aktivieren | Standardmäßig aktiviert |
| Beschaffung | [Zuständige Partei für Kaufvertrag](../procurement/purchase-agreements.md) | Standardmäßig aktiviert |
| Beschaffung | [Gespeicherte Ansichten für Bestellungen](saved-views-scm.md) | Standardmäßig aktiviert |
| Produktinformationsverwaltung | [Strenge Überprüfung auf Standardauftragsmengen](../production-control/default-order-settings.md) | Obligatorisch |
| Produktinformationsverwaltung | Vorverarbeitung des Stücklistenberichts, um Zeitüberschreitungen zu vermeiden | Standardmäßig aktiviert |
| Produktinformationsverwaltung | Standardfinanzdimensionen separat bei Verwendung von Artikelvorlagen | Standardmäßig aktiviert |
| Produktinformationsverwaltung | Produktdimensionsgruppen für Artikelvorlagen aktivieren | Standardmäßig aktiviert |
| Produktinformationsverwaltung | Produktvariantennamen basierend auf der Bezeichnung neu generieren | Standardmäßig aktiviert |
| Produktinformationsverwaltung | [Verbesserungen an der Seite mit Variantenvorschlägen](../pim/tasks/create-predefined-product-variants.md) | Standardmäßig aktiviert |
| Produktionssteuerung | Verbesserte Artikelgewichtsmengenkommissionierung für die Produktion | Allgemein verfügbar |
| Produktionssteuerung | Eine neue Schaltfläche „Pause stoppen“ wurde zur Seite „Einzelvorgangskarten-Terminal“ hinzugefügt | Obligatorisch |
| Produktionssteuerung | [Aktivieren Sie die automatische Generierung der Kennzeichennummer, wenn die Berichtserstellung im Einzelvorgangskartengerät abgeschlossen wurde](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Produktionssteuerung | Ermöglicht den teilweisen Empfang von lohnbearbeiteten Artikeln und behebt ein Problem mit der Berechnung des Ausschusses für Stücklistenzeilen vom Typ Kreditor | Obligatorisch |
| Produktionssteuerung | [Funktion zum Sperren von Jobkartengerät und Jobkartenterminal, damit sie saniert werden können](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Produktionssteuerung | Verbesserungen der Dialogfelder „Genehmigen“ und „Einzelvorgänge übertragen“ | Obligatorisch |
| Produktionssteuerung | [Das Kennzeichen für Fertigmeldung wurde zum Einzelvorgangslistengerät hinzugefügt.](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Produktionssteuerung | [Beschriftung vom Einzelvorgangs-Kartengerät aus drucken](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Produktionssteuerung | [Produktionsumgebungsausführung](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Produktionssteuerung | [Anlagenverwaltungsfunktion für die Produktionsumgebungs-Ausführungsschnittstelle](../production-control/production-floor-execution-configure.md) | Standardmäßig aktiviert |
| Produktionssteuerung | [Einzelvorgangssuche für die Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) | Standardmäßig aktiviert |
| Produktionssteuerung | [Standardproduktionsreservierung überschreiben](../production-control/override-default-reservation-principle.md) | Standardmäßig aktiviert |
| Produktionssteuerung | [Vollständige Serien-, Chargen- und Kennzeichennummern in der Produktionsausführungsoberfläche anzeigen](whats-new-scm-10-0-21.md) | Standardmäßig aktiviert |
| Vertrieb und Marketing | [Auftragsdetails – Leistungsverbesserung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Allgemein verfügbar |
| Vertrieb und Marketing | Verkaufsangebotsdetails – Leistungsverbesserung | Allgemein verfügbar |
| Vertrieb und Marketing | Datenexportrichtlinie für referenzierten Auftrag | Obligatorisch |
| Vertrieb und Marketing | [Löschrichtlinie für Auftrag in Bestellposition](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Obligatorisch |
| Vertrieb und Marketing | [Datenexportrichtlinie für referenziertes Verkaufsangebot](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Obligatorisch |
| Vertrieb und Marketing | [Optimierung beim Export von Datenentitäten der Kontaktperson](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Standardmäßig aktiviert |
| Vertrieb und Marketing | Suche nach Feldern zur Einführung und zur Fertigstellung von Verkaufsangebotsdokumenten aktivieren | Standardmäßig aktiviert |
| Vertrieb und Marketing | [Berichtsleistung von „Top 100“-Kunden verbessern](whats-new-scm-10-0-23.md) | Standardmäßig aktiviert |
| Vertrieb und Marketing | Vorkalkulierten Debitorensaldo neu berechnen | Standardmäßig aktiviert |
| Vertrieb und Marketing | [Rückauftragspositionserfassung mit Dezimalstellen mit und ohne Artikelgewicht](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Standardmäßig aktiviert |
| Vertrieb und Marketing | [Gespeicherte Ansichten für Vertrieb und Marketing](saved-views-scm.md) | Standardmäßig aktiviert |
| Vertrieb und Marketing | Auftragsbestätigung mit nur einem Klick | Standardmäßig aktiviert |
| Lagerortverwaltung | [Crossdockingvorlagen mit Lagerplatzrichtlinien](../warehousing/planned-cross-docking.md) | Allgemein verfügbar |
| Lagerortverwaltung | [Erwartete Zugänge aus Qualitätsprüfungsaufträgen mit gesperrtem Beispielbestand deaktivieren](../inventory/inventory-blocking.md) | Allgemein verfügbar |
| Lagerortverwaltung | Kennzeichenempfangsverlauf | Allgemein verfügbar |
| Lagerortverwaltung | [Materialhandhabung Geräteschnittstelle](../warehousing/mhax.md) | Allgemein verfügbar |
| Lagerortverwaltung | [Mengen bei Freigabe an Lager auf nächste Verkaufseinheit abrunden](whats-new-scm-10-0-19.md) | Allgemein verfügbar |
| Lagerortverwaltung | Skalierungseinheitenunterstützung für Lagerort-App-Arbeitslisten | Allgemein verfügbar |
| Lagerortverwaltung | Lieferartdetails für Lieferungszyklus | Allgemein verfügbar |
| Lagerortverwaltung | [Schnellere API für das Schließen/erneute Öffnen von Containern auf Verpackungsstation verwenden](whats-new-scm-10-0-21.md) | Allgemein verfügbar |
| Lagerortverwaltung | [Für Wiederbeschaffungsaufträge ausgewählte Vorlagen überprüfen](whats-new-scm-10-0-20.md) | Allgemein verfügbar |
| Lagerortverwaltung | Wiederbeschaffungsvorlage erlauben, vorhandene sofortige Wiederbeschaffungsarbeit zu verwenden (einheitenübergreifend) | Obligatorisch |
| Lagerortverwaltung | Automatische Zuweisung der GUIDs bei der Erstellung von WHS-Benutzern | Obligatorisch |
| Lagerortverwaltung | Produktvarianten und Rückverfolgungsangaben in der Lagerhaltungs-App beim Artikelempfang aus Ladung erfassen | Obligatorisch |
| Lagerortverwaltung | [Bestandsstatus der Artikel ändern, die durch Rückverfolgungsangaben gesteuert werden](../inventory/inventory-statuses.md) | Obligatorisch |
| Lagerortverwaltung | [Arbeitspool für Arbeit ändern](../warehousing/change-work-pool-on-work.md) | Obligatorisch |
| Lagerortverwaltung | [Clusterposition voll](../warehousing/cluster-position-full.md) | Obligatorisch |
| Lagerortverwaltung | [Cluster-Einlagerungsfunktion](../warehousing/putaway-clusters.md) | Obligatorisch |
| Lagerortverwaltung | [Bestätigen und übertragen](../warehousing/confirm-and-transfer.md) | Obligatorisch |
| Lagerortverwaltung | [Ausgehende Lieferungen aus Batchaufträgen bestätigen](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Obligatorisch |
| Lagerortverwaltung | [Steuern, ob eine Empfangszusammenfassungsseite auf mobilen Geräten angezeigt wird](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligatorisch |
| Lagerortverwaltung | [Verzögerte Verarbeitung des manuellen Lagerbestandsumlagerungsvorgangs](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligatorisch |
| Lagerortverwaltung | Nicht zulassen, dass Ladungen erstellt werden, die nicht den Anforderungen der Vorlage für die Ladungserstellung von Wave entsprechen | Obligatorisch |
| Lagerortverwaltung | [Erweiterte Layouts für Kennzeichenbeschriftung](../warehousing/document-routing-layout-for-license-plates.md) | Obligatorisch |
| Lagerortverwaltung | [Alle Aktivitäten für Mehrfach-SKU-Lagerplatzrichtlinien auswerten](/troubleshoot/dynamics-365/supply-chain/warehousing/evaluate-multiple-location-directive-actions) | Obligatorisch |
| Lagerortverwaltung | Feld „Gesamtwert“ auf den Seiten „Alle Ladungen“ und „Ladungsdetails“ ausblenden | Obligatorisch |
| Lagerortverwaltung | Erstellungskonfiguration der Ladungsträgerbeschriftung | Obligatorisch |
| Lagerortverwaltung | Manuelle Korrektur der Ladungsposition für Administratoren oder ähnliche vertrauenswürdige Benutzer | Obligatorisch |
| Lagerortverwaltung | [Standortkennzeichenpositionierung](../warehousing/location-license-plate-positioning.md) | Obligatorisch |
| Lagerortverwaltung | [Lagerplatz-Produktdimensionsmischung](../warehousing/location-product-dimension-mixing.md) | Obligatorisch |
| Lagerortverwaltung | Feld „Lagerbestandsumlagerungsstatus“ des mobilen Geräts bearbeitbar machen | Obligatorisch |
| Lagerortverwaltung | Kommissionierdienst für manuelle Verkaufsposition für Administrator oder ähnliche vertrauenswürdige Benutzer | Obligatorisch |
| Lagerortverwaltung | [Verhindern, dass Kennzeichen für gelieferte Umlagerungsaufträge an anderen Lagerorten als dem Ziellagerort verwendet werden](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligatorisch |
| Lagerortverwaltung | Aufforderung zum Auflösen mehrdeutiger Namen für Lagerplatz/Kennzeichen | Obligatorisch |
| Lagerortverwaltung | [Qualitätsprüfung](../warehousing/quality-check.md) | Obligatorisch |
| Lagerortverwaltung | [Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App](../warehousing/install-configure-warehouse-management-app.md) | Obligatorisch |
| Lagerortverwaltung | [Zusätzliche Lagerplatzzone](../warehousing/additional-location-zones.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Umlagerungsaufträge aus der Lagerort-App erstellen und verarbeiten](../warehousing/create-transfer-order-from-warehouse-app.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | Schnelle Überprüfung für mobile Geräte am Lagerort aktivieren | Standardmäßig aktiviert |
| Lagerortverwaltung | [Maximale Ausführungszeit für den Einzelvorgang „Bereinigen der Lagerbestandseinträge für die Lagerortverwaltung“](../warehousing/onhand-cleanup.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Ausgehende Workloadvisualisierung](../warehousing/outbound-workload-visualization.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Lagerort-App-Ereignisse verarbeiten](../warehousing/warehouse-app-events.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Gespeicherte Ansicht für Ladungsplanungsworkbench](saved-views-scm.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Gespeicherte Ansicht für die Seite mit den Arbeitsdetails](saved-views-scm.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Gespeicherte Ansicht für die Zyklusverarbeitung](saved-views-scm.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Gespeicherte Ansichten für die Ladungsverarbeitung](saved-views-scm.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Gespeicherte Ansichten für die Lieferungsverarbeitung](saved-views-scm.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Zyklus-Batchauftragsdetails](../warehousing/wave-processing.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Wellenausführungsbenachrichtigungen](../warehousing/wave-execution-notifications.md) | Standardmäßig aktiviert |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattform-Updates für Finanz- und Betriebs-Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.25 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.25 der Finanz- und Betriebs-Apps (April 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.25 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868) an.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan](/dynamics365-release-plan/2022wave1/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

