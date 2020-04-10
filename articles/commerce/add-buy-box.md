---
title: Kauffeldmodul
description: Dieses Thema enthält Kauffeldmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 3417156cbf3cb20a5190e5e51b61b3423816895a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154062"
---
# <a name="buy-box-module"></a>Kauffeldmodul


[!include [banner](includes/banner.md)]

Dieses Thema enthält Kauffeldmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Der Begriff *Kauffeld* bezieht sich in der Regel auf einen Produktdetailseiten-Bereich, der „über der Falte“ angezeigt wird und die wichtigsten Informationen enthält, die erforderlich sind, um einen Produkteinkauf abzuschließen. (Ein Bereich, der „über der Falte“ ist, wird angezeigt, wenn die Seite zuerst geladen wird, sodass Benutzer nicht nach unten scrollen müssen, um sie zu sehen.)

Ein Kauffeldmodul ist ein spezieller Container, der verwendet wird, um alle zu Module verwenden, die im Kauffeldbereich einer Produktdetailseite angezeigt werden.

Die URL einer Produktdetailseite, die in einer Produktkennung enthalten ist. Alle Informationen, die erforderlich sind, um ein Kauffeldmodul zu stellen, werden von dieser Produktkennung berechnet. Wenn eine Produktkennung nicht bereitgestellt wird, wird das Kauffeldmodul nicht ordnungsgemäß auf einer Seite dargestellt. Daher kann ein Kauffeldmodul nur auf Seiten mit Produktkontext verwendet werden. Um es auf einer Seite ohne Produktkontext (z. B. einer Homepage oder einer Marketingseite) zu verwenden, müssen Sie zusätzliche Anpassungen vornehmen.

## <a name="buy-box-module-properties-and-slots"></a>Kaufen Sie Feldmoduleigenschaften und -Slots 

In einer Produktdetailseite wird ein Kauffeld in zwei Bereiche unterteilt: einen Medienbereich auf der linken und einen Inhaltsbereich auf der rechten Seite. Standardmäßig beträgt das Verhältnis der Breite der Medienbereichsspalte zur Breite der Inhaltsbereichsspalte 2:1. Auf mobilen Geräten werden diese beiden Regionen gestapelt, so dass die Regionen übereinander angezeigt werden. Mithilfe von Themen können Sie die Spaltenbreiten und den Stapelrang anpassen.

Ein Kauffeldmodul gibt den Titel, die Beschreibung, den Preis und die Bewertungen eines Produkts wieder. Außerdem können Kreditoren Produktvarianten mit unterschiedlichen Produktattributen wie Größe, Stil und Farbe auswählen. Wenn eine Produktvariante ausgewählt wird, werden andere Eigenschaften im Kauffeld, (beispielsweise die Produktbeschreibung und Bilder) aktualisiert, um die verschiedenen Informationen neu zu berechnen. 

Eine Mengenauswahl wird bereitgestellt, damit Kreditoren die Menge der zu kaufenden Artikel angeben können. Die maximale Menge, die gekauft werden kann, kann in den Site-Einstellungen festgelegt werden.
 
Über das Kauffeld können Kunden auch Aktionen ausführen, z. B. ein Produkt in den Warenkorb legen, ein Produkt zu ihrer Wunschliste hinzufügen und einen Abholort auswählen. Diese Aktionen können für ein Produkt oder eine Produktvariante ausgeführt werden. Um ein Produkt zu einer Wunschliste hinzuzufügen, muss der Kunde angemeldet sein.

Mithilfe von Designs können Sie die Reihenfolge der Produkteigenschaften und Aktionssteuerelemente der Kaufbox entfernen oder ändern. 

## <a name="module-properties"></a>Moduleigenschaften

- **Überschriften-Tag** – Diese Eigenschaft definiert das Überschriften-Tag für den Produkttitel. Wenn sich das Kauffeld oben auf der Seite befindet, sollte diese Eigenschaft auf **h1** festgelegt werden, um die Zugänglichkeitsstandards zu erfüllen. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Module, die im Kauffeldmodus verwendet werden können

- **Mediengalerie** - Dieses Modul wird verwendet, um die Bilder eines Produkts auf einer Produktdetailseite anzuzeigen. Es kann ein bis zu vielen Bildern unterstützen. Er unterstützt auch Miniaturbilder. Die Miniaturbilder können horizontal (als Zeile unter dem Bild) oder vertikal angeordnet werden (als Spalte neben dem Bild). Das Medienkatalogmodul kann dem Slot **Medien** im Kauffeldmodul hinzugefügt werden. Es unterstützt derzeit nur Bilder. 
- **Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen. Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen. Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).

## <a name="buy-box-module-settings"></a>Kauffeldmoduleinstellungen

Kauffeldmodule haben drei Einstellungen, die unter **Site-Einstellungen \> Erweiterungen**  konfiguriert werden können:

- **Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann. Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.
- **Bestandsscheck** – Wenn der Wert auf **Wahr** gesetzt ist, wird nur ein Artikel in den Einkaufskorb gelegt, nachdem das Kauffeldmodul sicherstellt, dass es auf Lager ist. Dieser ist für Bestandsscheck Szenarien ausgeführt, in denen es sich beim Artikel und für Szenarios versendet wird, wo er in Filiale aufgehoben wird. Wenn der Wert auf **Falsch** gesetzt wird, wird kein Bestandsscheck geleistet, bevor ein Artikel in den Einkaufskorb gelegt wird und der Auftrag erteilt wird.
- **Inventarpuffer** – Diese Eigenschaft wird verwendet, um eine Puffernummer für das Inventar anzugeben. Bestandspuffer – Lagerbestand wird in Echtzeit verwaltet und wenn viele Debitoren Bestellungen aufgeben, kann es schwierig sein, die Lagerzählung zu verwalten. Wenn ein Bestandsscheck erfolgt, und wenn der Bestand kleiner ist als der Pufferbetrag, wird das Produkt nicht als vorrätig behandelt. Wenn Verkäufe rasch in mehreren Kanälen erfolgen und die Bestandszählung nicht vollständig synchronisiert wird, ist das Risiko kleiner, dass ein Artikel verkauft wird, der nicht vorrätig ist.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit-Interaktion

Das Kauffeldmodul ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab. Die Produktkennung von der Produktdetailseite wird verwendet, um alle Informationen abzurufen.

## <a name="add-a-buy-box-module-to-a-page"></a>Hinzufügen eines Kauffeldmodul zu einer Seite

Um ein Kauffeldmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie ein Fragment, das mit dem Namen **Kauffeldfragment** bezeichnet ist und fügen Sie einen Kauffeldmodul AIF-Webdienst hinzu.
1. Im Slot **Medien** im Kauffeldmodul fügen Sie ein Mediengalleriemodul hinzu.
1. Fügen Sie im Slot **Auswahl speichern** des Kauffeldmoduls ein Store-Selector-Modul hinzu.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.
1. Erstellen Sie eine Vorlage für eine Produktdetailseite und bezeichnen Sie diese als **PDP-Vorlage**
1. Eine Standardseite hinzufügen.
1. Im Slot **Haupt-** der Standardseite fügen Sie ein Kauffeldfragment hinzu.
1. Speichern Sie die Vorlage, beenden Sie die Bearbeitung und veröffentlichen Sie sie.
1. Verwenden Sie die Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **PDP Seite** hat.
1. Im Slot **Haupt-** der neuen Seite fügen Sie ein Kauffeldfragment hinzu.
1. Seite speichern und Vorschau anzeigen. Fügen Sie die **? productid=&lt;Produktkennung&gt;**-Abfragezeichenfolgenparameter der URL der Vorschauseite hinzu. So wird der Produktkontext verwendet, um die Vorschauseite zu stellen und zu rendern.
1. Speichern Sie die Seite, beenden Sie die Bearbeitung und veröffentlichen Sie sie. Ein Kauffeld sollte auf der Produktdetailseite angezeigt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Shopauswahlmodul](store-selector.md)

[Containermodul](add-container-module.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
