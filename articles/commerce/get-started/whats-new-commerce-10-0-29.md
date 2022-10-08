---
title: Neuerungen oder Änderungen in Dynamics 365 Commerce 10.0.29. (Oktober 2022)
description: Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Microsoft Dynamics 365 Commerce 10.0.29 sind.
author: josaw1
ms.date: 09/29/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0629228516d688abf4dcd4280d1ad676f8f35331
ms.sourcegitcommit: ce4e56d798281258479432ad821287a1cc8e26bf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9601570"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10029-october-2022"></a>Neuerungen oder Änderungen in Dynamics 365 Commerce 10.0.29. (Oktober 2022)

[!include [banner](../includes/banner.md)]


In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Commerce Version 10.0.29 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1326 und ist im folgenden Zeitplan verfügbar:

- **Vorschauversion für Release:** August 2022
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** September 2022
- **Allgemeine Verfügbarkeit des Release (automatisches Update):** Oktober 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Artikels, um Funktionen einzubeziehen, die zum Build hinzugefügt wurden, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---------|------------------|----------------|--------------| 
| B2B | [Unterstützung für Kaufverträge über alle Commerce-Kanäle hinweg aktivieren](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Diese Funktion ermöglicht es Business-to-Business (B2B)-Verkäuferorganisationen, Kaufverträge in der Commerce headquarters zu verwenden, um vertragsbasierte Preise für ihre Käufer zu definieren. Wenn ein B2B-Käufer auf der E-Commerce-Website einkauft, wird die vertragsbasierte Preisgestaltung, die für die B2B-Käuferorganisation konfiguriert ist, automatisch auf die gesamte Produktfindung, den Kauf und das Bezahlerlebnis angewendet. | Funktionsverwaltung<p>*Unterstützung für Kaufverträgen über alle Commerce-Kanäle hinweg* |
| Customer Service | [Aktivieren Sie den Kundenservice mit Dynamics 365 Omnichannel for Customer Service](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | Ein erstklassiges Kundensupport-Erlebnis ist der Schlüssel, um Verbrauchern ein personalisiertes und angenehmes Handelserlebnis zu bieten. Derzeit gibt es mehrere Berührungspunkte für den Handel, z. B. physische Geschäfte, Online-Kanäle und soziale Kanäle. Verbraucher erwarten an all diesen Kontaktpunkten ein personalisiertes Support-Erlebnis. Diese Funktion hilft Ihnen, Warenkorbumwandlungen in Verkäufe zu steigern, die personalisierte Interaktion mit Verbrauchern zu steigern und den Kundenservice durch die Integration mit Dynamics 365 Omnichannel for Customer Service zu verbessern. | Vom Administrator/Ersteller aktiviert |
| E-Commerce | Unterstützung beim Produktvergleich im E-Commerce | Ermöglichen Sie Käufern, Produkte in einer Vielzahl von Kategorien zu vergleichen, damit sie die richtige Kaufentscheidung für sich selbst treffen können. Diese Funktion ist sowohl für Business-to-Consumer- (B2C) als auch für B2B-Sites verfügbar. | Site Builder | 
| Geschenkkarten | Unterstützung für Geschenkkartentabellen für den unternehmensübergreifenden Datenaustausch | Die Dynamics-Zentrale unterstützt die Möglichkeit, die unternehmensübergreifende gemeinsame Nutzung von Daten für bestimmte Tabellen in der Dynamics-Architektur zu ermöglichen. In dieser Funktion fügt Dynamics 365 Commerce Unterstützung für Geschenkkartentabellen für den unternehmensübergreifenden Datenaustausch hinzu. Daher können die Daten einer Geschenkkarte in einem Unternehmen jetzt auf ein anderes Unternehmen in der Umgebung dupliziert werden. Änderungen, die an der Tabelle der ursprünglichen Firmengeschenkkarten vorgenommen werden, werden an die duplizierte Firmengeschenkkartentabelle weitergegeben. | Entwickler |
| Globalisierung | [Commerce Lokalisierungsfunktionen für das neue Commerce SDK aktivieren](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-commerce-localization-features-new-commerce-sdk) | Die neue Funktion bietet die Möglichkeit, Commerce Lokalisierungsfunktionen von Commerce headquarters aus zu aktivieren, indem das Framework oder die Parameter der Funktionsverwaltung verwendet werden. Beispiele für die Steuerintegration sind jetzt im neuen Commerce SDK enthalten und unterstützen die unabhängige Paketerstellung. Diese Funktion ermöglicht auch die Einführung der Store Commerce-App durch globale Commerce-Kunden.<p><p>Diese Version enthält Commerce Lokalisierungsfunktionen und Beispiele für die Steuerintegration für [Österreich](../localizations/emea-aut-fi-sample.md), [die tschechische Republik](../localizations/emea-cze-fi-sample.md), [Frankreich](../localizations/emea-fra-cash-registers.md), [Deutschland](../localizations/emea-deu-fi-sample.md), [Italien](../localizations/emea-ita-fpi-sample.md), [Norwegen](../localizations/emea-nor-cash-registers.md) und [Polen](../localizations/emea-pol-fpi-sample.md). | Vom Administrator/Ersteller aktiviert |
| Offline | [POS-Offlinedatenbank-Komprimierung](../dev-itpro/implementation-considerations-offline.md#important-offline-features) | Diese neue Funktion reduziert die Größe von Offline-Datenbanken, indem sie eine automatische Indexkomprimierung außerhalb der Kanal-[Öffnungszeiten](../dev-itpro/store-hours.md) ermöglicht. | Funktionsverwaltung<p>*POS-Offlinedatenbank-Komprimierung* |
| Leistung | Entfernen Sie die RTS-Abhängigkeit für „Kunden bearbeiten“-Szenarien | Hohe Verfügbarkeit und hohe Leistung sind Standarderwartungen für Point-of-Sale (POS)- und E-Commerce-Kanäle. Um diese Erwartungen zu erfüllen, müssen Dynamics 365 Commerce Kanäle sich nicht mehr auf Echtzeitkommunikation mit der Handelszentrale verlassen, wenn Kundeninformationen bearbeitet werden. Die Möglichkeit, Kundeninformationen für asynchrone und nicht asynchrone Kunden asynchron zu bearbeiten, kann dazu beitragen, Echtzeitanrufe an die Commerce headquarters zu reduzieren. | Vom Administrator/Ersteller aktiviert |

## <a name="feature-state-changes-in-this-release"></a>Änderungen am Status der Funktionen in dieser Version

In der folgenden Tabelle sind Funktionen aufgeführt, die ab Version 10.0.29 obligatorisch oder standardmäßig aktiviert wurden. Alle diese Funktionen werden automatisch für Ihr System aktiviert, sobald Sie auf Version 10.0.29 aktualisieren. Obligatorische Funktionen können nicht ausgeschaltet werden, aber Funktionen, die standardmäßig aktiviert sind, können unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ausgeschaltet werden.

In der Tabelle sind auch Funktionen aufgeführt, die zuvor in der öffentlichen Vorschauversion enthalten waren, die aber in Version 10.0.29 allgemein verfügbar geworden sind. Diese Änderung weist darauf hin, dass die Funktionen jetzt für die Verwendung in Produktionsumgebungen empfohlen werden. Standardmäßig sind diese Funktionen ausgeschaltet, falls nicht anders eingestellt. Daher, wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktion | Titel | Neuer Featurezustand |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brasilien) Spezifische Commerce-Funktionalität für Brasilien | Standardmäßig aktiviert |
| RetailAdvancedGTETaxAdjustmentFeature | (Indien) Für Einzelhandelstransaktionen berechnete GST-Zeit in Retail POS auf Einzelhandelsauszüge anwenden | Standardmäßig aktiviert |
| RetailChronologicalInvoicePostingFeature_IT | (Italien) Buchung von Einzelhandelsrechnungen ohne chronologische Reihenfolge ermöglichen | Standardmäßig aktiviert |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Mexiko) Rabattanpassung im globalen CFDI für den Einzelhandel | Standardmäßig aktiviert |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Überschreibungen für technisches Profil der Steuerintegration | Standardmäßig aktiviert |
| RetailFiscalIntegrationConnectorLocationFeature | Direkte Steuerintegration über POS-Kassen | Standardmäßig aktiviert |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Lokaler Datenspeicher-Backup für Finanzverflechtung | Standardmäßig aktiviert |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Verschobene Registrierung von Dokumenten | Standardmäßig aktiviert |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | Status der Steuerregistrierung von POS-Kassen | Standardmäßig aktiviert |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (Indien) GST basierend auf der Rechnungsadresse für E-Commerce-Aufträge berechnen | Standardmäßig aktiviert |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Polen) Standardmäßiger Verkaufsdokumentstatus für Einzelhandelsrechnungen | Standardmäßig aktiviert |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Mexiko) Rundungsneuberechnung für Steuerbasisbeträge im globalen CFDI von Retail. | Standardmäßig aktiviert |
| RetailSupplementaryInvoiceFeature | Zusätzliche Rechnungen für Abholungstransaktionen aktivieren, die in Einzelhandelsgeschäften abgeschlossen wurden | Standardmäßig aktiviert |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Bestandspuffer und Lagerbestände aktivieren    |  Standardmäßig aktiviert|
|RetailInboundOutboundInventoryValidationFeature|   Überprüfung in eingehenden und ausgehenden POS-Bestandsvorgängen aktivieren   |   Standardmäßig aktiviert   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Erweiterte kanalseitige Lagerberechnungslogik für E-Commerce |   Standardmäßig aktiviert   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Bestandsregulierungen in der Verkaufsstelle   |  Standardmäßig aktiviert  |
| RetailMultiplePickupDeliveryModeFeature |  Unterstützung für mehrere Abholungslieferarten     |   Obligatorisch    |
|  RetailProductAvailabilityOptimizationFeature |   Optimierte Produktverfügbarkeitsberechnung  |  Obligatorisch |
|   RetailPricingDataManagerV2Feature   |   Leistung für Commerce-Preisgestaltungsmodul verbessern |   Obligatorisch |
|  RetailPricingPreventUnintendedRecalculationFeature   | Verhindert unerwünschte Preisberechnung für Handelsaufträge    |  Obligatorisch  |
| RetailTeamsIntegration    |   Microsoft Teams-Integration aktivieren| Obligatorisch   |  
| ConsumerEFDSyncProcessFeature_BR | (Brasilien) NFC-e-synchrone Verarbeitung | Standardmäßig aktiviert |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Unterstützung für interne und externe Connectors im Steuer-Integration-Framework | Obligatorisch |
| RetailTaxRegistrationIdEnableFeature_BR | (Brasilien) Suchen von Debitoren in Retail POS nach Steuernummern | Obligatorisch |
| RetailTaxRegistrationIdEnableFeature_IN | (Indien) Suchen von Debitoren in Retail POS nach Steuernummern | Obligatorisch |
| RetailTaxRegistrationIdEnableFeature_IT | (Italien) Verwaltung von Kundeninformationen in Retail POS | Obligatorisch |
| RetailTaxRegistrationIdEnableFeature_PL | (Polen) Verwaltung von Kundeninformationen in Retail POS | Obligatorisch |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (USt. im Einzelhandel, Indien) Gutschriften mit Verweisen auf ursprüngliche Rechnungen aktualisieren | Obligatorisch |
| RetailUserDefinedCertificateProfileFeature | Benutzerdefinierte Zertifikatprofile für Einzelhandelsgeschäfte | Obligatorisch |
  

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Microsoft Dynamics 365 Commerce 10.0.29 enthält Plattform-Updates. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.29 der Apps für Finanzen und Betrieb (Oktober 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates der Version 10.0.29 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c) an. 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2022wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-features"></a>Entfernte und veraltete Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beschreibt Funktionen, die für Commerce entfernt oder veraltet sind.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
