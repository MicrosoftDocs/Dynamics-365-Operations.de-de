---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696760"
---
# <a name="cart-module"></a>Einkaufswagenmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Einkaufswagenmodul ist ein Container, der verwendet wird, um alle Module zu hosten, die erforderlich sind, um Artikel im Einkaufskorb anzuzeigen. Beispielsweise umfasst er alle Artikel, die dem Einkaufskorb, der Auftragszusammenfassung und dem Promotionscode hinzugefügt wurden.

Ein Auscheckenmodul rendert Daten basierend auf der Warkenkorb-Kennung Die Kennung ist möglicherweise ein Browsercookie, das über die Site verfügbar ist.

## <a name="cart-module-properties-and-slots"></a>Einkaufswagenmodul-Eigenschaften und Slots

Als Container steuert ein Einkaufswagenmodul die grundlegenden Eigenschaften, wie die Überschrift und die Breite. Die Überschrift ist normalerweise Text wie **Einkaufstasche**, **Ihr Einkaufskorb** oder **Artikel im Einkaufskorb**. Die Breiteneinstellung bestimmt, ob die Module im Containers in den Container passen müssen oder  ob sie den Bildschirm ausfüllen können.

Die Einkaufskorbseite wird in mehrere Regionen unterteilt: Einkaufskorbpositionsartikel, Auftragszusammenfassung, Auschecken und Suche in Filiale Funktionen. Jede Region wird einem Slot im Einkaufswagenmodul zugeordnet, und jeder Slot nimmt einen vordefinierten Satz Module an.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Module, die im Einkaufswagenmodul verwendet werden können

- **Einkaufswagenpositionsartikel** – Dieses Modul zeigt eine Zusammenfassung der einzelnen Artikel an, die dem Einkaufskorb hinzugefügt wurde. Die Informationen enthalten den Produkttitel, die ausgewählten Dimensionen, den Preis, die Menge und die Rabatte. Dieses Modul unterstützt außerdem Aktivitäten wie „aus dem Einkaufskorb entfernen“ und „Hinzufügen zum Wunschzettel“. Für jede Position gibt es eine Option, um den Artikel zu versenden oder ihn vom Shop abzuholen. Diese Option muss im Modul im Shop abholen getrennt konfiguriert werden.
- **Auftragszusammenfassung** – Dieses Modul wird eine Auftragszusammenfassung anzeigen. Die Informationen beinhalten die Zwischensumme, die Steuern und die Ersparnisse. Eine Überschrift kann für dieses Modul konfiguriert werden.
- **Promocode** – Dieses Modul ermöglicht es dem Debitor, Promotionscodes einzulösen. Ein Promotionscode kann angewendet oder entfernt werden.
- **Auschecken** – Dieses Modul startet die Auscheckenaktivität und leitet den Benutzer auf die Seite Auschecken um. Drei Links müssen für dieses Modul konfiguriert werden:

    - **Auschecken** – Dieser Link zwingt Debitoren, sich anzumelden, wenn sie nicht bereits angemeldet sind.
    - **Gast auschecken** – Mit diesem Link können anonyme Kunden Bestellungen tätigen. Wird nur angezeigt, wenn Kunden nicht angemeldet sind.
    - **Zurück zum Einkaufen** – Mit diesem Link können Debitoren zur Startseite gehen oder zu einer beliebigen Seite, damit sie mit dem Einkaufen fortfahren können.

- **Umfangreicher Inhaltsblock** – Dieses Modul unterstützt benutzerdefiniertes Nachrichten im Einkaufswagenmodul. Die Meldungen werden durch das Content Management-System (CMS) gesteuert. Jede Nachricht kann hinzugefügt werden, wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“
- **Im Shop abholen** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen. In diesem Modul werden standardmäßig Filialen angezeigt, die in einem Radius von 50 Kilometern vom Standort des Kunden sind. Allerdings kann der Suchradius im Modul angepasst werden. Für jeden Shop wird ein Bestandsscheck ausgeführt, wenn die Bestandsscheckfunktionen aktiviert ist und eine entsprechende Nachricht an Lager oder nicht vorrätig angezeigt wird.
- **Shopsuche durch Bing Maps**- Dieses Modul kann im Shop-Modul im Shop abholen verwendet werden. Es ermöglicht Kunden, nach Shops zu suchen, indem ein Ort eingeben wird. Die Anwendungsprogrammierschnittstelle (API) für die Geocodierung von Bing Maps wird verwendet, um den angegebenen Standort, den der Kunde eingegeben hat, in eine Breite und eine Länge zu konvertieren. Wenn das Modul nicht verwendet wird, werden nur Filialen, die sich nahe dem aktuellen Standort des Debitors befinden, angezeigt und der Debitor kann nicht nach einem anderen Standort suchen.

## <a name="cart-module-settings"></a>Einkaufswagen-Einstellungen

Einkaufswagenmodule haben drei Einstellungen, die konfiguriert werden können:

- **Höchstmenge** – Die maximale Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann. Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.
- **Bestandsscheck** – Wenn der Wert auf **Wahr** gesetzt ist, wird nur ein Artikel in den Einkaufskorb gelegt, nachdem das Kauffeldmodul sicherstellt, dass es auf Lager ist. Dieser ist für Bestandsscheck Szenarien ausgeführt, in denen es sich beim Artikel und für Szenarios versendet wird, wo er in Filiale aufgehoben wird. Wenn der Wert auf **Falsch** gesetzt wird, wird kein Bestandsscheck geleistet, bevor ein Artikel in den Einkaufskorb gelegt wird und der Auftrag erteilt wird.
- **Bestandspuffer** – Lagerbestand wird in Echtzeit verwaltet und wenn viele Debitoren Bestellungen aufgeben, kann es schwierig sein, die Lagerzählung zu verwalten. Daher kann ein Puffer zu Lagerzwecken definiert werden. Wenn ein Bestandsscheck erfolgt, und wenn der Bestand kleiner ist als der Pufferbetrag, wird das Produkt nicht als vorrätig behandelt. Wenn Verkäufe rasch in mehreren Kanälen erfolgen, sodass die Bestandszählung nicht vollständig synchronisiert wird, ist das Risiko kleiner, dass ein Artikel verkauft wird, der nicht vorrätig ist.

## <a name="retail-server-interaction"></a>Retail Server-Interaktion

Das Einkaufswagenmodul ruft Produktinformationen mithilfe der Retail Server  APIs ab. Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen vom Retail Server abzurufen.

## <a name="add-a-cart-module-to-a-page"></a>Ein Einkaufswagenmodul einer Seite hinzufügen

Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie ein Fragment, das mit dem Namen **Einkaufswagenfragment** bezeichnet ist und fügen Sie einen Einkaufswagenmodul hinzu.
1. Im **Einkaufswagenpositionsartikel** Slot des Einkaufswagenmoduls, fügen Sie eine Einkaufswagenpositionsartikelmodul hinzu.
1. Im **Auftragszusammenfassung** Slot fügen Sie ein Auftragszusammenfassungsmodul hinzu.
1. Im **Promocode** Slot fügen Sie ein Promocodemodul hinzu.
1. Im **Auschecken** Slot fügen Sie ein Auscheckenmodul hinzu.
1. Im **Shop suchenb** Slot fügen Sie eine Entnahme im Shopmodul hinzu.
1. Im Modul im Shop abholen wählen Sie den Slot **Shop suchen** und fügen einen Shop über das Bing Maps Modul hinzu.
1. Laden Sie das Fragmen hoch und veröffentlichen Sie es.
1. Erstellen Sie eine Vorlage mit der Bezeichnung **Einkaufswagenvorlage** und fügen Sie das Einkaufswagenfragment hinzu, das Sie soeben erstellt haben.
1. Speichern Sie die Vorlage, laden Sie sie hoch und veröffentlichen Sie sie.
1. Hier können Sie eine Seite erstellen, für die die neue Vorlage verwendet wird.
1. Seite speichern und Vorschau anzeigen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
