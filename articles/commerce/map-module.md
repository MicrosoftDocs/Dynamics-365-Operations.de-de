---
title: Kartenmodul
description: In diesem Thema werden Kartenmodule behandelt und deren Konfiguration in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: af6aedb6c0112822155c6d855909578a927d1c2c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665419"
---
# <a name="map-module"></a>Kartenmodul

[!include [banner](includes/banner.md)]


In diesem Thema werden Kartenmodule behandelt und deren Konfiguration in Microsoft Dynamics 365 Commerce beschrieben.

## <a name="overview"></a>Übersicht

Ein Kartenmodul zeigt die Standorte von Geschäften auf einer interaktiven Karte an, die mithilfe der [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/) gerendert wird. Ein Bing Maps-API-Schlüssel ist erforderlich und muss auf der Seite „Freigegebene Parameter“ in Commerce Headquarters hinzugefügt werden. Kartenmodule bieten verschiedene Ansichten wie Straße, Luftbild und Streetside, die Benutzer auswählen können, um Kartenpositionen anzuzeigen. Sie erlauben außerdem Interaktionen wie Zoomen und die Verwendung des Standortes des Benutzers.

Ein Kartenmodul ermittelt in Verbindung mit dem Shopauswahlmodul die geografischen Standorte von Geschäften, die auf einer Karte gerendert werden müssen. Die Shopauswahl- und Kartenmodule interagieren, wenn ein Benutzer ein Geschäft in einem dieser Module auf einer Seite auswählt. Kartenmodule können über die Interaktion mit Shopauswahlmodulen hinaus für andere Szenarien erweitert werden. Eine Modulanpassung ist jedoch erforderlich.

> [!NOTE]
> Das Kartenmodul ist in der Dynamics 365 Commerce-Version 10.0.13 verfügbar.

Das folgende Bild zeigt ein Beispiel eines Kartenmoduls, das auf einer Ladenstandortseite verwendet wird.

![Beispiel eines Shopauswahlmoduls](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Moduleigenschaften

| Eigenschaftenname             | Wert                 | Beschreibung |
|---------------------------|-----------------------|-------------|
| Überschrift | Text | Die Überschrift für das Modul. |
| Reißzweckenoptionen: Standardsymbol | Bild | Das Reißzweckensymbol, das für Geschäfte verwendet werden soll, die auf einer Karte angezeigt werden. |
| Reißzweckenoptionen: Aktives Symbol | Bild | Das Reißzweckensymbol, das für ein Geschäft verwendet werden soll, das auf einer Karte ausgewählt wird. |
| Reißzweckenoptionen: Standardsymbolfarbe | Zeichenfolge | Der Text- oder Hexadezimalwert für die Farbe der Reißzweckensymbole auf einer Karte. |
| Reißzweckenoptionen: Farbe aktives Symbol | Zeichenfolge | Der Text- oder Hexadezimalwert für die Farbe der auf einer Karte ausgewählten Reißzweckensymbole. |
| Index anzeigen | **True** oder **False** | Wenn diese Eigenschaft auf **Wahr** gesetzt wird, zeigt jedes Reißzweckensymbol, das für ein Geschäft steht, eine Zahl an. Diese Zahl stimmt mit der Zahl in der Listenansicht überein, die das Shopauswahlmodul anzeigt. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Zulässige Kartierungs-URLs zu den Inhaltssicherheitsrichtlinien einer Website hinzufügen

Damit das Kartenmodul mit Bing Karten interagieren kann, müssen Sie sicherstellen, dass die folgenden Zuordnungs-URLs gemäß der Inhaltssicherheitsrichtlinie (CSP) Ihrer Website zulässig sind. Diese Einstellung erfolgt im Commerce Site Builder, indem zulässige URLs zu verschiedenen Inhaltssicherheitsrichtlinie der Website hinzugefügt werden (z. B. **img-src**). Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie](manage-csp.md). 

- Fügen Sie der **connect-src**-Richtlinie **&#42;.bing.com** hinzu.
- Fügen Sie der **img-src**-Richtlinie **&#42;.virtualearth.net** hinzu.
- Fügen Sie zur **script-src**-Richtlinie **&#42;.bing.com, &#42;.virtualearth.net** hinzu.
- Fügen Sie der **script style-src**-Richtlinie **&#42;.bing.com** hinzu.

## <a name="add-a-map-module-to-a-page"></a>Ein Kartenmodul einer Seite hinzufügen

Ausführliche Informationen zum Konfigurieren eines Kartenmoduls auf einer Seite finden Sie unter [Shopauswahlmodul](store-selector.md). 
 
## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Shopauswahlmodul](store-selector.md)

[Bing Karten für Ihr Unternehmen verwalten](./dev-itpro/manage-bing-maps.md)

[Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]