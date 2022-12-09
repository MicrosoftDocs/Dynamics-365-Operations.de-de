---
title: Leistungsspektrum der Store Commerce-App
description: In diesem Artikel werden die Funktionen beschrieben, die in der Store Commerce-App für Microsoft Dynamics 365 Commerce zur Verfügung stehen.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788511"
---
# <a name="store-commerce-app-capabilities"></a>Leistungsspektrum der Store Commerce-App

[!include [banner](includes/banner.md)]

Die Store Commerce-App ist die modernde Verkaufsstellenumgebung (POS) für Microsoft Dynamics 365 Commerce. Sie ermöglicht Unternehmen, Transaktionen im Geschäft abzuwickeln und Backoffice-Vorgänge wie Inventarisierung und Auftragsverarbeitung zu verwalten. Die App ermöglicht es Unternehmen auch, Kundenbeziehungen mit Loyalität und Kundenaktionen zu steuern. 

Die von Commerce Scale Unit (CSU) unterstützte Store Commerce-App bietet eine vollständige Omnichannel-Lösung. Ein Kunde kann beispielsweise ein Produkt online kaufen und in einem Geschäft in der Nähe abholen und so seinen Einkauf über alle Kanäle hinweg fortsetzen, ohne Daten zu verlieren. 

Dieser Artikel bietet eine Übersicht über die Fähigkeiten der Store Commerce-App.

## <a name="platform"></a>Plattform

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Omnichannel | Dynamics 365 Commerce basiert auf einer umfangreichen Omnichannel-Lösung, die Backoffice-, In-Store-, Callcenter- und digitale Umgebungen vereint. | [Übersicht](index.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Monitorloser Commerce | Die Commerce Scale Unit hostet das monitorlose Commerce-Modul. Das monitorlose Commerce-Modul dient als zentraler Punkt für die gesamte Commerce-Geschäftslogik und unterstützt eine vollständige Omnichannel-Lösung. | <p>[Übersicht über die Architektur](commerce-architecture.md)</p><p>[Monitorlose Architektur](dev-itpro/retail-server-architecture.md)</p> | [Fachvortrag](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | Commerce headquarters bietet Backoffice-Fähigkeiten, die die Konfiguration von Produkten, Mitarbeitern, Geschäftsprozessen, Preisen und anderen für das Unternehmen erforderlichen Funktionen ermöglichen. | [Übersicht über die Architektur](commerce-architecture.md) | |
| Verkaufsstelle (POS) | Die Store Commerce-App ist die POS-Umgebung für Dynamics 365 Commerce. Sie bietet funktionsreiche und umfassende POS-Funktionen, die Vertriebsmitarbeitern, Kassierern und Managern helfen, einen hervorragenden Kundenservice zu bieten. Darüber hinaus bietet es Einzelhändlern mehrere Bereitstellungsoptionen, trägt zur Leistungssteigerung bei und bietet ein verbessertes Application Lifecycle Management (ALM). | [Store Commerce-App](dev-itpro/store-commerce.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[-Video](https://youtu.be/7B332XH_zfs)</p><p>[Migration von MPOS zu Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Cloudbereitstellung | Zur Lastverteilung und geografischen Nähe können mehrere Instanzen von Commerce Scale Units bereitgestellt werden. | [Cloudbereitstellung](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Lokale Bereitstellung | Mithilfe einer lokalen Geschäftsdatenbereitstellung können Commerce-Kunden mehr Verantwortung für und Verwaltung von Dynamics 365-Umgebung erlangen. | [On-Premises-Bereitstellung](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Geräteverwaltung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Mehrere Formfaktoren | Die Store Commerce-App wird auf mehreren Geräteformfaktoren wie PCs, Tablets und mobilen Geräten unterstützt. Die dynamische Benutzeroberfläche (UI) ermöglicht eine automatische Größenänderung des Layouts und die Anpassung an die Bildschirmgröße. | [Visuelle Konfigurationen](pos-screen-layouts.md) |  |
| Plattformübergreifend | Die Store Commerce-App wird auf Web-, Windows-, iOS- und Android-Plattformen unterstützt. | [Plattformen](dev-itpro/hybridapp.md) | |
| Branding | Mit dem Bildschirm-Designer können Sie Bildschirmlayouts an Ihre Geschäftsanforderungen anpassen. Darüber hinaus können Designs, Layouts, Farben und Bilder basierend auf Mitarbeiterrollen erstellt und dann im Interesse der Markenkonsistenz und Benutzerfreundlichkeit von allen Benutzern gemeinsam genutzt werden. | [Visuelle Konfigurationen](pos-screen-layouts.md) | [-Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topologie | Je nach der Netzwerkverfügbarkeit werden verschiedene In-Store-Topologien unterstützt. | <p>[Topologie](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infografik](dev-itpro/retail-in-store-topology.md)</p> | |
| Verwaltung mehrerer Geräte | Mehrere Geräte in den Filialen können einfach von Commerce headquarters aus verwaltet werden. | [Aktivierung](set-up-activation-accounts-validate-devices-hq.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Mitarbeiter-Verwaltung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Anmeldung | Jeder Filialmitarbeiter kann eine eigene Anmeldung haben. Zu den Anmeldetypen gehören Benutzername, Barcode, Magnetstreifenleser (MSR), Biometrie und Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Erweiterte Anmeldung](extended-logon.md)</p> | |
| Berechtigungen | Für Mitarbeiter werden verschiedene Berechtigungsstufen unterstützt, z. B. die Berechtigung zum Erstellen von Aufträgen und die Berechtigung zum Bearbeiten von Aufträgen. | [Berechtigungen](tasks/create-pos-permission-groups.md) | |
| Zeit- und Anwesenheitsverwaltung | Die Anwesenheit kann mithilfe der Stechuhrfunktion verwaltet werden. Anwesenheitsdaten können mithilfe der Dynamics 365 Human Resources App in die Gehaltsabrechnung einfließen. | [Zeitverwaltung](retail-time-attendance.md) | |
| Verkaufsprovision | Der Verkauf, die vom Verkäufer erfasst werden, um Provisionen oder andere Anreize zu berechnen. | [Provision](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Verkaufsförderung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Sortimentsverwaltung | Merchandising-Manager können Produkte so sortieren, dass sie in einem bestimmten Kanal und während eines bestimmten Zeitraums zum Verkauf stehen. | [Sortimente](assortments.md) | |
| Kataloge | Merchandising-Manager können Kataloge verwalten, um die Produkte, die Sie anbieten möchten, mit katalogspezifischen Preisen auszuweisen. | [Kataloge](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Produkt- und Kategorieverwaltung | In Commerce headquarters können Merchandising-Manager Produkte mit Varianten, Attributen, einer Maßeinheit usw. erstellen. Sie können auch eine Kategoriehierarchie definieren, mit der Produkte organisiert werden. | [Produkt](retail-hierarchies.md) | |
| Bündel | Merchandising-Manager können Produkte so gruppieren, dass sie als Paket oder Kit verkauft werden. | [Bausätze](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Infocodes | Verwenden Sie Infocodes, um das Kassenpersonal aufzufordern, Informationen zu unterschiedlichen Aktionen am POS, wie Artikelverkauf, Artikelrückgabe oder Debitorenauswahl einzugeben. | [Infocodes](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Verknüpfte Artikel | Verwenden Sie verknüpfte Artikel, um Upsell-Möglichkeiten für Produkte zu nutzen, wenn ein Artikel zur Transaktion hinzugefügt wird. | [Verknüpfte Artikel](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garantien | Garantieverlängerungen können zusammen mit Produkten verkauft werden. | [Garantie](extended-warranty.md) | |
| Beschriftungsdruck | Beschriftungen mit Produktinformationen wie Chargennummer, Seriennummer und Ablaufdatum können erstellt werden. | [Beschriftungsdruck](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Assistierter Verkauf

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Produktsuche | Browsen Sie Produkte nach Kategorie. | [Produkthierarchie](retail-hierarchies.md) | |
| Produktsuche | Suchen Sie Produkte nach Namen und verfeinern Sie die Suche anhand von Produktattributen wie Marke, Preis und Material. Diese Funktion wird von der Azure Cognitive Search unterstützt. | [Cloudbasierte Suche](cloud-powered-search-overview.md) | |
| Seite Produktdetails | Umfangreiche Produktdetailseiten können Bilder, eine Beschreibung, Produktattribute und empfohlene Produkte enthalten. Empfehlungen werden vom Dienst „Empfehlungen“ unterstützt. | | |
| Produktvergleich | Vergleichen Sie mehrere Produkte und helfen Sie Kunden, eines auszuwählen und einer Transaktion hinzuzufügen. | | |
| Endloses Regal | Suchen Sie ganz einfach in anderen Geschäften nach Beständen und erstellen Sie Aufträge. | [Bestandsuche](pos-inventory-lookup-operation.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Empfehlungen | Nutzen Sie den Empfehlungen-Dienst für das Upselling und Cross-Selling von Produkten. Dieser Dienst verwendet eine patentierte Technologie, um Empfehlungen basierend auf Kauftrends und Merkmalen vorzuschlagen, wie neu eingetroffene Produkte, ähnlich aussehende Produkte und Bestseller. Diese Empfehlungen sind auf den Produktdetailseiten, der Seite **Details zum Debitor** und der Seite **Transaktionen** verfügbar. | [Empfehlungen](product-recommendations.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Kundenbeziehung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Kundenverwaltung | Erstellen, bearbeiten und verwalten Sie Debitorenkonten. Debitorenkonten können im asynchronen Modus verwaltet werden, um eine Verarbeitung in Echtzeit zu vermeiden. | [Management](customer-mgmt-stores.md) | |
| Debitorattribute | Das Framework für Debitorattribute ermöglicht die Erfassung zusätzlicher kundenbezogener Daten basierend auf Geschäftsanforderungen. | [Attribute](dev-itpro/customer-attributes.md) | |
| Seite „Details zum Debitor“ | Eine reichhaltige Seite „Details zum Debitor“ bietet eine Omnichannel-Ansicht der Interaktionen des Debitors über alle Kanäle hinweg. Diese Interaktionen umfassen Einkäufe, Wunschlisten und Treuepunkte. | | |
| Cloudbasierte Debitorensuche | Suchen Sie Kunden nach Name, Telefonnummer, E-Mail-Adresse, Kundenkarte, Adresse usw. | [Cloudbasierte Suche](pos-search-improvements.md#customer-search) | |
| Treue und Prämien | Debitoren können an Treueprogrammen teilnehmen und kanalübergreifend Treuepunkte sammeln und einlösen. | [Kundentreue](set-up-customer-loyalty-program.md) | [-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Kundenaktionen | Verwalten Sie wichtige Kunden mithilfe eines Kundenbuchs und verfolgen Sie Aktivitäten und Notizen im Kundenprofil. Mit der Dynamics 365 Customer Insights-Integration erhalten die Mitarbeiter der Filialen Hinweise auf die nächstbeste Aktion für jeden Kunden. | [Kundenaktionen](clienteling-overview.md#activities-and-notes) | [-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Preise und Rabatte

| Funktionen | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Handelsvereinbarungen | Preismanager können Handelsvereinbarungen verwenden, um Sonderpreise zu definieren, die auf langfristigen Vereinbarungen mit bestimmten Debitoren basieren. | [Preisgestaltung](price-management.md)| [-Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Verkaufsverträge | Preismanager können Verkaufsvereinbarungen verwenden, um vertragsbasierte Preise in gewerblichen Business-to-Business-(B2B-)-Szenarien zu definieren. | [Preisgestaltung](price-management.md) | |
| Preisregulierungen | Preismanager können die Preisregulierungsfunktion verwenden, um Preisabschläge für seine Produkte im Zeitverlauf zu erstellen, nachzuverfolgen und zu verwalten. | [Preisregulierungen](price-adjustments-discounts.md) | |
| Rabatte | Preismanager können verschiedene Arten von Rabatten einrichten, um eine Vielzahl von Promotionen durchzuführen. Zu diesen Rabatten zählen einfache Rabatte, Mengenrabatte, Schwellenwertrabatte, Angebots-Sortimentrabatte, zahlungsmittelbasierte Rabatte und Versandrabatte, | [Rabatte](retail-discounts-overview.md) | |
| Gutscheine | Preismanager können Gutscheincodes oder Strichcodes einrichten, sie mit Rabatten verknüpfen und an Debitoren weitergeben. Vertriebsmitarbeiter können Gutscheine zu Verkaufstransaktionen hinzufügen oder entfernen. | [Gutscheine](coupons.md) | |
| Preisgruppen | Preismanager können die Preisgruppenfunktion verwenden, um kontextbezogene Preise basierend auf Kanälen, Katalogen, Zugehörigkeiten oder Treueprogrammen festzulegen. | [Preisgestaltung](price-management.md) | |
| Verfügbare Promotions | Vertriebsmitarbeiter können leicht verfügbare Promotions für Produkte im Geschäft, Produkte, die einer Transaktion hinzugefügt wurden, usw. nachschlagen. | [Preisberechnungsfunktionen](pos-pricing-functions.md) | |
| Preisüberprüfung | Vertriebsmitarbeiter können schnell die aktiven Verkaufspreise von Produkten im Geschäft überprüfen. | [Preisberechnungsfunktionen](pos-pricing-functions.md) | |
| Preisüberschreibungen | Vertriebsmitarbeiter mit den erforderlichen Berechtigungen können vom System konfigurierte oder berechnete Preise überschreiben. | [Preisberechnungsfunktionen](pos-pricing-functions.md) | |
| Manuelle Rabatte | Vertriebsmitarbeiter mit den erforderlichen Berechtigungen können manuelle Rabatte auf Verkaufstransaktionen oder Verkaufspositionen anwenden. | [Preisberechnungsfunktionen](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektronische Zahlungen

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Soll und Haben | Die Store Commerce-App unterstützt die wichtigsten Kredit- und Debitkartenzahlungen über das Adyen-Zahlungsgateway und die Auftragserfüllung über PayPal. Das Zahlungs-SDK ermöglicht externe Gateway-Verbindungen, die von Integrationen unabhängiger Softwareanbieter (ISV) unterstützt werden. | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Zahlungen](payment-methods.md)</p> | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Unterstützung digitaler Wallets | Die Store Commerce-App unterstützt Zahlungen über digitale Wallet-Zahlungsmethoden, die keine BIN-Bereiche (Bankidentifikationsnummer) verwenden, wie dies bei herkömmlichen Kredit- und Debitkarten der Fall ist. Zahlungsmethoden können digitalen Wallet-Zahlungen wie Adyen zugeordnet werden. | [Brieftasche](wallets.md) | |
| Geschenkkartenunterstützung | Bankidentifikationsnummer Dynamics 365-Geschenkkarten, Stored Value Solutions (SVS) und Givex-Geschenkkarten. Geschenkgutscheine können mit einem Auftrag gekauft und eingelöst werden. | [Geschenkkarten](dev-itpro/gift-card.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Betrugsschutz | Dynamics 365 Fraud Protection hilft Ihnen, betrügerische Aktivitäten zu verhindern und Stellen zu identifizieren, an denen Betrug unbemerkt bleiben könnte. | [Fraud Protection](dev-itpro/dfp.md) | [-Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Steuern und Gebühren

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Steuern | Die Store Commerce-App unterstützt verschiedene Varianten von indirekten Steuern, wie etwa Ausgangssteuer, Mehrwertsteuer (MwSt.), Steuern auf Waren- und Dienstleistungen (GST), einheitenbasierte Gebühren und Quellensteuer. | [Steuern](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Gebühren | Gebühren können auf Positionsebene, Header-Ebene, als automatische Gebühren, nach Kanal usw. konfiguriert werden. | [Belastungen](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Auftragsverarbeitung und -erfüllung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Auftragserstellung | Ein Auftrag kann zum Versand oder zur Abholung in einem Geschäft in der Nähe erstellt werden. Für die Abholung können Zeitfenster bereitgestellt werden. | [Übersicht](customer-orders-overview.md) | |
| Auftragsänderung | Ein Auftrag kann geändert, zurückgegeben, storniert usw. werden. | <p>[Stornieren](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Rücklieferungen](pos-returns.md)</p> | |
| Suche | Suchen und filtern Sie Aufträge anhand auftragsspezifischer Informationen. | [Suche](enhancedorderrecall.md) | |
| Auftragsattribute | Das Framework für Auftragsattribute ermöglicht die Erfassung auftragsbezogener Informationen basierend auf Geschäftsanforderungen. | [Attribute](dev-itpro/order-attributes.md) | |
| Direktlieferung | Artikel können für die direkte Lieferung durch einen Anbieter an eine Debitorenadresse markiert werden. Eine Direktlieferung wird auch als Dropshipping bezeichnet. | [Direktlieferung](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Angebot | Filialmitarbeiter können Angebote für Debitoren erstellen und einen Sonderpreis, manuelle Rabatte und ein Angebotsgültigkeitsdatum angeben. | [Angebot](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Auftragserfüllung | Geschäfte können Bestellungen kommissionieren, verpacken und versenden. Den versandfertigen Paketen kann ein Lieferschein beigefügt werden. | [Auftragserfüllung](order-fulfillment-overview.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[-Video](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Verteilte Auftragsverwaltung | Die Store Commerce-App unterstützt eine intelligente Optimierung der Auftragserfüllung, bei der Geschäftsstrategien basierend auf der Art des Geschäfts, der Art des Debitors, des Ursprungs eines Auftrags und der Liefermethode eines Auftrags konfiguriert werden können. | [DOM](dom.md) | [-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Lagerverwaltung

| Funktionen | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Käuferübertragung | Optimieren Sie die Verteilung des verfügbaren Bestands von einem Verteilerzentrum auf mehrere Filialen oder Lagerorte. | [Käuferübertragung](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Crossdocking | Optimieren Sie die Verteilung des Bestands bei eingehenden Aufträgen auf mehrere Filialen oder Lagerorte. | [Crossdocking](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Eingehender Bestand | Nehmen Sie Bestände von einem Anbieter über eine Bestellung oder von einem anderen Lagerort über einen Umlagerungsauftrag entgegen. Erstellen Sie eine eingehende Bestellung oder eine Aufforderung für einen Umlagerungsauftrag. | [Zugang](pos-inbound-inventory-operation.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Ausgehender Bestand | Versenden Sie Bestand über einen Umlagerungsauftrag an einen anderen Lagerort und erstellen Sie eine Anforderung für einen ausgehenden Umlagerungsauftrag. | [Ausgehend](pos-outbound-inventory-operation.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Bestandsuche | Überprüfen Sie den Lagerbestand auf Produkte in allen Filialen und Lagerorten und prüfen Sie den ATP-Bestand (verfügbar für Zusage) für zukünftige Daten. | [Bestandsuche](pos-inventory-lookup-operation.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Lagerregulierung | Passen Sie im Lagerort eines Geschäfts ein- oder ausgehenden Bestand an, um bestimmte Geschäftsanforderungen zu erfüllen, ohne einen Verkauf, eine Quittung oder eine erneute Zählung zu verwenden. | [Lagerregulierung](work-with-store-inventory.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Bestandsmengen | Zählen Sie den physischen Bestand und passen Sie den im Buchhaltungssystem erfassten Bestand entsprechend an. | [Inventur](work-with-store-inventory.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Bestandsbewegungen | Verschieben Sie Bestände zwischen Standorten in einem Geschäft. | [Bewegung](work-with-store-inventory.md) | <p>[Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[-Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Finanzdaten

| Funktionen | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Zahlungsmanagement | Die Store Commerce-App unterstützt die Verwaltung von Bargeld und anderen festgelegten Zahlungsmitteln im Geschäft. Darüber hinaus kann die Schichtabstimmung im Geschäft für erweiterte Funktionen zur Bargeldverwaltung aktiviert werden. | [Bargeld](cash-mgmt.md) | |
| Finanzaufstellungen und -abstimmungen | Bar- und Buchungsvorgängen für ein Geschäft werden in Commerce headquarters durch die Aufstellungsbuchungsprozesse erfasst. | [Aufstellungen](retail-statements.md) | |
| Einnahmen- und Ausgabenbuchungen | Verarbeiten Sie Handkassenbuchungen im Geschäft und zeichnen Sie Einnahmen auf, die nicht auf herkömmliche Weise erzielt werden, z. B. Fundgeld, der Anteil der Einnahmen eines Cafés in Ihrer Lobby und Teppichreinigungsdienste. | [Aufstellungen](retail-statements.md) | |
| Rechnungszahlungen | Erfassen Sie Zahlungen gegen Rechnungen. | [Rechnung](payinvoice.md) | |

## <a name="employee-productivity"></a>Mitarbeiterproduktivität

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Aufgabenverwaltung | Erstellen Sie Aufgabenlisten und Aufgaben und weisen Sie sie Geschäften und Mitarbeitern zu. Verfolgen Sie den Status von Aufgaben in allen Geschäften. Nahtlose Integration mit Microsoft Teams steht zur Verfügung. | <p>[Aufgabenverwaltung](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [-Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Hardware und Peripheriegeräte

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Peripheriegeräte verbinden | Verbinden Sie Peripheriegeräte wie Drucker, Kassenladen, Scanner oder Zahlungsgeräte mit einem POS-Terminal. | [Peripheriegeräte](retail-peripherals-overview.md) ||
| Peripheriegeräte freigeben | Belegdrucker, Kassenschubladen und Zahlungsgeräte können von vielen Terminals gemeinsam genutzt werden, indem sie an eine gemeinsame Hardwarestation angeschlossen werden. | <p>[Hardwarestation](retail-peripherals-overview.md) ||
| POS- und Peripheriegerätesimulator | Der Peripheriegerätesimulator unterstützt das Testen von Szenarien, die normalerweise physische POS-Peripheriegeräte erfordern. Dazu gehört ein POS-Simulator, mit dem die Kompatibilität der physischen Peripheriegeräte ohne Bereitstellung an den POS-Client getestet werden kann. | [Simulator](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Eingänge

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Belege drucken | Belege verschiedener Art, z. B. Verkaufsbelege, Kreditkartenbelege, Geschenkbelege und Rechnungen, können standardmäßig oder nach Bestätigung durch den Kassierer an der Kasse gedruckt werden. Sie können auch aus der Erfassung nachgedruckt werden. | [Es wird gedruckt](receipt-templates-printing.md) | |
| E-Mail-Bons | Belege können vom POS aus per E-Mail versendet werden, nachdem die Bezahlung abgeschlossen ist. | [E-Mail](email-receipts.md) | |
| Belege gestalten | Kassenbons können angepasst werden, sodass sie Daten und Layouts anzeigen, die für den Einzelhändler und Transaktionstyp geeignet sind. Belege können auch so erweitert werden, dass sie benutzerdefinierte Daten enthalten, die vom Einzelhändler benötigt werden. | [Entwurf](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Offline-Unterstützung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Nahtlos offline | Dank nahtlosem Offline-Zugriff können Sie auch dann weiter Transaktionen durchführen, wenn die Internetverbindung eingeschränkt oder nicht verfügbar ist. Der Datenausschluss hilft Ihnen, die Datengröße der Offline-Datenbanken zu reduzieren und die Leistung zu maximieren. | [Offline](pos-operations.md) | |
| Leistungsbasiertes Umschalten | Wechseln Sie in den Offlinemodus, wenn eine Leistungsminderung festgestellt wird. | [Offline](dev-itpro/implementation-considerations-offline.md) | [-Video](https://youtu.be/sQU-2pgHToI) |
| Offline-Dashboard | Das Dashboard **Offlinestatus** zeigt den Offlinestatus, Fehler und Details der Daten für jedes Gerät. Daher ist es einfach, den Status vieler Geräte zu verwalten. | [Offline](dev-itpro/implementation-considerations-offline.md) | [-Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Erweiterbarkeit

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Commerce Headquarters | Lösungen von Commerce headquarters können durch Hinzufügen oder Ändern von Geschäftsprozessen angepasst werden. Commerce headquarters unterstützt die Verwendung von Metadaten und ein codegesteuertes Erweiterungsmodell, um benutzerdefinierte Funktionen hinzuzufügen. Dies lässt sich einfach in externe Lösungen integrieren. | [Übersicht](dev-itpro/extend-customer-cdx-package.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Monitorloser Commerce | Das erweiterbare Omnichannel-API-Framework kann zum Anpassen und Hinzufügen von Geschäftslogik verwendet werden. APIs mit Anforderungshandlern und Vor-Trigger- und Nach-Trigger-Erweiterungsmustern. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Das Commerce SDK enthält den Code, Codebeispiele, Vorlagen und Tools, die zum Erweitern oder Anpassen der Dynamics 365 Commerce Funktionalität erforderlich sind. Das SDK wird je nach Erweiterungskomponenten in verschiedenen Repositorys (Repos) in GitHub veröffentlicht. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Verkaufsstelle | Die Store Commerce-App kann mithilfe der POS-Erweiterungsfunktion des Commerce SDK unabhängig erweitert werden. Das Framework unterstützt die Anpassung der Benutzererfahrung (UX), der Workflows und der Geschäftslogik. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Fachvortrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Berichterstattung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Umsatzberichte | Verkaufsberichte nach Personal, Kasse, Zahlungsart, Rückgaben, Produkt usw. stehen Filialleitern zur Verfügung. Manager können diese Berichte anzeigen und verwenden, um Provisionen zuzuweisen und Produkttrends zu identifizieren. | | |

## <a name="diagnostics"></a>Diagnose

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Betriebliche Erkenntnisse | Vom Geschäft zusammengestellt Zuverlässigkeits- und Leistungskennzahlen zum Dienstzustand sind im Application Insights Abonnement des Debitors verfügbar. Es stehen erweitere Warn- und Überwachungsfunktionen zur Verfügung. | | |
| Systemdiagnose | Die Verfügbarkeit von Peripheriegeräten, die mit einem POS verbunden sind, kann durch Ausführen der Statusprüfung überprüft werden. Einzelne Peripheriegeräteprobleme können dann behoben und verifiziert werden. | [Systemdiagnose](pos-healthcheck.md) | [-Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalisierung

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Unterstützung für mehrere Märkte | Marktspezifische Funktionen wie Steuerintegration, GST, erweiterte Rechnungsstellung und Vorauszahlungen werden standardmäßig unterstützt. Diese Funktion deckt mehrere Märkte in Europa, Nord-, Mittel- und Südamerika, Russland, Asien, Saudi-Arabien usw. ab. | [Globalisierung](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Compliance

| Fähigkeit | Description | Dokumentation | Ergänzende Inhalte |
|---|---|---|---|
| Microsoft-Standards | Die Store Commerce-App erfüllt die Microsoft-Standards für Sicherheit, Datenschutz, Barrierefreiheit, die Datenschutz-Grundverordnung (DSGVO), die Datengrenze der Europäischen Union (EU) usw. | | |

