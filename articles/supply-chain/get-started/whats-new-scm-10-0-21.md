---
title: Vorschauversion von Dynamics 365 Supply Chain Management 10.0.21 (Oktober 2021)
description: In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Supply Chain Management 10.0.21 neu oder geändert wurden.
author: kamaybac
ms.date: 08/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 517411512760374f1d1fd3b8ea3615563c47202c2e847569d00cb17a94657630
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012036"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Vorschauversion von Dynamics 365 Supply Chain Management 10.0.21 (Oktober 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema werden die Funktionen aufgeführt, die in der Microsoft Dynamics 365 Supply Chain Management Vorschauversion 10.0.21 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.960 und ist wie folgt verfügbar:

- **Vorschauversion für Release:** August 2021
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** September 2021
- **Allgemeine Verfügbarkeit des Release (automatisches Update):** Oktober 2021

## <a name="known-deployment-issue"></a>Bekanntes Bereitstellungsproblem
Bei der Bereitstellung von Version 10.0.21 auf IaaS erhalten Sie möglicherweise die folgende Bereitstellungswarnung:

**Warnungscode:** 95017

**Warnmeldung:** Ausführung von Skript [SetupDiagnostics] gegen VM fehlgeschlagen

Die Bereitstellung funktioniert trotz der Warnung, jedoch können die folgenden bekannten Probleme in Lifecycle Services (LCS) auftreten:

-   Auf der Seite **Umgebungsüberwachung** erscheint der Link **Detaillierte Versionsinformationen anzeigen** nicht, sodass Sie die spezifischen Versionen der in Ihrer Umgebung installierten Module nicht sehen können. Ohne diese Daten können nachfolgende Hotfixes fehlschlagen, da der Prozess, der Hotfixes anwendet, diese Daten verwendet, um zu überprüfen, ob die Voraussetzungen für die Modulversion erfüllt sind. Da es nicht möglich ist, den PEAP/Vorschauversion in der Produktion zu verwenden oder Hotfixes anzuwenden, sollten die Auswirkungen minimal sein.
-   Die Registerkarten **Leistungsmetriken** und **Indexanalyse** auf der Seite **Umgebungsüberwachung** Seite unter Einblicke in SQL zeigen keine Daten an. Alle anderen Funktionen der **Umgebungsüberwachung** funktionieren wie gewünscht.
-   Die Seite **Vollständige Systemdiagnose** wird nicht zugänglich sein. Die zugehörigen Daten über den Status der nächtlichen Collector-Läufe und die von den Regeln erkannten Probleme werden ebenfalls nicht angezeigt.

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Die Spalte *Funktion* bietet Links zum [Release-Plan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), wo Sie die offiziellen Release-Termine für jede Funktion sehen können. Die Spalte *Weitere Informationen* enthält weitere Informationen und/oder Links zur zugehörigen Dokumentation.

Die meisten dieser Funktionen müssen aktiviert werden mithilfe von [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), bevor Sie sie verwenden können. Einige der aufgelisteten Funktionen befinden sich noch in der Vorschau, während andere möglicherweise bereits allgemein verfügbar sind.

| Funktionsbereich | Funktion | Weitere Informationen |
|---|---|---|
| Bestand&nbsp;und&nbsp;Logistik | [Die Globale Bestandsbuchhaltung ist ein Add-In für Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Startseite für die globale Bestandsbuchhaltung](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Regulierungen des verfügbaren Lagerbestands mit Codes buchen, die mit Gegenkonten verbunden sind](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Ursachencodes für Lagerinventuren anzeigen](../warehousing/reason-codes-for-counting-journals.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Datenexportrichtlinie für referenziertes Verkaufsangebot](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Wählen Sie, ob Änderungen an Daten, auf die Angebote verweisen, dazu führen, dass diese Angebote (oder Positionen) im nächsten inkrementellen Export berücksichtigt werden. Ihre inkrementellen Exporte werden schneller ausgeführt, wenn Sie solche Angebote oder Positionen nicht berücksichtigen.<br><br>Diese Funktion fügt eine Einstellung namens **Von Verkaufsangeboten referenzierte Daten während der Änderungsnachverfolgung überspringen** zur Seite **Debitorenparameter** hinzu. |
| Bestand&nbsp;und&nbsp;Logistik | [Barcodes im Lagerort mit GS1-Formatstandards scannen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | *Demnächst*<!-- KFM: Add doc link when ready. --> |
| Bestand&nbsp;und&nbsp;Logistik | Versiegelte Angebote <!-- KFM: Add RP link when available --> | *Demnächst*<!-- KFM: Add doc link when ready. --> |
| Bestand&nbsp;und&nbsp;Logistik | [Abzugs- und Artikelgewichterweiterungen für das Rückvergütungsmanagement](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Verwalten von Abzügen mit der Abzugsworkbench](../rebate-management/deduction-workbench.md )<br><br>[Rückvergütungen verarbeiten, überprüfen und veröffentlichen](../rebate-management/process-review-post.md)<br><br>[Rückvergütungsverwaltungsgeschäfte](../rebate-management/rebate-management-deals.md) |
| Bestand&nbsp;und&nbsp;Logistik | [Schrittanweisungen für die Lagerort-App](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | *Demnächst*<!-- KFM: Add doc link when ready --> |
| Bestand&nbsp;und&nbsp;Logistik | [Arbeitspausen und Nachverfolgungsaktualisierungen für Gesamttransportkosten](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Nachverfolgung für Einlagerung aktualisieren](../landed-cost/update-tracking-putaway.md )<br><br>[Waren in Zustellung bearbeiten](../landed-cost/in-transit-processing.md) |
| Produktprogrammplanung | [Negative Tage für die Planungsoptimierung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Verzögerungstoleranz (negative Tage)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet eine schrittweise Verbesserung einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben). Wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktionsbereich | Funktion&nbsp;Name&nbsp;in Funktion&nbsp;Verwaltung | Weitere Informationen |
|---|---|---|
| Kostenverwaltung | Fortschrittdetails zum Lagerabschluss | Diese Vorschaufunktion ermöglicht eine detaillierte Ansicht des Lagerabschlussfortschritts. |
| Produktprogrammplanung | (Vorschau) Prioritätsgesteuerte MRP-Unterstützung für die Planungsoptimierung | Diese Vorschaufunktion für die Planungsoptimierung ermöglicht eine Masterprogrammplanung, die von der Planungspriorität mit Neubestellungspunkt gesteuert wird. Zu den hervorgehobenen Änderungen gehören: Feld **Planungspriorität** in Auftragspositionen, Bestellpositionen, Bedarfsplanung und geplante Aufräge; eine neue Dispositionesverfahrenoption; Feld **Artikelabdeckung** für Neubestellungspunkt; Produktprogrammplanungs-Setup-Formulare zur Steuerung der Planungsprioritäts-Setup; und Berechnungslogik für die Planungsoptimierung, um die Planungspriorität festzulegen und zu respektieren. |
| Beschaffung | Übermäßige Inanspruchnahme von allgemeinen Budgetreservierungen verhindern, wenn mehrere Bestellanforderungen im Workflow sind | Diese Vorschaufunktion verbessert die Fehlerprüfung, wenn Benutzer Bestellanforderungen einreichen und genehmigen, die den verbleibenden Saldo einer allgemeinen Budgetreservierungsposition überschreiten. Dies trägt dazu bei, einen übermäßigen Verbrauch allgemeiner Budgetreservierungen zu verhindern, wenn mehrere Bestellanforderungen im Workflow sind. |
| Produktionssteuerung | Vollständige Serien-, Chargen- und Kennzeichennummern in der Produktionsausführungsoberfläche anzeigen | Diese Funktion bietet eine verbesserte Erfahrung beim Anzeigen von Listen von Serien-, Chargen- und Kennzeichennummern in der Produktionsausführungsoberfläche. Die Anzeige wechselt von einer Kartenansicht mit begrenzter Zeichenanzahl in eine Listenansicht, die genügend Platz bietet, um die vollständigen Werte anzuzeigen. Die Liste bietet auch die Möglichkeit, nach bestimmten Nummern zu suchen. |
| Lagerortverwaltung | Einlagerungsarbeit von ASNs entkoppeln | Diese Funktion ist zum Senden und Empfangen von Vorabliefernotizen (ASN) erforderlich, wenn Sie einen Lagerverwaltungs-Workload auf einer Saklierungseinheit ausführen (als Teil einer verteilten Hybridtopologie). Es fügt eine neue dedizierte Datenbanktabelle für das Speichern von Informationen über Einlagerungsarbeiten hinzu. Bisher wurden diese Informationen in Tabellen gespeichert, die auch für die Vorabliefernotizen verwendet werden. |
| Lagerortverwaltung | Gemischte Einheiten platzieren | Ermöglicht dem System, Artikel an Lagerplätzen zu platzieren, die gemischte Einheiten enthalten (z. B. Behälter und Kisten). Für jede Position in der Zuteilungsvorlage können Sie mit dieser Funktion auswählen, ob die Position Artikel Lagerplätzen mit gemischten oder einzelnen Einheiten zuteilen soll. |
| Lagerortverwaltung | Schnellere API für das Schließen/erneute Öffnen von Containern auf Verpackungsstation verwenden | Wenn diese Vorschaufunktion aktiviert ist, werden Bestandstransaktionen in Bezug auf Behälter mithilfe eines neuen, leichtgewichtigen Prozesses erstellt, der die Leistung beim Schließen oder Wiederöffnen von Behältern während der manuellen Verarbeitung an der Verpackungsstation verbessert. |

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
