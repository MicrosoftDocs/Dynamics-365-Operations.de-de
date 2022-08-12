---
title: Häufig gestellte Fragen zu Commerce-Kataloge für B2B
description: In diesem Artikel finden Sie Antworten auf häufig gestellte Fragen zu Microsoft Dynamics 365 Commerce-Katalogen.
author: ashishmsft
ms.date: 07/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 68c648c5caf2667f413b236dc437fc2c74c40d07
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168984"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Häufig gestellte Fragen zu Commerce-Kataloge für B2B

[!include [banner](includes/banner.md)]

Dieser Artikel enthält Antworten auf häufig gestellte Fragen zu Microsoft Dynamics 365 Commerce [Business-to-business (B2B) Katalogen](catalogs-b2b-sites.md).

### <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Warum kann ich keine katalogspezifische Navigationshierarchie konfigurieren oder eine Option zum Zuordnen einer Kundenhierarchie sehen?

Stellen Sie sicher, dass die Funktion **Verwendung mehrerer Kataloge auf Einzelhandelskanälen aktivieren** im Arbeitsbereich der Commerce headquarters **Funktionsverwaltung** aktiviert ist und dass es sich bei Ihrer Umgebung um die Commerce-Version 10.0.27 oder eine neuere Version handelt. Stellen Sie sicher, dass Sie **B2B** unter **Katalogtyp** ausgewählt haben.

### <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Kann ich die katalogspezifische Hierarchie anzeigen und Kategorieseiten im Commerce Site Builder anreichern?

Ja, Commerce Site Builder-Benutzer, die Zugriff haben auf die **Produkte**-Seite im Site Builder können einen Katalog auswählen und die katalogspezifische Hierarchie anzeigen. Über die **Produkte**-Seite können Benutzer auch eine Kategorieseite für eine bestimmte Kategorie im Katalog anreichern. Weitere Informationen finden Sie unter [Reichern Sie eine Kategorieangebotsseite an](enrich-category-page.md). Wenn Sie eine katalogspezifische Anreicherung wünschen, empfehlen wir, dass Sie für diesen Katalog eine eindeutige und eindeutige Navigationshierarchie haben.

### <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Kann ein B2B-Käufer in einem einzigen Checkout aus mehreren Katalogen einkaufen?

Ja, Einkäufe in einem einzigen Checkout aus mehreren Katalogen sind erlaubt. B2B-Käufer können anhand der Kataloganzeige in der Warenkorbansicht feststellen, welche Artikel aus welchen Katalogen hinzugefügt wurden.

### <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Was ist das erwartete Verhalten, wenn ein B2B-Käufer denselben Artikel aus verschiedenen Katalogen kauft?

Obwohl ein bestimmter Benutzer zu einem bestimmten Zeitpunkt Zugriff auf mehrere Kataloge haben kann, wird erwartet, dass sich die Produkte in diesen Katalogen gegenseitig ausschließen. Mit anderen Worten, dasselbe Produkt sollte idealerweise nicht Teil von mehr als einem Katalog für einen bestimmten Benutzer sein.

Wenn jedoch eine Situation auftritt, in der dasselbe Produkt zu mehreren Katalogen gehört, behält das System mehrere Warenkorbpositionen für dieses Produkt bei. Für jeden Katalog wird es eine eigene Zeile geben. Dasselbe Produkt aus zwei verschiedenen Katalogen wird an der Kasse nicht zusammengeführt.

### <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Gibt es eine Überprüfung der Katalogverfügbarkeit, wenn ein B2B-Käufer einkauft?

Ja. Ein B2B-Käufer darf nur dann zur Kasse gehen, wenn alle Artikel im Einkaufswagen aus gültigen Katalogen stammen. Wenn Einkaufswagenartikel aus abgelaufenen oder zurückgezogenen Katalogen stammen, werden sie entfernt und der Benutzer wird benachrichtigt.

### <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Sind während des Einkaufserlebnisses Suche und Produktfindung (einschließlich verwandter und empfohlener Produktkollektionen) katalogspezifisch?

Ja. Sobald ein Benutzer einen bestimmten Katalog auswählt, wird die gesamte Shopping Journey katalogspezifisch. Diese Journey umfasst Produktfindungserfahrungen wie Suchvorschläge, Suchergebnisse, Kategorieergebnisse, Einschränkungen, Preise, Attribute und empfohlene Produkte (wie neue, meistverkaufte, trendige, häufig zusammen gekaufte und verwandte Produkte).

### <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Kann ein B2B-Käufer aus dem Standardsortiment (catalogID=0) einkaufen?

Nein, ein B2B-Käufer darf nicht aus dem Standardsortiment einkaufen. Dieses Sortiment ist nur für anonymes Surfen bestimmt. Wenn einem B2B-Käufer Katalogzuweisungen fehlen (ausstehende Aktualisierungen von seiner Verwaltung), kann er keine Kataloge sehen, aus denen er auswählen kann, und es ist keine Kategoriehierarchie sichtbar.

### <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Können Marketinginhalte für ein katalogspezifisches Produkt kuratiert werden?

Derzeit wird die Produktanreicherung nur auf der Ebene der Website und des Kanals unterstützt. Mit anderen Worten: Wenn ein Produkt angereichert ist und von mehreren Katalogen gemeinsam genutzt wird, wird die entsprechende angereicherte Produktdetailseite (PDP) für dieses Produkt in allen Katalogen für eine bestimmte Website auf dieselbe Weise dargestellt. 

### <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Ist Katalogunterstützung sowohl für B2B- als auch für Business-to-Consumer (B2C)-Onlinekanäle verfügbar?

Derzeit sind die Commerce-Kataloge nur für B2B-Online-Kanäle vorgesehen.

### <a name="a-new-customer-was-added-to-the-customer-hierarchy-or-a-new-hierarchy-was-associated-with-the-catalog-but-the-catalog-is-not-available-to-the-user-why"></a>Ein neuer Debitor wurde der Kundenhierarchie hinzugefügt oder eine neue Hierarchie wurde mit dem Katalog verknüpft, aber der Katalog ist für den Benutzer nicht verfügbar. Warum?

Stellen Sie sicher, dass Sie **1010** Aufträge ausgeführt haben, nachdem Sie den neuen Debitor mit einer bestehenden Kundenhierarchie verbunden haben und als Sie die neue Kundenhierarchie erstellt haben. Die mit der Kundenhierarchie verbundenen Kataloge werden erst nach erfolgreichem Abschluss des **1010** Auftrags sichtbar. Wenn der Katalog ebenfalls neu ist, stellen Sie sicher, dass Sie den Auftrag **1150** (Katalog) sowie die Aufträge **1010** ausgeführt haben. Wie bei jedem neuen Katalog sollten Sie etwas Zeit zulassen, damit die Daten mit dem Kanal und dem Suchindex synchronisiert werden können. Wenn ein Auftrag den Status „Angewandt“ hat, bedeutet dies, dass die Daten mit der Channel-Datenbank synchronisiert werden, aber es dauert noch eine Weile, bis die Daten mit dem Suchindex synchronisiert sind. 

### <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Können wir katalogspezifische Artikel für weiteren/ergänzenden Verkauf einrichten?

Derzeit wird nur die Funktionalität verwandter Produkte unterstützt. Für Callcenter sind jedoch Up-Selling- und Cross-Selling-Artikelkonfigurationen verfügbar.

Die folgenden Funktionen werden ebenfalls nur für Callcenter unterstützt:

- Katalogquellcodes
- Verwenden von Quellenkennungen, um Kosten und Rücklaufquoten zu verfolgen
- Katalogspezifische Bestell- und Artikelskripte
- Katalogseitenanalyse
- Kataloganforderungen
- Zahlungspläne
- Kostenlose Produkte basierend auf Quellcodes

### <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Können wir Katalogquellcodes für B2B-Bestellungen über das E-Commerce-Portal verwenden?

Nein Katalogquellcodes werden nur für Callcenter-Kanäle unterstützt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Commerce-Kataloge für B2B-Websites erstellen](catalogs-b2b-sites.md)

[Katalog-Picker-Modul](catalog-picker.md)

[Auswirkung der Erweiterbarkeit von Commerce-Katalogen auf B2B-Anpassungen](catalogs-b2b-sites-dev.md)
