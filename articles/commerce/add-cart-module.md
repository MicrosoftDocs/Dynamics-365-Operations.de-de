---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154016"
---
# <a name="cart-module"></a>Einkaufswagenmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Über das Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht. Das Modul zeigt eine Bestellzusammenfassung an und der Kunde kann Werbecodes anwenden oder entfernen.

Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen. Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**. Sie können die Route für diesen Link unter **Seiteneinstellungen \>Erweiterungen \>Routen** konfigurieren.

Das Warenkorbmodul rendert Daten basierend auf der Warenkorb-ID, einem auf der gesamten Site verfügbaren Browser-Cookie.

## <a name="cart-module-properties-and-slots"></a>Einkaufswagenmodul-Eigenschaften und Slots

Das Wagenmodul hat eine **Überschrift**-Eigenschaft, die auf Werte wie **Einkaufstasche** und **Artikel im Einkaufskorb** gesetzt werden kann. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Module, die im Einkaufswagenmodul verwendet werden können

- **Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul. Die Meldungen werden durch das Content Management-System (CMS) gesteuert. Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“
- **Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen. Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen. Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).

## <a name="cart-module-settings"></a>Einkaufswagen-Einstellungen

Einkaufswagenmodule haben die folgenden Einstellungen, die unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden können:

- **Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann. Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.
- **Bestandsscheck** – Wenn der Wert auf **Wahr** gesetzt ist, wird nur ein Artikel in den Einkaufskorb gelegt, nachdem das Kauffeldmodul sicherstellt, dass es auf Lager ist. Diesee Lagerüberprüfung wird für Szenarien ausgeführt, bei denen der Artikel versendet wird und für Szenarien, wenn der Artikel in der Filiale abgeholt wird. Wenn der Wert auf **Falsch** gesetzt wird, wird kein Bestandsscheck geleistet, bevor ein Artikel in den Einkaufskorb gelegt wird und der Auftrag erteilt wird.
- **Inventarpuffer** – Diese Eigenschaft wird verwendet, um eine Puffernummer für das Inventar anzugeben. Bestandspuffer – Lagerbestand wird in Echtzeit verwaltet und wenn viele Debitoren Bestellungen aufgeben, kann es schwierig sein, die Lagerzählung zu verwalten. Wenn ein Bestandsscheck erfolgt, und wenn der Bestand kleiner ist als der Pufferbetrag, wird das Produkt nicht als vorrätig behandelt. Wenn Verkäufe rasch in mehreren Kanälen erfolgen und die Bestandszählung nicht vollständig synchronisiert wird, ist das Risiko kleiner, dass ein Artikel verkauft wird, der nicht vorrätig ist.
- **Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben. Die Route kann auf Site-Ebene konfiguriert werden, sodass Einzelhändler den Kunden zur Homepage oder zu einer anderen Seite der Site zurückführen können.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit-Interaktion

Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab. Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.

## <a name="add-a-cart-module-to-a-page"></a>Ein Einkaufswagenmodul einer Seite hinzufügen

Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie ein Fragment, das mit dem Namen **Einkaufswagenfragment** bezeichnet ist und fügen Sie ein Einkaufswagenmodul dem neuen Fragment hinzu.
1. Hinzufügen eines Titels zum Einkaufswagenmodul.
1. Fügen Sie dem Einkaufswagenmodul ein Store-Selector-Modul hinzu.
1. Speichern Sie das Fragment, beenden Sie die Bearbeitung und veröffentlichen Sie das Fragment.
1. Erstellen Sie eine Vorlage mit der Bezeichnung **Einkaufswagenvorlage** und fügen Sie dann das Einkaufswagenfragment hinzu, das Sie soeben erstellt haben.
1. Speichern Sie die Vorlage, beenden Sie die Bearbeitung und veröffentlichen Sie die Vorlage.
1. Hier können Sie eine Seite erstellen, für die die neue Vorlage verwendet wird.
1. Seite speichern und Vorschau anzeigen.
1. Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Shopauswahlmodul](store-selector.md)

[Kauffeldmodul](add-buy-box.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
