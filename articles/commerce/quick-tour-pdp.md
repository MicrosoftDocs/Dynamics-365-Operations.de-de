---
title: Übersicht der Produktdetailseiten
description: Dieses Thema bietet eine Übersicht über Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697864"
---
# <a name="overview-of-product-details-pages"></a>Übersicht der Produktdetailseiten

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Übersicht

Eine PDP bietet detaillierte Informationen zu einem Produkt und ermöglicht es Kunden, Produktoptionen wie Größe, Stil und Farbe auszuwählen. Eine PDP sollte alle Produktinformationen enthalten, die ein Kunde benötigt, um eine Kaufentscheidung zu treffen.

Die folgende Abbildung zeigt ein Beispiel für eine PDP.

![Beispiel einer Produktdetailseite](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Kopf- und Fußzeilenmodule

Oben in der PDP befindet sich eine Kopfzeile mit allen Produktkategorien und anderen Seiten, die Kunden auf Wunsch des Einzelhändlers durchsuchen sollen. Unten in der Seite befindet sich eine Fußzeile mit Direktlinks zu verschiedenen Themen, die Kunden interessieren könnten.

## <a name="buy-box-module"></a>Kauffeldmodul

Das wichtigste Modul auf einer PDP ist das Kauffeldmodul. Daher ist es das erste Element im Hauptabschnitt der Seite. Ein Kauffeldmodul ist ein Containermodul und enthält mehrere Module, die die wichtigsten Informationen zum Produkt enthalten. Zu diesen Informationen gehören der Produktname, die Produktbilder, die Beschreibung, der Preis und die Produktbewertungen.

Mit dem Kauffeldmodul kann der Kunde Produktoptionen (z. B. Größe, Stil und Farbe) auswählen und das Produkt in den Einkaufskorb legen. Der Kunde kann das Produkt auch online kaufen und in einem Geschäft abholen. Das Modul Online kaufen und im Geschäft abholen verwendet die Integration mit Bing Maps-APIs (Application Programming Interfaces), um Geschäfte in der Nähe oder Geschäfte an einem anderen vom Kunden angegebenen Ort zu finden.

Ein Kauffeldmodul erfordert eine Produkt-ID. Diese ID wird aus dem Seitenkontext abgeleitet. Wenn einer Seite, deren Seitenkontext keine Produkt-ID enthält, ein Kauffeldmodul hinzugefügt wird, werden die Informationen nicht korrekt wiedergegeben.

## <a name="product-specifications-module"></a>Produktklassifizierungsmodul

Mit dem Produktklassifizierungsmodul können zusätzliche Details zum Produkt angezeigt werden. Diese Details werden aus den Produktattributen in Dynamics 365 Retail übernommen. Das Produktklassifizierungsmodul zeigt jedes Attribut, bei dem die Eigenschaft **sichtbar** auf **true** gesetzt ist. Es erfordert eine Produkt-ID, um die Produktattribute abzurufen.

## <a name="recommendations-module"></a>Empfehlungsmodul

Das Empfehlungsmodul ist ein wichtiges Modul auf einer PDP. Während Kunden nach Produkten suchen, sollten ihnen mehr Produktoptionen angeboten werden, damit sie das richtige Produkt finden und einen Kauf tätigen können. Mithilfe von Empfehlungen können Kunden auf einfache Weise verwandte Inhalte entdecken und weiter einkaufen.

Es gibt verschiedene Arten von Empfehlungslisten:

- Die Liste **Personen gefällt auch** basiert auf dem maschinellen Lernen. Sie verwendet die Transaktionshistorie anderer Kunden, um Empfehlungen abzugeben. Diese Liste wird vom Empfehlungsdienst erstellt und ähnelt den Listen „Kunden, die dies gekauft haben, kauften auch ...“. Eine Produkt-ID ist zum Generieren dieser Liste erforderlich.
- Die Liste **Zugehörig** kann für ein Produkt in Retail konfiguriert werden. Beispielsweise können für eine braune Lederreisehandtasche mehrere Handtaschen auf Lederbasis oder für Reisezwecke entworfene Handtaschen für die Themenliste konfiguriert werden. Andere Typen zugehöriger Listen, wie **Zubehör** und **Weitere ähnliche Aktivitäten**, können auch in Retail konfiguriert werden. Eine Produkt-ID ist zum Generieren dieser Liste erforderlich. Daher ist die Liste leer, wenn sie zu einer Startseite hinzugefügt wird, auf der der Seitenkontext keine Produkt-ID enthält.
- Algorithmisch generierte Empfehlungslisten, wie **Populär**, **Bestseller** und **Neu** können in PDPs verwendet werden. Diese Listen stehen zwar möglicherweise nicht in direktem Zusammenhang mit dem Produkt auf der PDP, sind jedoch eine weitere Möglichkeit, Kunden bei der Suche nach Produkten zu unterstützen, die sie interessieren könnten. Diese Listentypen erfordern keine Produkt-ID. Hierbei handelt es sich um generische Listen, die auf der Grundlage von Einkaufsmustern auf der gesamten Website erstellt werden.
- Redaktionslisten sind manuell kuratierte Listen. Beispielsweise kann ein Einzelhändler entscheiden, Listen von Produkten, die präsentiert werden sollen, manuell zu kuratieren.

## <a name="ratings-and-reviews-module"></a>Bewertungs- und Prüfungsmodul

Das Bewertungs- und Prüfungsmodul zeigt Bewertungen und Prüfungen an, die von anderen Kunden bereitgestellt wurden. Hiermit kann ein Kunde auch seine eigene Bewertung des Produkts verfassen. Zusätzlich enthält es ein Histogramm, das den Bewertungstrend für das Produkt anzeigt. Weitere Details erhalten Sie unter [Bewertungs- und Prüfungsüberblick](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Marketingmodule

Wenn Marketinginhalte für ein bestimmtes Produkt spezifisch sind, kann der PDP ein beliebiges Marketingmodul hinzugefügt werden. Sie können einer PDP Marketingmodule hinzufügen, indem Sie die Seite „anreichern“. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht der Startseite](quick-tour-home-page.md)

[Übersicht der Standard-Kategorie-Landingpage und Suchergebnisseite](category-search-page-overview.md)

[Übersicht der Einkaufswagen- und Auschecken-Seiten](quick-tour-cart-checkout.md)

[Übersicht der Kontenverwaltungsseiten](quick-tour-account-management.md)
