---
title: Produktauflistung mit Bestandserfassung
description: In diesem Artikel wird beschrieben, wie Organisationen Seiten zur Produktauflisten auf ihrer Microsoft Dynamics 365 Commerce E-Commerce-Website konfigurieren, damit sie den Bestand erfassen.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473732"
---
# <a name="inventory-aware-product-listing"></a>Produktauflistung mit Bestandserfassung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Organisationen Seiten zur Produktauflisten auf ihrer Microsoft Dynamics 365 Commerce E-Commerce-Website konfigurieren, damit sie den Bestand erfassen. Zu den Produktauflistungsseiten gehören Kategorie-Angebotsseiten und Suchergebnisseiten.

Käufer erwarten im Allgemeinen, dass die Produkterkennung auf einer E-Commerce-Website durchgehend den Bestand erfassen, damit sie entscheiden können, was zu tun ist, wenn ein Produkt ausverkauft ist. Das [Commerce-Modulbibliothek](starter-kit-overview.md) Kategorie- und Suchergebnismodule können so konfiguriert werden, dass sie Bestandsdaten einbeziehen. Auf diese Weise können sie die folgenden Erfahrungen bieten:

- Bestandsangaben neben Produkten anzeigen.
- Nicht vorrätige Produkte aus der Produktliste ausblenden.
- Nicht vorrätige Produkte an das Ende von Produktlistenseiten verschieben.
- Bestandsbasierte Produktfilterung unterstützen.

Um diese Erfahrungen zu aktivieren, müssen Sie zuerst das Feature **Erweiterte E-Commerce-Produktermittlung zur Bestandserfassung** in Commerce headquarters aktivieren.

> [!NOTE]
> Ab der Commerce-Version 10.0.29 ist das Feature **Erweiterte E-Commerce-Produktermittlung zur Bestandserfassung** standardmäßig aktiviert.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Das Produktattribut für die Bestandsverfügbarkeit einrichten

Die Produktauflistung mit Bestandserfassung verwendet das Produktattribute-Framework. Als Voraussetzung muss ein dediziertes Produktattribut erstellt werden, um Bestandsverfügbarkeitsdaten zu erfassen.

Um das Produktattribut für die Bestandsverfügbarkeit in Commerce headquarters einzurichten, folgen Sie diesen Schritten.

1. Gehen Sie zu **Einzelhandel und Handel \> IT für Einzelhandel und Handel \> Produkte und Bestand \> Produktattribute mit Lagerbestand befüllen**.
1. Geben Sie im Dialogfeld **Produktattribute mit Lagerbestand befüllen** im Feld **Produktattribut und Typname** einen benutzerdefinierten Namen für das dedizierte Produktattribut ein, das erstellt wird, um Bestandsdaten zu erfassen.
1. Wählen Sie im Feld **Bestandsverfügbarkeit basierend auf** den Mengentyp aus, auf dem die Berechnung des Lagerbestands basieren soll: **Physisch verfügbar** oder **Verfügbare Menge**.
1. Legen Sie Option **Stapelverarbeitung** auf **Ja** fest.
1. Wählen Sie **OK** aus.

> [!NOTE]
> Für eine konsistente Berechnung des Lagerbestands über die Seiten Ihrer E-Commerce-Website hinweg wählen Sie denselben Mengentyp sowohl im Feld **Bestandsverfügbarkeit basierend auf** des Auftrags **Produktattribute mit Lagerbestand befüllen** und in der Einstellung **Lagerbestand basierend auf** im Commerce Website-Generator aus.

Nachdem das dedizierte Produktattribut erstellt wurde, besteht der nächste Schritt darin, das Attribut für den Online-Kanal zu konfigurieren.

Um das neue Produktattribut für den Online-Kanal in Commerce headquarters zu konfigurieren, folgen Sie diesen Schritten.

1. Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.
1. Wählen Sie den Online-Kanal aus, für den die Produktauflistungsumgebung mit Bestandserfassung aktiviert werden soll.
1. Wählen und öffnen Sie eine zugehörige Attributgruppe und fügen Sie ihr dann das neue Produktattribut hinzu.
1. Gehen Sie zu **Einzelhandel und Handel \> IT für Einzelhandel und Handel \> Vertriebsplan** und führen Sie den Einzelvorgang **1150** (**Katalog**) aus. Sie sollten diesen Einzelvorgang als Stapelverarbeitung planen, der mit der gleichen Häufigkeit ausgeführt wird, wie der Einzelvorgang **Produktattribute mit Lagerbestand befüllen**.

> [!NOTE]
> In Commerce-Version 10.0.26 und früher müssen Sie nach dem Hinzufügen des Bestandsverfügbarkeit-Produktattribut zu einer Attributgruppe auch **Attributmetadaten festlegen** auswählen und dann die Optionen **Attribut für Kanal anzeigen**, **Abrufbar**, **Kann verfeinert werden** und **Kann abgefragt werden** für das neue Produktattribut aktivieren.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Das Anzeigeverhalten für nicht vorrätige Produkte auf Produktauflistungsseiten aktivieren

Nachdem alle vorherigen Konfigurationsschritte abgeschlossen sind, verfügen die Einschränkungen auf Kategorie- und Suchergebnisseiten über eine Filteroption mit Bestandserfassung. Für jede Produktkachel, die auf der Seite erscheint, wird eine Lagerbestandsangabe angezeigt.

Die Kategorie- und Suchergebnisseite zeigt Produkte auf der Hauptebene an, nicht auf der Produktvariantenebene. Der Lagerbestand, der neben jedem Produkt angezeigt wird, ist ein aggregierter Lagerbestand, der sich aus dem Lagerbestand aller Varianten eines Produkts ergibt. Der Lagerbestand einer Variante wird basierend auf dem verfügbaren Lagerbestand dieser Variante im Standardlager des Online-Kanals in Commerce headquarters berechnet. Der Lagerbestand eines Masterprodukts hat zwei mögliche Werte, die den Status „Auf Lager“ und „Nicht auf Lager“ darstellen. Ein Masterprodukt gilt als ausverkauft, wenn alle seine Varianten ausverkauft sind. Ansonsten gilt das Produkt als auf Lager. Das Angabe für den Wert wird aus der Definition [Lagerbestand](inventory-buffers-levels.md) abgerufen. Wenn kein Lagerbestand definiert ist, sind die Standardbezeichnungen (in Englisch) **Verfügbar** und **Ausverkauft**.

Sie könne die Einstellung **Bestandseinstellungen für Produktlistenseiten** im Commerce Website-Generator konfigurieren, um zu steuern, wie die Kategorie- und Suchergebnisseiten nicht vorrätige Produkte anzeigen. Weitere Informationen finden Sie unter [Bestandeinstellungen anwenden](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
