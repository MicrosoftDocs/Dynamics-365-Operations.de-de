---
title: Vorschau auf Dynamics 365 Supply Chain Management 10.0.27 (Juli 2022)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.27 neu oder geändert wurden.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: a91f2cdae0fed75f07d6cae86d24aeedfca80e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844495"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>Vorschau auf Dynamics 365 Supply Chain Management 10.0.27 (Juli 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Vorschauversion 10.0.27 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1227 und ist im folgenden Zeitplan verfügbar:

- **Vorschau auf die Veröffentlichung:** April 2022
- **Allgemeine Verfügbarkeit der Freigabe (Selbst-Update):** Juni 2022
- **Allgemeine Verfügbarkeit der Version (Auto-Update):** Juli 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Artikels, um Funktionen einzubeziehen, die zum Build hinzugefügt wurden, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---|---|---|---|
| Bestand und Logistik | [Bestandszuordnung für das Bestandssichtbarkeits-Add-In](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Inventory Visibility Bestandszuweisung](../inventory/inventory-visibility-allocation.md) | Standardmäßig aktiviert |
| Fertigung | Ansicht „Mein Tag“ für die Produktionsausführungsoberfläche | [Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte](../production-control/production-floor-execution-use.md) und [Urlaubssalden in der Produktionsausführungsoberfläche anzeigen](../production-control/production-floor-execution-payroll-stats.md) | Funktionsverwaltung:<br>*Ansicht „Mein Tag“ für die Produktionsausführungsoberfläche* |
| Planung | [Unterstützung für die Planungsoptimierung zur Vergabe von Unteraufträgen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Verwalten Sie Lohnarbeit in der Produktion](../production-control/manage-subcontract-work-production.md) | Standardmäßig aktiviert |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein‑ oder ausschalten möchten, müssen Sie dies in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Produktprogrammplanung | Lieferzeit des Bestands beim Erstellen eines geplanten Umlagerungsauftrags berücksichtigen | Wenn ein geplanter Umlagerungsauftrag erstellt wird, führt diese Funktion dazu, dass das System die Lieferzeit des Bestands berücksichtigt, die in den standardmäßigen Auftragseinstellungen des Artikels angegeben ist, wenn das Wareneingangsdatum des geplanten Umlagerungsauftrags für die Lieferdatumskontrolle als *Kein* oder *Verkauf* berechnet wird. Wenn die Vorlaufzeit der Umlagerung angegeben wird, wird ihr Wert für die Berechnung des Wareneingangsdatums verwendet und die Transporttage werden ignoriert. |
| Beschaffung | Standardmäßige Brokervertragssteuerinformationen auf Kreditorenrechnungspositionen | Mit dieser Funktion wird eine Logik eingeführt, um Standardwerte für die Felder **Mehrwertsteuer** und **Artikelmehrwertsteuer** in Kreditorenrechnungspositionen von Brokerverträgen festzulegen. Diese Logik wird nur angewandt, wenn die Kostenart der Brokervertragszeile Sachkonto/Sachkonto ist. Die Artikelmehrwertsteuergruppe übernimmt ihren Standardwert aus der Brokerbeschaffungskategorie (falls eingerichtet) oder aus der Kostenart. Die Mehrwertsteuergruppe übernimmt ihren Standardwert aus dem Kreditorenkonto. |
| Beschaffung | Anzahl der Bestellungszeilen pro Stapelverarbeitungsaufgabe begrenzen | Diese Funktion hilft Ihnen, die Systemleistung beim Buchen von Bestätigungen und Produktzugängen zu optimieren. Sie fügt eine neue Einstellung namens **Zeilen pro Aufgabe** auf der Registerkarte **Lieferung** der Seite **Beschaffungs- und Beschaffungsparameter** hinzu. Mit dieser neuen Einstellung können Sie die Anzahl der von jeder Stapelverarbeitungsaufgabe verarbeiteten Auftragszeilen begrenzen. Dies trägt dazu bei, dass große Stapelverarbeitungsaufgaben das System nicht verlangsamen. |
| Produktinformationsverwaltung | Produktattributwerte ausfüllen | Diese Funktion fügt eine periodische Aufgabe namens *Produktattributwerte ausfüllen* hinzu. Diese neue periodische Aufgabe erstellt fehlende Datensätze mit Produktattributwerten für Attribute, die mit Produkten über eine Produktkategorie verknüpft sind. |
| Produktionssteuerung | Zusätzliche Konfiguration auf der Produktionsausführungsoberfläche | <p>Diese Funktion fügt der Seite **Produktionsausführung konfigurieren** die folgenden Optionen hinzu:</p><ul><li>**Automatisches Öffnen des Startdialogs bei Abschluss der Suche** – Bei Aktivierung dieser Option wird das Dialogfeld **Einzelvorgang starten** automatisch geöffnet, wenn Arbeitskräfte die Suchleiste zur Suche nach der Stelle verwenden.</li><li>**Automatisches Öffnen des Berichtsfortschrittsdialogs bei Abschluss der Suche** – Bei Aktivierung dieser Option wird das Dialogfeld **Fortschritt melden** für den Einzelvorgang automatisch geöffnet, wenn Arbeitskräfte die Suchleiste zur Suche nach der Stelle verwenden.</li><li>**Standardmäßige Restmenge im Berichtsfortschrittsdialog** – Bei aktivierter Option zeigt das Dialogfeld **Fortschritt melden** die verbleibende Menge, die für einen Produktionsauftrag gemeldet werden soll.</li></ul><p>Weitere Informationen finden Sie unter [Produktionsausführungsschnittstelle konfigurieren](../production-control/production-floor-execution-configure.md).</p> |
| Produktionssteuerung | Produktionsteams in der Produktionsausführungsoberfläche | <p>Wenn mehrere Arbeitskräfte dem gleichen Produktionsauftrag zugewiesen sind, können sie nun eine Arbeitskraft als Pilot benennen. Die verbleibenden Arbeitskräfte werden automatisch zu Assistenten dieses Piloten. Für das übrige Team muss nur der Pilot den Auftragsstatus registrieren, während die Zeitdatensätze für alle Teammitglieder gelten. Diese Funktion unterstützt außerdem ein Szenario namens *Unterstützende Ressource*. In diesem Szenario kann sich eine Arbeitskraft als Assistent einer anderen Arbeitskraft registrieren, die dann Pilot der neu gebildeten Gruppe wird.</p><p>Weitere Informationen finden Sie unter [Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte](../production-control/production-floor-execution-use.md).</p> |
| Produktionssteuerung | Bericht über Planungsartikel in der Produktionsausführungsoberfläche | Diese Funktion vereinfacht den Prozess der Berichterstellung für Chargenaufträge für Planungsartikel auf der Produktionsausführungsoberfläche. Wenn ein Chargenauftrag für ein Produkt mit dem Produktionstyp *Planungsartikel* erstellt wird, ist es nur möglich, die Co-Produkte und Nebenprodukte für diese Chargenaufträge als abgeschlossen zu melden. Chargenaufträge für Planungsartikel werden normalerweise zur Unterstützung von Zerlegungsprozessen verwendet, bei denen ein Rohmaterialprodukt in mehrere eindeutig identifizierbare Produkte zerlegt wird. Wenn ein Chargenauftrag für einen Planungsartikel als abgeschlossen gemeldet wird, werden den Arbeitskräften nur die Co-Produkte und Nebenprodukte im Dialog **Fortschritt melden** angezeigt. Zuvor wurde auch der Planungsartikel angezeigt, was die Arbeitskräfte verwirren konnte. |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Diese Artikel stehen nicht unbedingt im Zusammenhang mit den neuen Funktionen, die für diese Version hinzugefügt wurden, wie in den vorherigen Abschnitten aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Kostenverwaltung | [Gewichteter Durchschnitt (Datum) enthält physischen Wert und Markierung](../cost-management/weighted-average-date.md) |
| Verteilte Hybridtopologie | [Ausprobieren von Scale-Units in einer verteilten hybriden Topologie](../cloud-edge/cloud-edge-try-out.md) |
| Duales Schreiben | [On-Demand-Synchronisierung mit dem Preisgestaltungsmodul von Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Lagerortverwaltung | [Für Lagerort freigeben](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Microsoft Dynamics 365 Supply Chain Management 10.0.27 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.27 der Finanz- und Betriebs-Apps (Juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.27 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271) an.

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
