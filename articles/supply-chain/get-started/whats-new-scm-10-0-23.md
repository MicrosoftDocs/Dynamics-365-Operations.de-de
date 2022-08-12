---
title: Was ist neu oder geändert in Dynamics 365 Supply Chain Management 10.0.23 (Januar 2022)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.23 neu oder geändert wurden.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: ded645ebaea1230b68525c247ee91e3893211774
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124527"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10023-january-2022"></a>Was ist neu oder geändert in Dynamics 365 Supply Chain Management 10.0.23 (Januar 2022)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.23 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1037 und ist wie folgt verfügbar:

- **Vorschau auf Release:** Oktober 2021
- **Allgemeine Verfügbarkeit von Release (manuelles Update):** Dezember 2021
- **Allgemeine Verfügbarkeit von Release (automatisches Update):** Januar 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Die Spalte *Funktion* bietet Links zum [Release-Plan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), wo Sie die offiziellen Release-Termine für jede Funktion sehen können. Die Spalte *Weitere Informationen* enthält weitere Informationen und/oder Links zur zugehörigen Dokumentation. Informationen zum Aktivieren einer Funktion finden Sie in der Spalte *Aktiviert von*. Weitere Informationen zur Funkions-Verwaltung finden Sie unter [Funktions-Verwaltung Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Möglicherweise aktualisieren wir diesen Artikel, um Funktionen einzubeziehen, die es in den Build geschafft haben, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von   |
|---|---|---|---|
| Globales Adressbuch | Definieren Sie in der Adresseinrichtung einen Standardstaat/eine Standardprovinz für jedes Land/jede Region | Sie können nun in der Adresseinrichtung für das globale Adressbuch für jedes Land/jede Region ein Standard-Bundesland/eine Standardprovinz definieren. Wenn ein Standardstaat/eine Standardprovinz festgelegt ist, wird dies der Standardwert, der in die Felder des Bundesstaats/der Provinz eingegeben wird, wenn Sie einen neuen Landkreis- oder Stadtdatensatz für dieses Land/diese Region erstellen. Siehe auch [Adresseinrichtung](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Standardmäßig aktiviert. |
| Bestand&nbsp;und&nbsp;Logistik | [Aufgaben in Mobile Warehouse Management-App pausieren](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Umleitungen für Schritte in den Menüpunkten des Mobilgeräts konfigurieren](../warehousing/warehouse-app-detours.md) | Funktionsverwaltung (*Umwege über die Warehouse Management-App*) |
| Bestand&nbsp;und&nbsp;Logistik | [Höher gestufte Felder der Warehouse-App](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Höher gestufte Felder für Schritte im mobilen Gerät konfigurieren](../warehousing/warehouse-app-promoted-fields.md)| Funktionsverwaltung (*Beworbene Felder für die Lager-App*) |
| Fertigung | [Integration des Fertigungssteuerungssystems](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [Integration in Fertigungssteuerungssysteme von Drittanbietern](../production-control/mes-integration.md) | Funktionsverwaltung (*Integration des Fertigungssteuerungssystems*) |
| Fertigung | [Bericht zu Co- und Nebenprodukten von der Produktionsausführungsoberfläche](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte](../production-control/production-floor-execution-use.md) | Funktionsverwaltung (*Bericht zu Co- und Nebenprodukten von der Produktionsausführungsoberfläche*) |
| Planung | [Unterstützung der Planungsoptimierung für prioritätsbasierte Planung](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [Prioritätsbasierte Planung](../master-planning/planning-optimization/priority-based-planning.md) | Funktionsverwaltung (*Prioritätsgesteuerte MRP-Unterstützung für die Planungsoptimierung*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version neu sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein- oder ausschalten möchten, müssen Sie dies in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun, wo sie mit der Spalte *Funktionsname in der Funktionsverwaltung* der folgenden Tabelle angezeigt werden.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Anlagenverwaltung | Gegenkonten für Ausgaben in Arbeitsauftragserfassungen | Mit dieser Funktion können Sie für jede in einem Arbeitsauftragsjournal aufgeführte Ausgabe ein Ausgleichskonto angeben. Normalerweise können Sie jeder Ausgabe ein Kreditorenkonto zuordnen, aber auch andere Kontotypen werden unterstützt. Es fügt zwei neue Spalten (**Verrechnungskontotyp** und **Gegenkonto**) zum Inforegister **Aufwand** auf der Seite **Arbeitsauftragsjournal** hinzu.|
| Kostenverwaltung | Zugehörige Belege für Neubewertungen von Standardkostenrundungen | <p>Wenn eine Bestandsfinanzbuchung (z. B. eine Kundenauftragsrechnung oder eine Bestandsbuchung) vorgenommen wird, veranlasst diese Funktion das System, einen separaten Beleg für alle zugehörigen Standardkostenrundungs-Neubewertungen zu erstellen und diesen als zugehörigen Beleg an den Finanzbuchungsbeleg anzuhängen.</p><p>Ohne diese Funktion zeichnet das System die Neubewertungen der Standardkostenrundung auf derselben Belegbuchung auf. Dieses Verhalten kann manchmal zu widersprüchlichen Datumsangaben führen, da die Neubewertungen das Sitzungs- oder Systemdatum verwenden, während Finanzbuchungen das Buchungsdatum verwenden.</p> |
| Lager- und Lagerortverwaltung | \[Russland\] Wertmäßige Storno-Lagerbuchungen gemäß dem Korrekturkennzeichen im Finanzbeleg für Aufträge buchen | Diese Funktion wirkt sich auf die Funktion zur Korrektur von Gutschriften für Russland aus. Es ermöglicht das Buchen von Bestandsbuchungen für Verkaufsrechnungen gemäß der Korrekturmöglichkeit im Hauptbuch. Wenn diese Funktion aktiviert ist, gibt es keine Diskrepanzen mehr zwischen **Korrektur** Markierung auf dem Finanzbeleg der Lagertransaktion und **Storno** Flag auf Lagertransaktionen. |
| Lager- und Lagerortverwaltung | (Russland) Berechnung des Lagersaldo-Umschlagsberichts im Batch | Für russische Lokalisierungen von Supply Chain Management bietet diese Funktion die Möglichkeit, den *Lagersaldo-Umschlagsbericht* im Batch auszuführen, ihn zu speichern und die früher generierten Berichte zu anzeigen. |
| Lager- und Lagerortverwaltung | (Russland) Übersetzungen in lokale Sprache in landes- oder regionsspezifischen Primärformularen in der Lagerverwaltung verwenden | Für russische Lokalisierungen von Supply Chain Management bietet diese Funktion die Verwendung von russischen Übersetzungen für Produkt-/Artikelnamen und Maßeinheiten in den folgenden russischspezifischen Lagerausdrucken: Inventurliste (INV-3), Inventurliste (INV-5) und Inventurliste (INV-6). |
| Produktprogrammplanung | Azure Machine Learning Service für die Planung des Bedarfs | Diese Funktion ermöglicht es dem Azure Machine Learning Service, Bedarfsplanungen basierend auf historischen Daten zu generieren. Weitere Informationen finden Sie unter [Einrichtung der Bedarfsplanung](../master-planning/demand-forecasting-setup.md). |
| Beschaffung | Aktualisierungsverlauf für Bestellung bereinigen | Mit dieser Funktion können Sie temporäre historische Aufzeichnungen im Zusammenhang mit Bestellaktualisierungen bereinigen. Es fügt eine neue Schaltfläche namens **Update-Verlauf der Käufe bereinigen** zum Aktionsbereich auf der Seite **Alle Bestellungen** hinzu. Diese Funktion ist standardmäßig aktiviert. |
| Produktionssteuerung | (Vorschau) Automatische Kommissionierung von für den Lagerort aktivierten Materialien für automatisch gebuchte Kommissionierlisten | Mit dieser Funktion können Sie Lagerungsdimensionen für automatisch gebuchte, abgeleitete und zurückgelieferte Kommissionierlistenerfassungen automatisch kommissionieren und abschließen. |
| Produktionssteuerung | Validieren Sie das Verfallsdatum von Rohstoffen gegen das geplante Verbrauchsdatum | Diese Funktion ändert, wie das Verfallsdatum von Chargen validiert wird, wenn eine Charge von Rohmaterial zur Verwendung während der Produktion reserviert wird. Wenn diese Funktion aktiviert ist, wird das Ablaufdatum der Charge gegen das geplante Verbrauchsdatum (das Rohmaterialdatum) validiert, das in der Produktionsstücklistenposition oder Chargenauftragsformelposition festgelegt ist. Wenn diese Funktion deaktiviert ist, wird das Ablaufdatum der Charge mit dem geplanten Lieferdatum des Produktions- oder Chargenauftrags (wie zuvor) verglichen. |
| Vertrieb und Marketing | Aktualisierungsverlauf für Verkauf basierend auf Alter bereinigen | Mit dieser Funktion können Sie das maximale Alter von Datensätzen festlegen, die aufbewahrt werden sollen, wenn die periodische Aufgabe **Bereinigung der Verkaufsaktualisierungshistorie** ausgeführt wird. Ältere Datensätze werden gelöscht. Dies ist nützlich, wenn Sie die regelmäßige Ausführung der Aufgabe festlegen, da das Alter immer relativ zum Ausführungsdatum der Aufgabe berechnet wird. Ohne diese Funktion können Sie nur ein bestimmtes Datum für die ältesten Aufzeichnungen festlegen, die aufbewahrt werden sollen. Weitere Informationen finden Sie unter [Datenbereinigung der Verkaufshistorie planen](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Vertrieb und Marketing | Berichtsleistung von „Top 100“-Kunden verbessern | Diese Funktion verbessert die Leistung der **Top 100**-Kunden berichten, indem der Bericht immer für alle Kunden ausgeführt wird (was der beabsichtigte Verwendungszweck ist), anstatt benutzerdefinierte Abfragen zuzulassen. Wenn diese Funktion aktiviert ist, werden alle **Einzuschließende Aufzeichnungen**-Einstellungen sind im Berichtsdialog **Top 100** deaktiviert. |
| Lagerortverwaltung | Unterstützung der Skalierungseinheit für die Freigabe ausgehender Aufträge für den Lagerort | Wenn diese Funktion aktiviert ist, können ausgehende Aufträge vom Hub direkt an die Skalierungseinheit freigegeben werden, von wo aus die Aufträge erfüllt werden sollen. |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Diese Artikel beziehen sich nicht unbedingt auf die neuen Funktionen, die für diese Version hinzugefügt wurden, wie im vorherigen Abschnitt aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Verwaltung für technische Änderung | [Engineering-Attribute und Engineering-Attribut-Suche](../engineering-change-management/engineering-attributes-and-search.md) beschreibt nun, wie Engineering-Attribut-Vererbung funktioniert. |
| Produktprogrammplanung | [Masterplanung mit Bedarfsprognosen](../master-planning/planning-optimization/demand-forecast.md) und [Schlüssel zur Prognosereduzierung](../master-planning/reduction-keys.md) bieten jetzt weitere Informationen zum Arbeiten mit Reduktionsschlüsseln. |
| Produktprogrammplanung | [Sicherheitsbestandserfüllung für Artikel](../master-planning/safety-stock-replenishment.md) bietet jetzt weitere Informationen zur Verwendung von Minimum-/Maximum-Schlüsseln. |
| Produktprogrammplanung | [Bestandsprognosen](../master-planning/inventory-forecast.md) bietet jetzt weitere Informationen zum Zuweisen von Prognosen. |
| Produktprogrammplanung | [Beschaffungsplan](../master-planning/supply-schedule.md) |
| Lagerortverwaltung | [Globale Parameter für mobile Geräte](../warehousing/mobile-device-parameters.md) |
| Lagerortverwaltung | [Verankerung](../warehousing/anchoring.md) |
| Vertrieb und Marketing | Der Intercompany-Handel wird nun ausführlich beschrieben, beginnend mit [Intercompany-Handel einrichten](../sales-marketing/intercompany-trade-set-up.md) und verwandte Artikel. |
| Vertrieb und Marketing | [Verbesserungen an der Leistung der Verkaufshistorienbereinigung](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Lagerverwaltung | Die Dokumentation zur Inventarsichtbarkeit wurde erweitert und aktualisiert, beginnend mit [Übersicht über das Inventarsichtbarkeits-Add-In](../inventory/inventory-visibility.md) und verwandte Artikel. |
| Lagerortverwaltung | [Benutzerkonten für mobile Geräte](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattform-Updates für Finanz- und Betriebs-Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.23 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.23 der Finanz- und Betriebs-Apps (November 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.23 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910) an.

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2021wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

