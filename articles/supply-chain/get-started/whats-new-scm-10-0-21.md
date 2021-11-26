---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.21. (Oktober 2021)
description: In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Supply Chain Management 10.0.21 neu oder geändert wurden.
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3b5f0c6947944ec875c30fa912f830f245b5a48e
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777936"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.21. (Oktober 2021)

[!include [banner](../includes/banner.md)]

Dieses Thema listet Funktionen auf, die in Microsoft Dynamics 365 Supply Chain Management-Version 10.0.21 entweder neu sind oder geändert wurden. Diese Version hat die Build-Nummer 10.0.960 und ist wie folgt verfügbar:

- **Vorschauversion für Release:** August 2021
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** September 2021
- **Allgemeine Verfügbarkeit des Release (automatisches Update):** Oktober 2021

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Die Spalte *Funktion* bietet Links zum [Release-Plan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), wo Sie die offiziellen Release-Termine für jede Funktion sehen können. Die Spalte *Weitere Informationen* enthält weitere Informationen und/oder Links zur zugehörigen Dokumentation.

Die meisten dieser Funktionen müssen aktiviert werden mithilfe von [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), bevor Sie sie verwenden können.

| Funktionsbereich | Funktion | Mehr erfahren |
|---|---|---|
| Bestand&nbsp;und&nbsp;Logistik | [Die Globale Bestandsbuchhaltung ist ein Add-In für Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Startseite für die globale Bestandsbuchhaltung](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Regulierungen des verfügbaren Lagerbestands mit Codes buchen, die mit Gegenkonten verbunden sind](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Ursachencodes für Lagerinventuren anzeigen](../warehousing/reason-codes-for-counting-journals.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Datenexportrichtlinie für referenziertes Verkaufsangebot](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Wählen Sie, ob Änderungen an Daten, auf die Angebote verweisen, dazu führen, dass diese Angebote (oder Positionen) im nächsten inkrementellen Export berücksichtigt werden. Ihre inkrementellen Exporte werden schneller ausgeführt, wenn Sie solche Angebote oder Positionen nicht berücksichtigen.<br><br>Diese Funktion fügt eine Einstellung namens **Von Verkaufsangeboten referenzierte Daten während der Änderungsnachverfolgung überspringen** zur Seite **Debitorenparameter** hinzu. |
| Bestand&nbsp;und&nbsp;Logistik | [Versiegelte Angebote](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [Versiegeltes Angebot bei Angebotsanforderungen](../procurement/sealed-bidding.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Barcodes im Lagerort mit GS1-Formatstandards scannen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1-Barcodes und QR-Codes](../warehousing/gs1-barcodes.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Soft-Reservierung für das Inventory Visibility-Add-In](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Bestandstransparenzreservierungen](../inventory/inventory-visibility-reservations.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Abzugs- und Artikelgewichterweiterungen für das Rückvergütungsmanagement](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Verwalten von Abzügen mit der Abzugsworkbench](../rebate-management/deduction-workbench.md )<br><br>[Rückvergütungen verarbeiten, überprüfen und veröffentlichen](../rebate-management/process-review-post.md)<br><br>[Rückvergütungsverwaltungsgeschäfte](../rebate-management/rebate-management-deals.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Schrittanweisungen für die Lagerort-App](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Schritttitel und Anweisungen für die mobile Warehouse Management-App anpassen](../warehousing/mobile-app-titles-instructions.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Arbeitspausen und Nachverfolgungsaktualisierungen für Gesamttransportkosten](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Nachverfolgung für Einlagerung aktualisieren](../landed-cost/update-tracking-putaway.md )<br><br>[Waren in Zustellung bearbeiten](../landed-cost/in-transit-processing.md) |
| Produktprogrammplanung | [Negative Tage für die Planungsoptimierung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Verzögerungstoleranz (negative Tage)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet eine schrittweise Verbesserung einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben). Wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktion&nbsp;Name&nbsp;in Funktion&nbsp;Verwaltung | Mehr erfahren |
|---|---|---|
| Kostenverwaltung | Fortschrittdetails zum Lagerabschluss | Diese Vorschaufunktion ermöglicht eine detaillierte Ansicht des Lagerabschlussfortschritts. |
| Beschaffung | Übermäßige Inanspruchnahme von allgemeinen Budgetreservierungen verhindern, wenn mehrere Bestellanforderungen im Workflow sind | Diese Vorschaufunktion verbessert die Fehlerprüfung, wenn Benutzer Bestellanforderungen einreichen und genehmigen, die den verbleibenden Saldo einer allgemeinen Budgetreservierungsposition überschreiten. Dies trägt dazu bei, einen übermäßigen Verbrauch allgemeiner Budgetreservierungen zu verhindern, wenn mehrere Bestellanforderungen im Workflow sind. |
| Produktionssteuerung | Vollständige Serien-, Chargen- und Kennzeichennummern in der Produktionsausführungsoberfläche anzeigen | Diese Funktion bietet eine verbesserte Erfahrung beim Anzeigen von Listen von Serien-, Chargen- und Kennzeichennummern in der Produktionsausführungsoberfläche. Die Anzeige wechselt von einer Kartenansicht mit begrenzter Zeichenanzahl in eine Listenansicht, die genügend Platz bietet, um die vollständigen Werte anzuzeigen. Die Liste bietet auch die Möglichkeit, nach bestimmten Nummern zu suchen. |
| Vertrieb und Marketing | Begrenzen Sie die Anzahl der Verkaufsaufträge, die für die Buchung ausgewählt werden können | Mit dieser Funktion können Sie die maximale Anzahl von Verkaufsaufträgen festlegen, die beim Buchen von Bestätigungen, Kommissionierlisten, Lieferscheinen und Rechnungen auf der Seite mit den Verkaufsaufträgen ausgewählt werden können. Sie wird automatisch aktiviert. Die Funktion fügt eine Einstellung namens **Max. Anzahl von Verkaufsaufträgen für die Buchung** auf der Seite **Parameter für Debitoren** hinzu. Die neue Einstellung ist standardmäßig auf einen Wert von *100* festgelegt. Die Funktion trägt dazu bei, die Leistung der Seite mit den Verkaufsaufträgen zu verbessern, wenn eine erhebliche Anzahl von Verkaufsaufträgen ausgewählt ist. Sie hat keinen Einfluss auf die Anzahl der Verkaufsaufträge, die von einer periodischen Aufgabe verarbeitet werden können. |
| Lagerortverwaltung | Einlagerungsarbeit von ASNs entkoppeln | Diese Funktion ist zum Senden und Empfangen von Vorabliefernotizen (ASN) erforderlich, wenn Sie einen Lagerverwaltungs-Workload auf einer Saklierungseinheit ausführen (als Teil einer verteilten Hybridtopologie). Es fügt eine neue dedizierte Datenbanktabelle für das Speichern von Informationen über Einlagerungsarbeiten hinzu. Bisher wurden diese Informationen in Tabellen gespeichert, die auch für die Vorabliefernotizen verwendet werden. |
| Lagerortverwaltung | Gemischte Einheiten platzieren | Ermöglicht dem System, Artikel an Lagerplätzen zu platzieren, die gemischte Einheiten enthalten (z. B. Behälter und Kisten). Für jede Position in der Zuteilungsvorlage können Sie mit dieser Funktion auswählen, ob die Position Artikel Lagerplätzen mit gemischten oder einzelnen Einheiten zuteilen soll. |
| Lagerortverwaltung | Schnellere API für das Schließen/erneute Öffnen von Containern auf Verpackungsstation verwenden | Wenn diese Vorschaufunktion aktiviert ist, werden Bestandstransaktionen in Bezug auf Behälter mithilfe eines neuen, leichtgewichtigen Prozesses erstellt, der die Leistung beim Schließen oder Wiederöffnen von Behältern während der manuellen Verarbeitung an der Verpackungsstation verbessert. |

## <a name="features-turned-on-by-default-in-this-release"></a>Diese Funktionen sind in dieser Version standardmäßig aktiviert.

Die folgende Tabelle listet die Funktionen auf, die in 10.0.21 standardmäßig aktiviert sind. Die meisten Funktionen, die atomatisch aktiviert wurden, können in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) deaktiviert werden.

| Funktionsname | Datum aktivieren | Funktion hinzugefügt am | Status der Funktion | Modul |
| :--- | :--- | :--- | :--- | :--- |
| Speicher für den Bericht zum verfügbaren Lagerbestand | 9/1/2021 | 4/1/2020 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Umlagerungsauftragsstornierung | 9/1/2021 | 7/13/2020 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Bestandserfassung entsperren | 9/1/2021 | 8/17/2020 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Gespeicherte Ansichten für die Lagerverwaltung | 9/1/2021 | 30.09.2020 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Navigation zur Stücklistenversion aus Stücklistenpositionen | 9/1/2021 | 11/11/2019 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Maßeinheit und Einheitsmenge in Bestandserfassungen verwenden | 9/1/2021 | 11/11/2019 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Leere Stapelverarbeitungsattributwerte zulassen | 9/1/2021 | 11/11/2019 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Positionsnummer von Bestandsübertragungsauftragpositionen automatisch erhöhen | 9/1/2021 | 10/11/2019 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Lagerbestandserfassungs-Genehmigungsworkflow | 9/1/2021 | 1/6/2020 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Warnfunktion für die Parameter des Bestandsqualitätsmanagements aktivieren | 9/1/2021 | 10/7/2019 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Umlagerungsauftrag aus der Verkaufsposition erstellen | 9/1/2021 | 8/31/2019 | Standardmäßig aktiviert | Lager- und Lagerortverwaltung |
| Prognosemodellauswahl auf der Seite mit den Informationen zur Bedarfsplanung | 9/1/2021 | 10/11/2019 | Standardmäßig aktiviert | Produktprogrammplanung |
| Visualisierung des Produktprogrammplanfortschritts | 9/1/2021 | 10/7/2019 | Standardmäßig aktiviert | Produktprogrammplanung |
| Automatische Umwandlung für die Planungsoptimierung | 9/1/2021 | 10/11/2019 | Standardmäßig aktiviert | Produktprogrammplanung |
| Parallele Umwandlung von Auftragsvorschlägen | 9/1/2021 | 8/31/2019 | Standardmäßig aktiviert | Produktprogrammplanung |
| Erfolgsmeldung zur Angebotsübermittlung | 9/1/2021 | 5/15/2019 | Standardmäßig aktiviert | Beschaffung |
| Zur Bestellung hinzugefügter Angebotsanforderungsverweis-Link | 9/1/2021 | 8/31/2019 | Standardmäßig aktiviert | Beschaffung |
| Möglichkeit, angenommene Bestellungen aus der Kreditor-Kooperationen als Stapel zu bestätigen | 9/1/2021 | 9/10/2019 | Standardmäßig aktiviert | Beschaffung |
| cXML-Einkaufserweiterungen | 9/1/2021 | 11/11/2019 | Standardmäßig aktiviert | Beschaffung |
| Link &quot;Offene veröffentlichte Angebotsanforderungen&quot; als Kachel anzeigen | 9/1/2021 | 30.09.2020 | Standardmäßig aktiviert | Beschaffung |
| Fragen und Antworten zur Angebotsanforderung | 9/1/2021 | 2/19/2020 | Standardmäßig aktiviert | Beschaffung |
| Gefahrengüter-Produktinformationen und Versanddokumentation | 9/1/2021 | 6/14/2020 | Standardmäßig aktiviert | Produktinformationsverwaltung |
| Strenge Überprüfung auf Standardauftragsmengen | 9/1/2021 | 6/24/2020 | Standardmäßig aktiviert | Produktinformationsverwaltung |
| Herkunftsland-Verwaltungsfunktion | 9/1/2021 | 7/13/2020 | Standardmäßig aktiviert | Produktinformationsverwaltung |
| Gespeicherte Ansichten für freigegebene Produkte | 9/1/2021 | 30.09.2020 | Standardmäßig aktiviert | Produktinformationsverwaltung |
| Verbesserungen der Dialogfelder „Genehmigen“ und „Einzelvorgänge übertragen“ | 9/1/2021 | 10/11/2019 | Standardmäßig aktiviert | Produktionssteuerung |
| Das Kennzeichen für Fertigmeldung wurde zum Einzelvorgangslistengerät hinzugefügt. | 9/1/2021 | 8/31/2019 | Standardmäßig aktiviert | Produktionssteuerung |
| Eine neue Schaltfläche „Pause stoppen“ wurde zur Seite „Einzelvorgangskarten-Terminal“ hinzugefügt | 9/1/2021 | 2/19/2020 | Standardmäßig aktiviert | Produktionssteuerung |
| Teilweisen Zugang von Artikeln aus Fremdarbeit aktivieren und ein Problem bei der Berechnung von Ausschuss für Stücklistenpositionen vom Typ „Lieferant“ beheben. | 9/1/2021 | 11/11/2019 | Standardmäßig aktiviert | Produktionssteuerung |
| Gespeicherte Ansichten zur Produktionssteuerung | 9/1/2021 | 8/17/2020 | Standardmäßig aktiviert | Produktionssteuerung |
| Dynamics 365 Guides für die Herstellung | 9/1/2021 | 7/13/2020 | Standardmäßig aktiviert | Produktionssteuerung |
| Produktionsumgebungsausführung | 9/1/2021 | 30.09.2020 | Standardmäßig aktiviert | Produktionssteuerung |
| Funktion zum Sperren von Jobkartengerät und Jobkartenterminal, damit sie saniert werden können | 9/1/2021 | 5/10/2020 | Standardmäßig aktiviert | Produktionssteuerung |
| Gebührenzuteilung für einen Auftrag | 9/1/2021 | 30.09.2020 | Standardmäßig aktiviert | Vertrieb und Marketing |
| Begrenzen Sie die Anzahl der Verkaufsaufträge, die für die Buchung ausgewählt werden können | 9/1/2021 | 9/1/2021 | Standardmäßig aktiviert | Vertrieb und Marketing |
| Aktualisierungshistorie für Auftrag bereinigen | 9/1/2021 | 9/1/2021 | Standardmäßig aktiviert | Vertrieb und Marketing |
| Nummernkreis für Zykluszählung-Arbeit ändern | 9/1/2021 | 10/7/2019 | Standardmäßig aktiviert | Lagerortverwaltung |
| Aufgabenbasierte Wellenbedarfswiederbeschaffung | 9/1/2021 | 10/7/2019 | Obligatorisch | Lagerortverwaltung |
| Feld „Gesamtwert“ auf den Seiten &quot;Alle Ladungen&quot; und &quot;Ladungsdetails&quot; ausblenden | 9/1/2021 | 10/7/2019 | Standardmäßig aktiviert | Lagerortverwaltung |
| Zyklusbeschriftungsdruck | 9/1/2021 | 2/19/2020 | Obligatorisch | Lagerortverwaltung |
| Zuordnung von Bestellbestandsbuchungen zur Ladung | 9/1/2021 | 1/6/2020 | Obligatorisch | Lagerortverwaltung |
| Erweiterte Layouts für Kennzeichenbeschriftung | 9/1/2021 | 2/19/2020 | Standardmäßig aktiviert | Lagerortverwaltung |
| Organisationsweite Arbeitssperrung | 9/1/2021 | 2/19/2020 | Obligatorisch | Lagerortverwaltung |
| Arbeitspositionsdetails | 9/1/2021 | 10/11/2019 | Standardmäßig aktiviert | Lagerortverwaltung |
| Feld „Lagerbestandsumlagerungsstatus“ des mobilen Geräts bearbeitbar machen | 9/1/2021 | 10/16/2019 | Standardmäßig aktiviert | Lagerortverwaltung |
| Ausgehende Lieferungen aus Batchaufträgen bestätigen | 9/1/2021 | 7/13/2020 | Standardmäßig aktiviert | Lagerortverwaltung |
| Steuern, ob eine Empfangszusammenfassungsseite auf mobilen Geräten angezeigt wird | 9/1/2021 | 4/1/2020 | Standardmäßig aktiviert | Lagerortverwaltung |
| Aufforderung zum Auflösen mehrdeutiger Namen für &#39;Lagerplatz/Kennzeichen&#39; | 9/1/2021 | 4/1/2020 | Standardmäßig aktiviert | Lagerortverwaltung |
| Produktvarianten und Rückverfolgungsangaben in der Lagerhaltungs-App beim Artikelempfang aus Ladung erfassen | 9/1/2021 | 5/10/2020 | Standardmäßig aktiviert | Lagerortverwaltung |
| Es ist nicht zulässig, Ladungen zu erstellen, die nicht den Anforderungen der Vorlage für die Wellenladungserstellung entsprechen. | 9/1/2021 | 8/17/2020 | Standardmäßig aktiviert | Lagerortverwaltung |
| Alle Aktivitäten für Mehrfach-SKU-Lagerplatzrichtlinien auswerten | 9/1/2021 | 30.09.2020 | Standardmäßig aktiviert | Lagerortverwaltung |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfethemen kürzlich hinzugefügt oder erheblich aktualisiert. Sie beziehen sich nicht unbedingt auf die neuen Funktionen, die für diese Version hinzugefügt wurden, wie im vorherigen Abschnitt aufgeführt, aber sie können Ihnen helfen, mehr aus den vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Themen |
|---|---|
| Produktprogrammplanung | [Bestandsplanung](../master-planning/inventory-forecast.md) |
| Produktprogrammplanung | [Parameter, die von der Planungsoptimierung nicht verwendet werden](../master-planning/planning-optimization/not-used-parameters.md) |
| Produktprogrammplanung | [Wiederbeschaffungsmethoden und Mengenänderung](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Produktprogrammplanung | [Zeitplanung mit unbegrenzter Kapazität](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Produktprogrammplanung | [Planhistorie und Planungsprotokolle einsehen](../master-planning/planning-optimization/plan-history-logs.md) |
| Lagerortverwaltung | [Verpackungsstrategien für Container](../warehousing/container-packing-strategy-overview.md) |
| Lagerortverwaltung | [Beispiele für Zykluszählungsszenarien](../warehousing/cycle-counting-scenarios.md) |
| Lagerortverwaltung | [Eingehende ASNs über die V2-Datenentität importieren](../warehousing/import-asn-v2-data-entity.md) |
| Lagerortverwaltung | [Zu hohe Entnahme für Aufträge und Umlagerungsaufträge verwenden](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Lagerortverwaltung | [Zyklusbeschriftungsdruck während des Zyklus planen](../warehousing/configure-task-based-wave-label-printing.md) |
| Lagerortverwaltung | [Was ist neu oder geändert in der Warehouse Management Mobile-App](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdate für Finance and Operations Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.21 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattformupdates für Version 10.0.21 von Finance and Operations-Apps (Oktober 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.21 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de) an.

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2021wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Das Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
