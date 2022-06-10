---
title: FAQ zu Commerce-Katalogen für B2B
description: Dieser Artikel gibt Antwort auf häufig gestellte Fragen zur Microsoft Dynamics 365 Commerce-Katalogen.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 5bdc7dfcb0e48aa85db2db4d178c5bf62ea0411b
ms.sourcegitcommit: bca0cb730307948368a9aabe322cf963688ed8b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782861"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>FAQ zu Commerce-Katalogen für B2B

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieses Thema enthält Antworten auf häufig gestellte Fragen zu Microsoft Dynamics 365 Commerce [Business-to-Business (B2B)-Katalogen](catalogs-b2b-sites.md).

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Warum kann ich keine katalogspezifische Navigationshierarchie konfigurieren oder eine Option zum Zuordnen einer Kundenhierarchie sehen?

Stellen Sie sicher, dass die Funktion **Ermöglicht die Verwendung von mehreren Katalogen für Kanäle im Einzelhandel** im **Funktionsverwaltung**-Arbeitsbereich in der Commerce-Zentralverwaltung aktiviert ist. Stellen Sie außerdem sicher, dass Ihre Umgebung die Commerce-Version 10.0.27 oder höher verwendet.

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Kann ich die katalogspezifische Hierarchie anzeigen und Kategorieseiten im Commerce Site Builder anreichern?

Ja, Commerce Site Builder-Benutzer, die Zugriff haben auf die **Produkte**-Seite im Site Builder können einen Katalog auswählen und die katalogspezifische Hierarchie anzeigen. Über die **Produkte**-Seite können Benutzer auch eine Kategorieseite für eine bestimmte Kategorie im Katalog anreichern. Weitere Informationen finden Sie unter [Reichern Sie eine Kategorieangebotsseite an](enrich-category-page.md). Wenn Sie eine katalogspezifische Anreicherung wünschen, empfehlen wir, dass Sie für diesen Katalog eine eindeutige und eindeutige Navigationshierarchie haben.

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Kann ein B2B-Käufer in einem einzigen Checkout aus mehreren Katalogen einkaufen?

Ja, Einkäufe in einem einzigen Checkout aus mehreren Katalogen sind erlaubt. B2B-Käufer können anhand der Kataloganzeige in der Warenkorbansicht feststellen, welche Artikel aus welchen Katalogen hinzugefügt wurden.

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Was ist das erwartete Verhalten, wenn ein B2B-Käufer denselben Artikel aus verschiedenen Katalogen kauft?

Obwohl ein bestimmter Benutzer zu einem bestimmten Zeitpunkt Zugriff auf mehrere Kataloge haben kann, wird erwartet, dass sich die Produkte in diesen Katalogen gegenseitig ausschließen. Mit anderen Worten, dasselbe Produkt sollte idealerweise nicht Teil von mehr als einem Katalog für einen bestimmten Benutzer sein.

Wenn jedoch eine Situation auftritt, in der dasselbe Produkt zu mehreren Katalogen gehört, behält das System mehrere Warenkorbpositionen für dieses Produkt bei. Für jeden Katalog wird es eine eigene Zeile geben. Dasselbe Produkt aus zwei verschiedenen Katalogen wird an der Kasse nicht zusammengeführt.

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Gibt es eine Überprüfung der Katalogverfügbarkeit, wenn ein B2B-Käufer einkauft?

Ja. Ein B2B-Käufer darf nur dann zur Kasse gehen, wenn alle Artikel im Einkaufswagen aus gültigen Katalogen stammen. Wenn Einkaufswagenartikel aus abgelaufenen oder zurückgezogenen Katalogen stammen, werden sie entfernt und der Benutzer wird benachrichtigt.

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Sind während des Einkaufserlebnisses Suche und Produktfindung (einschließlich verwandter und empfohlener Produktkollektionen) katalogspezifisch?

Ja. Sobald ein Benutzer einen bestimmten Katalog auswählt, wird die gesamte Shopping Journey katalogspezifisch. Diese Journey umfasst Produktfindungserfahrungen wie Suchvorschläge, Suchergebnisse, Kategorieergebnisse, Einschränkungen, Preise, Attribute und empfohlene Produkte (wie neue, meistverkaufte, trendige, häufig zusammen gekaufte und verwandte Produkte).

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Kann ein B2B-Käufer aus dem Standardsortiment (catalogID=0) einkaufen?

Nein, ein B2B-Käufer darf nicht aus dem Standardsortiment einkaufen. Dieses Sortiment ist nur für anonymes Surfen bestimmt. Wenn einem B2B-Käufer Katalogzuweisungen fehlen (ausstehende Aktualisierungen von seiner Verwaltung), kann er keine Kataloge sehen, aus denen er auswählen kann, und es ist keine Kategoriehierarchie sichtbar.

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Können Marketinginhalte für ein katalogspezifisches Produkt kuratiert werden?

Derzeit wird die Produktanreicherung nur auf Website- und Kanalebene unterstützt. Mit anderen Worten, wenn ein Produkt angereichert wird, wird es von mehreren Katalogen gemeinsam genutzt, und die entsprechende Produktdetailseite (PDP) für dieses Produkt wird in allen Katalogen für eine bestimmte Website auf die gleiche Weise gerendert.

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Ist Katalogunterstützung sowohl für B2B- als auch für Business-to-Consumer (B2C)-Onlinekanäle verfügbar?

Derzeit sind Commerce-Kataloge nur für B2B-Kanäle vorgesehen.

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Können wir katalogspezifische Artikel für weiteren/ergänzenden Verkauf einrichten?

Derzeit wird nur die Funktionalität verwandter Produkte unterstützt. Für Callcenter sind jedoch Up-Selling- und Cross-Selling-Artikelkonfigurationen verfügbar.

Die folgenden Funktionen werden ebenfalls nur für Callcenter unterstützt:

- Katalogquellcodes
- Verwenden von Quellenkennungen, um Kosten und Rücklaufquoten zu verfolgen
- Katalogspezifische Bestell- und Artikelskripte
- Katalogseitenanalyse
- Kataloganforderungen
- Zahlungspläne
- Kostenlose Produkte basierend auf Quellcodes

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Können wir Katalogquellcodes für B2B-Bestellungen über das E-Commerce-Portal verwenden?

Nein Katalogquellcodes werden nur für Callcenter-Kanäle unterstützt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Commerce-Kataloge für B2B-Websites erstellen](catalogs-b2b-sites.md)

[Auswirkung der Erweiterbarkeit von Commerce-Katalogen auf B2B-Anpassungen](catalogs-b2b-sites-dev.md)
