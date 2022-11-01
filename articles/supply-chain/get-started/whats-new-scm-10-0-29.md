---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.29. (Oktober 2022)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.29 neu oder geändert wurden.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d12932f35b3b451577d38948f60bc3a73c10e2a0
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714832"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.29. (Oktober 2022)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.29 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1326 und ist im folgenden Zeitplan verfügbar:

- **Vorschauversion für Release:** August 2022
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** September 2022
- **Allgemeine Verfügbarkeit des Release (automatisches Update):** Oktober 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Artikels, um Funktionen einzubeziehen, die zum Build hinzugefügt wurden, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---|---|---|---|
| Bestand und Logistik | [Zuordnen und Reservierung für WMS-Artikel in Inventory Visibility](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Bald verfügbar | Standardmäßig aktiviert |
| Bestand und Logistik | [Laden Sie optimierte Bestandslisten vorab](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Die Inventory Visibility-App verwenden](../inventory/inventory-visibility-power-platform.md) | Aktiviert durch Servicekonfiguration |
| Automatisierung der Lieferungen zur Auftragsfertigung | [Automatisierung der Lieferungen zur Auftragsfertigung](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Automatisierung der Lieferungen zur Auftragsfertigung](../master-planning/make-to-order-supply-automation.md) | Funktionsverwaltung:<br>*Automatisierung der Lieferungen zur Auftragsfertigung* |
| Planung | [Zeigen Sie detaillierte Einblicke für DDMRP an und wenden Sie sie an](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Bedarfsgesteuerte Planung im Überblick](../master-planning/planning-optimization/ddmrp-overview.md) | Funktionsverwaltung:<br>*(Vorschauversion) DDMRP für Planungsoptimierung* |
| Produktionssteuerung | [Markieren Sie fertige Waren vor der Buchung in Erfassungen als physisch verfügbar.](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Markieren Sie fertige Waren vor der Buchung in Erfassungen als physisch verfügbar.](../production-control/deferred-posting.md) | Funktionsverwaltung:<br>*(Vorschauversion) Markieren Sie fertige Waren vor der Buchung in Erfassungen als physisch verfügbar.* |
| Lagerortverwaltung | [Suchen Sie relevante Daten in der Warehouse Mobile App](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Daten mit den Umleitungen der mobilen Warehouse Management-App abfragen](../warehousing/warehouse-app-data-inquiry.md) | Funktionsverwaltung:<br>*Datenabfrage-Flow in der Warehouse Management-App* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein‑ oder ausschalten möchten, müssen Sie dies in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Kostenverwaltung | Optimierung der ausstehenden Preiskalkulierung für das Co-Produkt | Diese Funktion behebt einen Konflikt, der manchmal auftreten kann, wenn Nebenproduktpreise mithilfe mehrerer Threads berechnet werden. Dadurch sorgt das System dafür, dass jeder Kuppelproduktpreis nur einmal berechnet wird. Das Ergebnis dieser Berechnung wird dann als Eingabe für alle anderen Berechnungen verwendet. Wenn bereits ein ausstehender Preis vorhanden ist, wird dieser Preis verwendet. |
| Produktprogrammplanung | Gruppenbuchungen in Planungsoptimierung | Diese Funktion kann dazu beitragen, die Anzahl der Bestellvorschläge zu reduzieren, die generiert werden, um eine einzelne Verkaufsauftragsposition zu beliefern, wenn Sie die Planungsoptimierung verwenden. Wenn diese Funktion aktiviert ist, gruppiert Planning Optimization alle Bestandstransaktionen für eine Auftragsposition in einer einzigen Anforderung für die vollständige Menge. (Dieses Verhalten stimmt mit dem Verhalten des integrierten Planungsmoduls überein.) Angebot und Nachfrage werden separat gruppiert. Daher trägt die Funktion dazu bei, das Transaktionsvolumen zu reduzieren, wenn Sie Transaktionen aufgeteilt haben und wenn Sie Dimensionen (z. B. Chargennummern oder Seriennummern) verwenden, die keine Deckungsdimensionen sind. |
| Beschaffung | Lieferant für Bestellungen sperren | Mit dieser Funktion können Sie einen Lieferanten für Bestellungen zurückstellen. Es fügt einen neuen Sperrtyp *Bestellung* hinzu, der einen Kreditor für Bestellungen als gesperrt markiert. Sie können keine neuen Bestellungen für Lieferanten erstellen, die für Bestellungen zurückgestellt wurden, aber Sie können weiterhin mit allen offenen Rechnungen oder Zahlungen für diese Lieferanten fortfahren. |
| Vertrieb und Marketing | Positionsnettobetrag beim Importieren berechnen | Mit dieser Funktion können Sie steuern, ob das System Zeilensummen neu berechnen soll, wenn Sie Daten über *Verkaufsauftragszeilen*, *Verkaufsangebotspositionen* oder *Retourenauftragspositionen* Entität mit OData oder Dual-Write importieren. Es wirkt sich nur dann aus, wenn Sie auch über Bewertungsrichtlinien für Handelsabkommen verfügen, die Änderungen am Feld **Netto-Betrag** für VK-Auftragspositionen, VK-Angebotspositionen und/oder Rücklieferungspositionen einschränken. Es fügt eine Einstellung namens **Zeilennettobetrag berechnen** zur Seite **Debitorenbuchhaltung > Setup > Debitorenparameter** hinzu. Wenn diese Einstellung auf *Ja* eingestellt ist, berechnet das System die Positionsbeträge bei Bedarf immer neu (wodurch jegliche Bewertungsrichtlinie für Handelsabkommen für den Nettobetrag der Position ignoriert wird). Wenn die Einstellung auf *Nein* eingestellt ist, wird das System niemals automatisch den Nettobetrag der Position berechnen, selbst wenn eingehende Änderungen des Positionspreises, der Menge und/oder des Rabatts bedeuten würden, dass der Nettobetrag der Position neu berechnet werden müsste. Diese Funktion ist standardmäßig aktiviert und legt **Zeilennettobetrag berechnen** auf *Ja* fest. Die Einstellungen *Nein* entspricht dem Systemverhalten vor Version 10.0.23 und wird hauptsächlich bereitgestellt, um Legacy-Integrationsszenarien zu unterstützen.<br><br>Weitere Informationen finden Sie unter [Berechnen Sie die Zeilennettobeträge neu, wenn Sie Verkaufsaufträge, Angebote und Retouren importieren](../sales-marketing/calc-line-net-amounts-import.md). |
| Vertrieb und Marketing | Verkaufssummen mithilfe mehrerer Threads berechnen | Diese Funktion hilft, die Leistung zu verbessern, indem sie es dem System ermöglicht, die Parallelverarbeitung zu verwenden, wenn es Verkaufssummen in einem Stapel berechnet. Die Funktion fügt ein neues Feld **Anzahl der Themen** zum Dialogfeld **Berechnen Sie die Verkaufssummen** hinzu. Wenn Sie die Berechnung in einem Stapel ausführen möchten, können Sie dieses Feld verwenden, um die maximale Anzahl von Threads festzulegen. Wenn Sie den Wert auf *0* (Null) bzw. *1* setzen, wird ein einzelner Thread verwendet. Werte über 1 aktivieren Multithreading. |
| Vertrieb und Marketing | Manuell oder für Intercompany eingegebene Preise und Rabatte aktualisieren | Diese Funktion fügt Unterstützung für manuelle Änderungsrichtlinien für Intercompany-Bestellungen hinzu. Es umfasst die Unterstützung für die Übertragung manueller Änderungsrichtlinien zwischen konzerninternen Verkäufen und Bestellungen. Zuvor wurden manuelle Änderungsrichtlinien nur für nicht zwischenbetriebliche Bestellungen unterstützt. Wenn diese Funktion aktiviert ist, gibt Ihnen das System die Möglichkeit, Preise und Rabatte zu aktualisieren, nachdem Sie Änderungen an einer Intercompany-Bestellung gespeichert haben. Mit dieser Option können Sie auswählen, ob Sie die neuen Preise und Rabattdetails auf die Intercompany-Bestellung anwenden oder die Bestellung unverändert lassen möchten. |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Diese Artikel stehen nicht unbedingt im Zusammenhang mit den neuen Funktionen, die für diese Version hinzugefügt wurden, wie in den vorherigen Abschnitten aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Produktprogrammplanung, (CTP) | [Liefertermine für Kundenaufträge mit CTP berechnen](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Produktprogrammplanung, DDMRP | [Bedarfsgesteuerte Planung im Überblick](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Aktivieren Sie die DDMRP Funktion für Ihr System](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Bestandspositionierung](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Pufferprofil und Ebenen](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Bedarfsgesteuerte Planung](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Visuelle und kollaborative Ausführung](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Lagerortverwaltung | [Container zur Lieferung packen](../warehousing/packing-containers.md)<br>[Packarbeiten zum Packen von ausgehenden Containern und Verarbeiten von Sendungen](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Änderungen am Status der Funktionen in dieser Version

In der folgenden Tabelle sind Funktionen aufgeführt, die ab Version 10.0.29 obligatorisch oder standardmäßig aktiviert wurden. Alle diese Funktionen werden automatisch für Ihr System aktiviert, sobald Sie auf Version 10.0.29 aktualisieren. Obligatorische Funktionen können nicht ausgeschaltet werden, aber Funktionen, die standardmäßig aktiviert sind, können unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ausgeschaltet werden.

In der Tabelle sind auch Funktionen aufgeführt, die zuvor in der öffentlichen Vorschauversion enthalten waren, die aber in Version 10.0.29 allgemein verfügbar geworden sind. Diese Änderung weist darauf hin, dass die Funktionen jetzt für die Verwendung in Produktionsumgebungen empfohlen werden. Standardmäßig sind diese Funktionen ausgeschaltet, falls nicht anders eingestellt. Daher, wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktionsname | Neuer Featurezustand |
| --- | --- | --- |
| Anlagenverwaltung | [Anlagenverwaltungsfunktion für die Produktionsumgebungs-Ausführungsschnittstelle](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Kostenverwaltung | [Beschriftung der Stornierung bei Abschluss und Anpassung in „Stornieren“ ändern](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Obligatorisch |
| Kostenverwaltung | Details der Stücklistenkalkulation-Nachkalkulationsversionen bereinigen | Obligatorisch |
| Kostenverwaltung | [Vergleich der Artikelpreise für Lagerung](../cost-management/compare-item-price.md) | Obligatorisch |
| Kostenverwaltung | [Kostenberechnungsstufe](../cost-management/cost-calculation-level.md) | Standardmäßig aktiviert |
| Kostenverwaltung | Benutzerdefinierte Chargennummereinstellungen für die Stornierung des Lagerabschlusses aktivieren | Standardmäßig aktiviert |
| Kostenverwaltung | [Fortschrittdetails zum Lagerabschluss](whats-new-scm-10-0-21.md) | Standardmäßig aktiviert |
| Kostenverwaltung | [Lagerwert-Berichtsspeicher](../cost-management/inventory-value-report-storage.md) | Obligatorisch |
| Kostenverwaltung | Lagerwertbericht zur Datenbereinigung | Obligatorisch |
| Kostenverwaltung | Flexibler Durchschnitt, Fallback-Kostensequenz | Obligatorisch |
| Kostenverwaltung | Lagerabschlussprotokoll im Raster anzeigen | Obligatorisch |
| Kostenverwaltung | Artikel mit nicht vollständig ausgeglichenen Buchungen im Zusammenfassungsformat anzeigen | Obligatorisch |
| Lager- und Lagerortverwaltung | Leere Stapelverarbeitungsattributwerte zulassen | Obligatorisch |
| Lager- und Lagerortverwaltung | Positionsnummer von Bestandsübertragungsauftragpositionen automatisch erhöhen | Obligatorisch |
| Lager- und Lagerortverwaltung | Umlagerungsauftrag aus der Verkaufsposition erstellen | Obligatorisch |
| Lager- und Lagerortverwaltung | Feld „Bestandserfassungsposition“ im Workflow deaktivieren | Obligatorisch |
| Lager- und Lagerortverwaltung | Warnfunktion für die Parameter des Bestandsqualitätsmanagements aktivieren | Obligatorisch |
| Lager- und Lagerortverwaltung | (China) Physischen Zugang und Abgangskosten von den monatlichen Durchschnittskosten ausschließen | Standardmäßig aktiviert |
| Lager- und Lagerortverwaltung | [Lagerbestandserfassungs-Genehmigungsworkflow](../inventory/inventory-journal-workflow.md) | Obligatorisch |
| Lager- und Lagerortverwaltung | [Speicher für den Bericht zum verfügbaren Lagerbestand](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Obligatorisch |
| Lager- und Lagerortverwaltung | [Gespeicherte Ansichten für die Lagerverwaltung](saved-views-scm.md) | Obligatorisch |
| Lager- und Lagerortverwaltung | Umlagerungsauftragsstornierung | Obligatorisch |
| Lager- und Lagerortverwaltung | Maßeinheit und Einheitsmenge in Bestandserfassungen verwenden | Obligatorisch |
| Lager- und Lagerortverwaltung | Bestandserfassung entsperren | Obligatorisch |
| Fertigung | [Automatische Kommissionierung von für den Lagerort aktivierten Materialien für automatisch gebuchte Kommissionierlisten](whats-new-scm-10-0-23.md) | Allgemein verfügbar |
| Fertigung | Anzeige von Lagerungsdimensionen in der Materialliste für Produktionsarbeitsplan-Arbeitsgänge aktivieren | Obligatorisch |
| Fertigung | [Aktivieren, um Chargen- und Seriennummern einzugeben, während die Fertigmeldung vom Einzelvorgangs-Kartengerät abgeschlossen wird](../production-control/report-finished-job-device.md) | Standardmäßig aktiviert |
| Fertigung | Verbesserte Artikelgewichtsmengenkommissionierung für die Produktion | Standardmäßig aktiviert |
| Fertigung | [Einzelvorgangssuche für die Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Fertigung | [Fertigungssteuerungssystemintegration](../production-control/mes-integration.md) | Standardmäßig aktiviert |
| Fertigung | [Ansicht „Mein Tag“ für die Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) | Standardmäßig aktiviert |
| Fertigung | [Bedarfsbasierte Materialverfügbarkeitsprüfung für Produktionsaufträge](whats-new-scm-10-0-24.md) | Standardmäßig aktiviert |
| Fertigung | [Standardproduktionsreservierung überschreiben](../production-control/override-default-reservation-principle.md) | Obligatorisch |
| Fertigung | [Materialverbrauch in der Produktionsausführungsoberfläche (nicht WMS) registrieren](../production-control/production-floor-execution-configure.md) | Allgemein verfügbar |
| Fertigung | [Bericht über Artikel mit Artikelgewicht über die Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) | Allgemein verfügbar |
| Fertigung | [Bericht zu Co- und Nebenprodukten von der Produktionsausführungsoberfläche](../production-control/production-floor-execution-configure.md) | Standardmäßig aktiviert |
| Fertigung | [Bericht über Planungsartikel in der Produktionsausführungsoberfläche](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Standardmäßig aktiviert |
| Fertigung | [Gespeicherte Ansichten für die Produktionssteuerung](saved-views-scm.md) | Obligatorisch |
| Fertigung | [Vollständige Serien-, Chargen- und Kennzeichennummern in der Produktionsausführungsoberfläche anzeigen](../production-control/production-floor-execution-configure.md) | Obligatorisch |
| Fertigung | [Validieren Sie das Verfallsdatum von Rohstoffen gegen das geplante Verbrauchsdatum](whats-new-scm-10-0-23.md) | Standardmäßig aktiviert |
| Produktprogrammplanung | [Automatische Umwandlung für die Planungsoptimierung](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisch |
| Produktprogrammplanung | [Chargenfähige Umwandlung und Konsolidierung für geplante Sammel- und Verpackungschargenaufträge](whats-new-scm-10-0-20.md) | Standardmäßig aktiviert |
| Produktprogrammplanung | [Artikel mit Lagerbestand einbeziehen, wenn Vorverarbeitungsfilter aktiviert sind](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Standardmäßig aktiviert |
| Produktprogrammplanung | [Endloskapazitätsplanung zur Planungsoptimierung](../master-planning/planning-optimization/infinite-capacity-planning.md) | Standardmäßig aktiviert |
| Produktprogrammplanung | [Margen für Planungsoptimierung](../master-planning/planning-optimization/safety-margins.md) | Obligatorisch |
| Produktprogrammplanung | [Negative Tage für die Planungsoptimierung](../master-planning/planning-optimization/delay-tolerance.md) | Obligatorisch |
| Produktprogrammplanung | [Parallele Autorisierung der angepassten Bedarfsplanung](whats-new-scm-10-0-20.md) | Obligatorisch |
| Produktprogrammplanung | [Umwandlung von Bestellvorschlägen mit Filtern](../master-planning/planning-optimization/planned-order-firming.md) | Obligatorisch |
| Produktprogrammplanung | [Geplante Produktionsaufträge für die Planungsoptimierung](../master-planning/planning-optimization/production-planning.md) | Obligatorisch |
| Produktprogrammplanung | [Handelsvereinbarungen (Einkauf) für die Planungsoptimierung](../master-planning/planning-optimization/purchase-trade-agreement.md) | Obligatorisch |
| Produktprogrammplanung | [Gespeicherte Ansichten für Bestellvorschläge](saved-views-scm.md) | Obligatorisch |
| Beschaffung | Stellt Von- und Bis-Beträge bei Bestellungen in Rechnung | Obligatorisch |
| Beschaffung | Schaltfläche zum Zurücksetzen der Bestellanforderungsverteilung deaktivieren | Standardmäßig aktiviert |
| Beschaffung | [Zurücksetzen beschaffungsbezogener Workflows aktivieren](whats-new-scm-10-0-20.md) | Standardmäßig aktiviert |
| Beschaffung | [Anzahl der Bestellungszeilen pro Stapelverarbeitungsaufgabe begrenzen](whats-new-scm-10-0-27.md) | Standardmäßig aktiviert |
| Beschaffung | [Finanzdimensionen des Kreditors mit Finanzdimension der aktiven Dimensionsverknüpfung in der Bestellung zusammenführen](whats-new-scm-10-0-25.md) | Obligatorisch |
| Beschaffung | [Registrierte Mengen von gelagerten Produkten und Restmengen von nicht gelagerten Produkten für Eingänge und Kreditorenrechnungen buchen](whats-new-scm-10-0-26.md) | Allgemein verfügbar |
| Beschaffung | [Übermäßige Inanspruchnahme von allgemeinen Budgetreservierungen verhindern, wenn mehrere Bestellanforderungen im Workflow sind](whats-new-scm-10-0-21.md) | Standardmäßig aktiviert |
| Beschaffung | [Zuständige Partei für Kaufvertrag](../procurement/purchase-agreements.md) | Obligatorisch |
| Beschaffung | [Gespeicherte Ansichten für Bestellungen](saved-views-scm.md) | Obligatorisch |
| Produktinformationsverwaltung | Vorverarbeitung des Stücklistenberichts, um Zeitüberschreitungen zu vermeiden | Obligatorisch |
| Produktinformationsverwaltung | Standardfinanzdimensionen separat bei Verwendung von Artikelvorlagen | Obligatorisch |
| Produktinformationsverwaltung | Produktdimensionsgruppen für Artikelvorlagen aktivieren | Obligatorisch |
| Produktinformationsverwaltung | Verbesserungen bei der Artikel-Strichcode-Entität | Obligatorisch |
| Produktinformationsverwaltung | Produktvariantennamen basierend auf der Bezeichnung neu generieren | Obligatorisch |
| Produktinformationsverwaltung | [Gespeicherte Ansichten für freigegebene Produkte](saved-views-scm.md) | Obligatorisch |
| Produktinformationsverwaltung | [Verbesserungen an der Seite mit Variantenvorschlägen](../pim/tasks/create-predefined-product-variants.md) | Obligatorisch |
| Vertrieb und Marketing | [Gebührenzuteilung für einen Auftrag](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Obligatorisch |
| Vertrieb und Marketing | Aktualisierungshistorie für Auftrag bereinigen | Obligatorisch |
| Vertrieb und Marketing | [Aktualisierungsverlauf für Verkauf basierend auf Alter bereinigen](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Obligatorisch |
| Vertrieb und Marketing | [Optimierung beim Export von Datenentitäten der Kontaktperson](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Obligatorisch |
| Vertrieb und Marketing | Gesamtrabattgruppe für Verkaufsgutschrift kopieren | Obligatorisch |
| Vertrieb und Marketing | [Suche nach Feldern zur Einführung und zur Fertigstellung von Verkaufsangebotsdokumenten aktivieren](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Obligatorisch |
| Vertrieb und Marketing | [Berichtsleistung von „Top 100“-Kunden verbessern](whats-new-scm-10-0-23.md) | Obligatorisch |
| Vertrieb und Marketing | Wartedatensätze in Verlaufsbereinigungsaufgaben einschließen | Obligatorisch |
| Vertrieb und Marketing | Anzahl der Auftragspositionen pro Stapelverarbeitungsaufgabe begrenzen | Standardmäßig aktiviert |
| Vertrieb und Marketing | [Begrenzen Sie die Anzahl der Verkaufsaufträge, die für die Buchung ausgewählt werden können](whats-new-scm-10-0-21.md) | Obligatorisch |
| Vertrieb und Marketing | Vorkalkulierten Debitorensaldo neu berechnen | Obligatorisch |
| Vertrieb und Marketing | [Rückauftragspositionserfassung mit Dezimalstellen mit und ohne Artikelgewicht](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Obligatorisch |
| Vertrieb und Marketing | [Gespeicherte Ansichten für Vertrieb und Marketing](saved-views-scm.md) | Obligatorisch |
| Vertrieb und Marketing | [Auftragsbestätigung mit nur einem Klick](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Obligatorisch |
| Transportverwaltung | Nichtübereinstimmung von Frachtbriefen aus Frachtrechnungspositionen ohne gebuchte Kreditorenrechnungserfassung zulassen | Standardmäßig aktiviert |
| Transportverwaltung | [Erstellung einer Erfassung vom Typ „Kreditorenrechnung“ beim Verwerfen eines Frachtbriefs aktivieren](whats-new-scm-10-0-20.md) | Standardmäßig aktiviert |
| Transportverwaltung | [Kleinpaketlieferung](../warehousing/small-parcel-shipping.md) | Obligatorisch |
| Transportverwaltung | [USMCA-Zertifizierung des Ursprungsdokuments](../transportation/usmca-certification-of-origin.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Zusätzliche Lagerplatzzone](../warehousing/additional-location-zones.md) | Obligatorisch |
| Lagerortverwaltung | [Arbeit stornieren](../warehousing/cancel-warehouse-work.md) | Obligatorisch |
| Lagerortverwaltung | [Lieferung konsolidieren](../warehousing/configure-shipment-consolidation-policies.md) | Obligatorisch |
| Lagerortverwaltung | [Umlagerungsaufträge aus der Lagerort-App erstellen und verarbeiten](../warehousing/create-transfer-order-from-warehouse-app.md) | Obligatorisch |
| Lagerortverwaltung | Crossdockingvorlagen mit Lagerplatzrichtlinien | Standardmäßig aktiviert |
| Lagerortverwaltung | [Einlagerungsarbeit von ASNs entkoppeln](whats-new-scm-10-0-21.md) | Obligatorisch |
| Lagerortverwaltung | [Verzögerte Put-Vorgänge](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligatorisch |
| Lagerortverwaltung | Verzögerte Einlagerung: Container | Standardmäßig aktiviert |
| Lagerortverwaltung | Verzögerte Einlagerungsverarbeitung - für die Prüfvorlagenfunktion mit dem Auslöseereignis Vorherig aktivieren | Obligatorisch |
| Lagerortverwaltung | [Erwartete Zugänge aus Qualitätsprüfungsaufträgen mit gesperrtem Beispielbestand deaktivieren](../inventory/inventory-blocking.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | Schnelle Überprüfung für mobile Geräte am Lagerort aktivieren | Obligatorisch |
| Lagerortverwaltung | [Erweiterter Parser für GS1-Barcodes](../warehousing/gs1-barcodes.md) | Allgemein verfügbar |
| Lagerortverwaltung | [Flexible auftragsgebundene Kennzeichenreservierung](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligatorisch |
| Lagerortverwaltung | [Flexible Reservierung von Dimensionen auf Lagerortebene](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligatorisch |
| Lagerortverwaltung | [Nutzung von Lagerplatz für Positionskonsolidierung](../warehousing/item-consolidation-location-utilization.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | Kennzeichenempfangsverlauf | Standardmäßig aktiviert |
| Lagerortverwaltung | [Manuelle Lieferungskonsolidierung](../warehousing/consolidate-shipments-manual-workbench.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Dienst zur manuellen Auswahl von Umlagerungszeilen für Admins oder ähnliche vertrauenswürdige Benutzer](whats-new-scm-10-0-28.md) | Allgemein verfügbar |
| Lagerortverwaltung | [Materialhandhabung Geräteschnittstelle](../warehousing/mhax.md) | Obligatorisch |
| Lagerortverwaltung | [Neue Workbenchseiten zur Ladungsplanung](whats-new-scm-10-0-24.md) | Allgemein verfügbar |
| Lagerortverwaltung | [Ausgehende Workloadvisualisierung](../warehousing/outbound-workload-visualization.md) | Obligatorisch |
| Lagerortverwaltung | [Geplantes Crossdocking](../warehousing/planned-cross-docking.md) | Obligatorisch |
| Lagerortverwaltung | [Lagerort-App-Ereignisse verarbeiten](../warehousing/warehouse-app-events.md) | Obligatorisch |
| Lagerortverwaltung | Abfrageerweiterung für die Arbeitsvorlage zur Einlagerung des Co-Produkts und des Nebenprodukts | Obligatorisch |
| Lagerortverwaltung | [Mengen bei Freigabe an Lager auf nächste Verkaufseinheit abrunden](whats-new-scm-10-0-19.md) | Obligatorisch |
| Lagerortverwaltung | [Gespeicherte Ansicht für Ladungsplanungsworkbench](saved-views-scm.md) | Obligatorisch |
| Lagerortverwaltung | [Gespeicherte Ansicht für die Seite mit den Arbeitsdetails](saved-views-scm.md) | Obligatorisch |
| Lagerortverwaltung | [Gespeicherte Ansicht für die Zyklusverarbeitung](saved-views-scm.md) | Obligatorisch |
| Lagerortverwaltung | [Gespeicherte Ansichten für die Ladungsverarbeitung](saved-views-scm.md) | Obligatorisch |
| Lagerortverwaltung | [Gespeicherte Ansichten für die Lieferungsverarbeitung](saved-views-scm.md) | Obligatorisch |
| Lagerortverwaltung | [GS1-Barcodes scannen](../warehousing/gs1-barcodes.md) | Allgemein verfügbar |
| Lagerortverwaltung | Lieferartdetails für Lieferungszyklus | Obligatorisch |
| Lagerortverwaltung | [Gemischte Einheiten platzieren](whats-new-scm-10-0-21.md) | Obligatorisch |
| Lagerortverwaltung | [Schnellere API für das Schließen/erneute Öffnen von Containern auf Verpackungsstation verwenden](whats-new-scm-10-0-21.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Für Wiederbeschaffungsaufträge ausgewählte Vorlagen überprüfen](whats-new-scm-10-0-20.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Höher gestufte Felder der Warehouse-App](../warehousing/warehouse-app-promoted-fields.md) | Obligatorisch |
| Lagerortverwaltung | [Schrittanweisungen für die Lagerort-App](../warehousing/mobile-app-titles-instructions.md) | Obligatorisch |
| Lagerortverwaltung | [Status des Lagerplatzes an einem Lagerort](../warehousing/warehouse-location-status.md) | Obligatorisch |
| Lagerortverwaltung | [Umleitung für Warehouse Management-App](../warehousing/warehouse-app-detours.md) | Standardmäßig aktiviert |
| Lagerortverwaltung | [Zyklus-Batchauftragsdetails](../warehousing/wave-processing.md) | Obligatorisch |
| Lagerortverwaltung | [Wellenausführungsbenachrichtigungen](../warehousing/wave-execution-notifications.md) | Obligatorisch |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Microsoft Dynamics 365 Supply Chain Management 10.0.29 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.29 der Apps für Finanzen und Betrieb (Oktober 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates der Version 10.0.29 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) an.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2022wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
