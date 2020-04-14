---
title: Shopauswahlmodul
description: Dieses Thema enthält das Shopauswahlmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157339"
---
# <a name="store-selector-module"></a>Shopauswahlmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält das Shopauswahlmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Shopauswahlmodul wird für das Kundenszenario „Online kaufen, im Geschäft abholen“ (BOPIS) verwendet. Es zeigt eine Liste der Geschäfte an, in denen ein Produkt zur Abholung verfügbar ist, sowie die Öffnungszeiten und den Produktbestand für jedes Geschäft.

Das Shopauswahlmodul benötigt den Kontext eines Produkts und einen Suchort, um Filialen zu finden. Wenn kein Suchort vorhanden ist, wird standardmäßig der Browserstandort des Kunden verwendet, sofern der Kunde seine Zustimmung erteilt. Das Modul verfügt über ein Eingabefeld, in das der Kunde einen Ort (Postleitzahl oder Stadt und Bundesland) eingeben kann, um Geschäfte in der Nähe zu finden.

Das Store-Selector-Modul ist in der Anwendungsprogrammierschnittstelle (API) für die Geocodierung von Bing Maps integriert, um den angegebenen Standort in eine Breite und eine Länge zu konvertieren. Ein Bing Maps-API-Schlüssel ist erforderlich und muss auf der Seite „Freigegebene Commerce-Parameter“ in Dynamics 365 Commerce hinzugefügt werden.

Das Shopauswahlmodul kann einem Kaufboxmodul auf der Produktdetailseite (PDP) hinzugefügt werden, um Filialen anzuzeigen, in denen ein Produkt zur Abholung verfügbar ist. Es kann auch einem Einkaufswagenmodul hinzugefügt werden. Beim Hinzufügen zu einem Einkaufswagenmodul zeigt das Shopauswahlmodul Abholoptionen für jede Einkaufswagenposition an. Darüber hinaus kann dieses Modul mit benutzerdefinierter Codierung über Erweiterungen und Anpassungen zu anderen Seiten oder Modulen hinzugefügt werden.

Damit das BOPIS-Szenario funktioniert, sollten Produkte mit dem Liefermodus „Kundenabholung“ konfiguriert werden. Andernfalls wird das Modul nicht auf den jeweiligen Seiten angezeigt. Einzelheiten zum Konfigurieren des Übermittlungsmodus finden Sie unter [Lieferarten einrichten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Das folgende Bild zeigt ein Beispiel eines Speicherauswahlmoduls, das auf einem PDP verwendet wird.

![Beispiel eines Shopauswahlmoduls](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Speichern Sie die Verwendung des Auswahlmoduls im E-Commerce

- Ein Shopauswahlmodul kann auf einer Produktdetailseite (PDP) verwendet werden, um Filialen in der Nähe zu finden, in denen ein Produkt zur Abholung verfügbar ist.
- Ein Shopauswahlmodul kann auf einer Einkaufswagenseite verwendet werden, um Filialen in der Nähe zu finden, in denen ein Produkt im Einkaufswagen zur Abholung verfügbar ist.

## <a name="store-selector-module-properties"></a>Eigenschaften des Shopauswahlmoduls

| Eigenschaftenname             | Wert                 | Beschreibung |
|---------------------------|-----------------------|-------------|
| Suchradius | Nummer | Definiert den Suchradius für Geschäfte in Meilen. Wenn kein Wert angegeben wird, wird der Standardsuchradius von 50 Meilen verwendet.|
|Allgemeine Geschäftsbedingungen | URL    |  Für den Bing Maps-Dienst ist die URL zu den Nutzungsbedingungen erforderlich. |

## <a name="add-a-store-selector-module-to-a-page"></a>Hinzufügen eines Shopauswahlmoduls zu einer Seite

Ein Shopauswahlmodul benötigt den Kontext eines Produkts und kann daher nur in Kauffeld- und Einkaufswagenmodulen verwendet werden. Shopauswahlmodule funktionieren außerhalb dieser Module nicht.

- Informationen zum Hinzufügen eines Shopauswahlmoduls zu einem Kauffeldmodul finden Sie unter [Kauffeldmodul](add-buy-box.md). 
- Informationen zum Hinzufügen eines Shopauswahlmoduls zu einem Einkaufswagenmodul finden Sie unter [Einkaufswagenmodul](add-cart-module.md)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Schnelleinführung zur Produktdetailseite](quick-tour-pdp.md)

[Schnelleinführung zum Einkaufskorb und Auscheckvorgang](quick-tour-cart-checkout.md)

[Lieferarten einrichten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
