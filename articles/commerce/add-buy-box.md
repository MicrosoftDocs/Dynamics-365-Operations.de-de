---
title: Kauffeldmodul
description: Dieses Thema enthält Kauffeldmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811140"
---
# <a name="buy-box-module"></a>Kauffeldmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält Kauffeldmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Der Begriff *Kauffeld* bezieht sich in der Regel auf einen Produktdetailseiten-Bereich, der „über der Falte“ angezeigt wird und die wichtigsten Informationen enthält, die erforderlich sind, um einen Produkteinkauf abzuschließen. (Ein Bereich, der „über der Falte“ ist, wird angezeigt, wenn die Seite zuerst geladen wird, sodass Benutzer nicht nach unten scrollen müssen, um sie zu sehen.)

Ein Kauffeldmodul ist ein spezieller Container, der verwendet wird, um alle zu Module verwenden, die im Kauffeldbereich einer Produktdetailseite angezeigt werden.

Die URL einer Produktdetailseite, die in einer Produktkennung enthalten ist. Alle Informationen, die erforderlich sind, um ein Kauffeldmodul zu stellen, werden von dieser Produktkennung berechnet. Wenn eine Produktkennung nicht bereitgestellt wird, wird das Kauffeldmodul nicht ordnungsgemäß auf einer Seite dargestellt. Daher kann ein Kauffeldmodul nicht auf einer Seite verwendet werden, die keinen Produktkontext hat (z.B. eine Startseite oder eine Marketing-Seite).

## <a name="buy-box-module-properties-and-slots"></a>Kaufen Sie Feldmoduleigenschaften und -Slots 

Als Container steuert ein Kauffeldmodul die grundlegenden Eigenschaften, wie die Breite. Die Breiteneinstellung bestimmt, ob die Module im Containers in den Container passen müssen oder  ob sie den Bildschirm ausfüllen können.

In einer Produktdetailseite wird ein Kauffeld in zwei Bereiche unterteilt: einen Medienbereich auf der linken und einen Inhaltsbereich auf der rechten Seite. Diese beiden Regionen werden anhand von Slots im Kauffeldmodul dargestellt. Jeder Slot ist vorkonfiguriert, um nur bestimmte Module zu akzeptieren, die durch den Slot unterstützt werden. So ermöglicht eine Slot **Medien** nur das Medienkatalogmodul.

Standardmäßig ist das Verhältnis zwischen der Spaltenbreiten für den Bereich Medien und den Bereich Inhaltstext 2:1. Allerdings können die Spaltenbreiten nach Thema überschrieben werden. Darüber hinaus werden auf mobilen Geräten diese beiden Regionen gestapelt, so dass die Regionen übereinander angezeigt werden.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Module, die im Kauffeldmodus verwendet werden können

- **Mediengalerie** - Dieses Modul wird verwendet, um die Bilder eines Produkts auf einer Produktdetailseite anzuzeigen. Es kann ein bis zu vielen Bildern unterstützen. Er unterstützt auch Miniaturbilder. Die Miniaturbilder können horizontal (als Zeile unter dem Bild) oder vertikal angeordnet werden (als Spalte neben dem Bild). Das Medienkatalogmodul kann dem Slot **Medien** im Kauffeldmodul hinzugefügt werden. Es unterstützt derzeit nur Bilder und Videos.
- **Produkttitel** – Dieses Modul zeigt den Titel des Produkts in einer Produktdetailseite angezeigt. Standardmäßig wird die **H1** Überschriftsmarkierung verwendet, aber die Überschriftsmarkierung kann nach Bedarf geändert werden.
- **Produktbewertung** – Dieses Modul zeigt die Sternbewertungen, basierend auf Beurteilungen der Kunden für ein Produkt. Das Kauffeldmodul ruft die Produktbewertungen für jedes Produkt aus dem Bewertungs-Service ab.
- **Produktpreis** – Dieses Modul zeigt den Preis des Produkts an. Der Preis enthält durchgestrichene Preise und Rabatte.
- **Produktbeschreibung** – Dieses Modul zeigt die Beschreibung des Produkts an.
- **Produkt konfigurieren** – Dieses Modul zeigt die Größe, den Stil und die Dimensionen des Produkts an. Die Dimensions-Auswahlen können Vertikal gestapelt werden, oder sie können nebeneinander angezeigt werden. Wenn eine Produktvariante ausgewählt wird, werden andere Eigenschaften im Kauffeld, (beispielsweise die Produktbeschreibung und Bilder) aktualisiert, um die verschiedenen Informationen neu zu berechnen.
- **Produktmenge** - Dieses Modul wird zur Konfiguration der Produktmenge verwendet. Eine Profileinrichtung beschränkt die Menge eines Produkts oder der Variante, die dem Einkaufskorb hinzugefügt werden können.
- **Zum Einkaufskorb hinzufügen** Dieses Modul wird verwendet, um die Aktivität des Hinzufügens zum Einkaufskorb durchzuführen. Nur ein Produkt oder eine Variante kann dem Einkaufskorb hinzugefügt werden. Das bedeutet, kann ein Vorlagenprodukt nicht in den Einkaufskorb gelegt werden kann. Das Modul **Navigieren Sie zum Einkaufskorb** enthält eine Eigenschaft, die der Standortsautor festlegen kann. Wird diese Eigenschaft auf **Wahr** festgelegt, wird der Benutzer immer zur Einkaufswagenseite geführt, wenn eine Aktivität „dem Einkaufskorb hinzufügen“ ausgelöst wird. Wenn es auf **Falsch** festgelegt wurde, kann der Debitor weiter die Produktdetailseite durchsuchen, wenn Artikel in den Einkaufskorb gelegt werden.
- **Dem Wunschzettel hinzufügen** – Dieses Modul wird verwendet, um einen Artikel dem Wunschzettel des Debitors hinzuzufügen. Nur ein Produkt oder eine Variante kann der Wunschliste hinzugefügt werden. Zudem muss der Debitor bei der Site angemeldet sein. Das Modul enthält Fehlerbehandlungslogik, um zu überprüfen, ob beide diese Bedingungen erfüllt sind.
- **Suchen im Shop** – Dieses Modul löst den Fluss „Online kaufen, im Shop abholen“ aus.
- **Im Shop abholen** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen. In diesem Modul werden standardmäßig Filialen angezeigt, die in einem Radius von 50 Kilometern vom Standort des Kunden sind. Allerdings kann der Suchradius im Modul angepasst werden. Für jeden Shop wird ein Bestandsscheck ausgeführt, wenn die Bestandsscheckfunktionen aktiviert ist und eine entsprechende Nachricht an Lager oder nicht vorrätig angezeigt wird.
- **Shopsuche durch Bing Maps**- Dieses Modul kann im Shop-Modul im Shop abholen verwendet werden. Es ermöglicht Kunden, nach Shops zu suchen, indem ein Ort eingeben wird. Die Anwendungsprogrammierschnittstelle (API) für die Geocodierung von Bing Maps wird verwendet, um den angegebenen Lagerplatz in eine Breite und eine Länge zu konvertieren. Wenn das Modul verwendet wird, nur Filialen, sich nahe dem aktuellen Standort des Debitors werden, angezeigt und der Debitor kann nicht für einen anderen Speicherort suchen.
- **Umfangreicher Inhaltsblock** – Dieses Modul kann eine Meldung anzeigen, die der Site-Autor oder Einzelhändler im Kauffeld promoten möchte, wie „bei Problemen mit der Bestellung kontaktieren Sie 1-800-FABRIKAM“ oder „kostenloser Versand bei Aufträgen über € 100“. Die Meldungen werden durch das Content Management-System (CMS) gesteuert.

## <a name="buy-box-module-settings"></a>Kauffeldmoduleinstellungen

Kauffeldmodule haben drei Einstellungen, die konfiguriert werden können:

- **Höchstmenge** – Die maximale Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann. Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.
- **Bestandsscheck** – Wenn der Wert auf **Wahr** gesetzt ist, wird nur ein Artikel in den Einkaufskorb gelegt, nachdem das Kauffeldmodul sicherstellt, dass es auf Lager ist. Dieser ist für Bestandsscheck Szenarien ausgeführt, in denen es sich beim Artikel und für Szenarios versendet wird, wo er in Filiale aufgehoben wird. Wenn der Wert auf **Falsch** gesetzt wird, wird kein Bestandsscheck geleistet, bevor ein Artikel in den Einkaufskorb gelegt wird und der Auftrag erteilt wird.
- **Bestandspuffer** – Lagerbestand wird in Echtzeit verwaltet und wenn viele Debitoren Bestellungen aufgeben, kann es schwierig sein, die Lagerzählung zu verwalten. Daher kann ein Puffer zu Lagerzwecken definiert werden. Wenn ein Bestandsscheck erfolgt, und wenn der Bestand kleiner ist als der Pufferbetrag, wird das Produkt nicht als vorrätig behandelt. Wenn Verkäufe rasch in mehreren Kanälen erfolgen, sodass die Bestandszählung nicht vollständig synchronisiert wird, ist das Risiko kleiner, dass ein Artikel verkauft wird, der nicht vorrätig ist.

## <a name="retail-server-interaction"></a>Retail Server-Interaktion

Das Kauffeldmodul ruft Produktinformationen mithilfe der Retail Server  APIs ab. Die Produktkennung von der Produktdetailseite wird verwendet, um alle Informationen abzurufen.

## <a name="add-a-buy-box-module-to-a-page"></a>Hinzufügen eines Kauffeldmodul zu einer Seite

Um ein Kauffeldmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie ein Fragment, das mit dem Namen **Kauffeldfragment** bezeichnet ist und fügen Sie einen Kauffeldmodul AIF-Webdienst hinzu.
1. Im Slot **Medien** im Kauffeldmodul fügen Sie ein Mediengalleriemodul hinzu.
1. Im **Inhalt** Slot des Kauffeldmoduls, fügen Sie die folgenden Module hinzu: Produkttitel, Produktbewertung, Produktpreis, Produktbeschreibung, Produkt konfigurieren, in den Einkaufskorb legen, dem Wunschzettel hinzufügen und suchen im Shop. Sie können die Einrichtung im Slot **Inhalt** anpassen, um das gewünschte Layout zu erreichen.
1. Wählen Sie das Modul im Shop suchen aus. Im Slot innerhalb dieses Moduls fügen Sie ein Modul im Shop abholen hinzu.
1. Im Slot innerhalb des Moduls im Shop abholen fügen Sie eine Shopsuche mithilfe dem Bing Maps Modul hinzu.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.
1. Erstellen Sie eine Vorlage für eine Produktdetailseite und bezeichnen Sie diese als **PDP-Vorlage**
1. Eine Standardseite hinzufügen.
1. Im Slot **Haupt-** der Standardseite fügen Sie ein Kauffeldfragment hinzu.
1. Speichern Sie die Vorlage, laden Sie sie hoch und veröffentlichen Sie sie.
1. Verwenden Sie die Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **PDP Seite** hat.
1. Im Slot **Haupt-** der neuen Seite fügen Sie ein Kauffeldfragment hinzu.
1. Seite speichern und Vorschau anzeigen. Fügen Sie die **? productid=&lt;Produktkennung&gt;**-Abfragezeichenfolgenparameter der URL der Vorschauseite hinzu. So wird der Produktkontext verwendet, um die Vorschauseite zu stellen und zu rendern.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie. Ein Kauffeld sollte auf der Produktdetailseite angezeigt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
