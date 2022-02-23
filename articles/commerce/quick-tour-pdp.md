---
title: Übersicht der Produktdetailseiten
description: Dieses Thema bietet eine Übersicht über Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412670"
---
# <a name="product-details-pages-overview"></a>Übersicht der Produktdetailseiten

[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Übersicht

Eine PDP bietet detaillierte Informationen zu einem Produkt und ermöglicht es Kunden, Produktoptionen wie Größe, Stil und Farbe auszuwählen. Eine PDP sollte alle Produktinformationen enthalten, die ein Kunde benötigt, um eine Kaufentscheidung zu treffen.

Die folgende Abbildung zeigt ein Beispiel für eine PDP.

![Beispiel einer Produktdetailseite](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Kopf- und Fußzeilenmodule

Oben in der PDP befindet sich eine Kopfzeile mit allen Produktkategorien und anderen Seiten, die Kunden auf Wunsch des Einzelhändlers durchsuchen sollen. Unten in der Seite befindet sich eine Fußzeile mit Direktlinks zu verschiedenen Themen, die Kunden interessieren könnten.

## <a name="buy-box-module"></a>Kauffeldmodul

Das wichtigste Modul auf einer PDP ist das Kauffeldmodul, das als erstes Element im Hauptabschnitt der Seite angezeigt wird. Ein Kauffeldmodul zeigt wichtige Produktinformationen wie den Produktnamen, die Produktbeschreibung, den Produktpreis, Produktbilder und Produktbewertungen an.

Mit dem Kauffeldmodul kann der Kunde Produktoptionen (z. B. Größe, Stil und Farbe) auswählen und das Produkt in den Einkaufskorb legen. Der Kunde kann das Produkt auch online kaufen und in einem Geschäft abholen. Das Modul Online kaufen und im Geschäft abholen verwendet die Integration mit Bing Maps-APIs (Application Programming Interfaces), um Geschäfte in der Nähe oder Geschäfte an einem anderen vom Kunden angegebenen Ort zu finden.

Ein Kauffeldmodul erfordert eine Produkt-ID. Diese ID wird aus dem Seitenkontext abgeleitet. Wenn einer Seite, deren Seitenkontext keine Produkt-ID enthält, ein Kauffeldmodul hinzugefügt wird, werden die Informationen nicht korrekt wiedergegeben.

## <a name="product-specifications-module"></a>Produktklassifizierungsmodul

Mit dem Produktklassifizierungsmodul können zusätzliche Details zum Produkt angezeigt werden. Diese Details werden aus den Produktattributen in Commerce übernommen. Das Produktklassifizierungsmodul zeigt jedes Attribut, bei dem die Eigenschaft **sichtbar** auf **true** gesetzt ist. Es erfordert eine Produkt-ID, um die Produktattribute abzurufen.

## <a name="recommendations-module"></a>Empfehlungsmodul

Das Empfehlungsmodul ist ein wichtiges Modul auf einer PDP. Während Kunden nach Produkten suchen, sollten ihnen mehr Produktoptionen angeboten werden, damit sie das richtige Produkt finden und einen Kauf tätigen können. Mithilfe von Empfehlungen können Kunden auf einfache Weise verwandte Inhalte entdecken und weiter einkaufen.

Es gibt verschiedene Arten von Empfehlungslisten:

- Die Liste **Personen gefällt auch** basiert auf dem maschinellen Lernen. Sie verwendet die Transaktionshistorie anderer Kunden, um Empfehlungen abzugeben. Diese Liste wird vom Empfehlungsdienst erstellt und ähnelt den Listen „Kunden, die dies gekauft haben, kauften auch ...“. Eine Produkt-ID ist zum Generieren dieser Liste erforderlich.
- Die Liste **Zugehörig** kann für ein Produkt in Commerce konfiguriert werden. Beispielsweise können für eine braune Lederreisehandtasche mehrere Handtaschen auf Lederbasis oder für Reisezwecke entworfene Handtaschen für die Themenliste konfiguriert werden. Andere Typen zugehöriger Listen, wie **Zubehör** und **Weitere ähnliche Aktivitäten**, können auch in Commerce konfiguriert werden. Eine Produkt-ID ist zum Generieren dieser Liste erforderlich. Daher ist die Liste leer, wenn sie zu einer Startseite hinzugefügt wird, auf der der Seitenkontext keine Produkt-ID enthält.
- Algorithmisch generierte Empfehlungslisten, wie **Populär**, **Bestseller** und **Neu** können in PDPs verwendet werden. Diese Listen stehen zwar möglicherweise nicht in direktem Zusammenhang mit dem Produkt auf der PDP, sind jedoch eine weitere Möglichkeit, Kunden bei der Suche nach Produkten zu unterstützen, die sie interessieren könnten. Diese Listentypen erfordern keine Produkt-ID. Hierbei handelt es sich um generische Listen, die auf der Grundlage von Einkaufsmustern auf der gesamten Website erstellt werden.
- Redaktionslisten sind manuell kuratierte Listen. Beispielsweise kann ein Einzelhändler entscheiden, Listen von Produkten, die präsentiert werden sollen, manuell zu kuratieren.

## <a name="ratings-and-reviews-modules"></a>Bewertungs- und Prüfungsmodule

Mit drei Modulen können Prüfungen angezeigt und hinzugefügt werden:

- **Prüfungen** – Dieses Modul zeigt Bewertungen und Prüfungen an, die von anderen Kunden bereitgestellt wurden. Kunden können die Prüfungen sortieren und filtern. Dieses Modul ermöglicht es auch Kunden, Prüfungen zuzustimmen oder abzulehnen und Probleme zu melden.
- **Prüfung schreiben** – Mit diesem Modul können Kunden ihre eigenen Produktprüfungen verfassen.
- **Bewertungshistogramm** – Dieses Modul enthält ein Histogramm, das den Bewertungstrend für ein Produkt anzeigt.

Weitere Details erhalten Sie unter [Bewertungs- und Prüfungsüberblick](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Marketingmodule

Wenn Marketinginhalte für ein bestimmtes Produkt spezifisch sind, kann der PDP ein beliebiges Marketingmodul hinzugefügt werden. Sie können einer PDP Marketingmodule hinzufügen, indem Sie die Seite „anreichern“. Weitere Details finden Sie unter [Erweitern einer Produktseite](enrich-product-page.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht der Startseite](quick-tour-home-page.md)

[Übersicht der Einkaufswagen- und Auschecken-Seiten](quick-tour-cart-checkout.md)

[Übersicht der Kontenverwaltungsseiten](quick-tour-account-management.md)

[Erweitern einer Produktdetailseite](enrich-product-page.md)
