---
title: Bestandseinstellungen anwenden
description: Dieser Artikel behandelt Inventareinstellungen und beschreibt, wie sie in Microsoft Dynamics 365 Commerce angewendet werden.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 49310a44f8b9c636734e04d4eed9445384b55791
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405319"
---
# <a name="apply-inventory-settings"></a>Bestandseinstellungen anwenden

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt Inventareinstellungen und beschreibt, wie sie in Microsoft Dynamics 365 Commerce angewendet werden.

Die Inventareinstellungen geben an, ob das Inventar überprüft werden soll, bevor Produkte in den Warenkorb gelegt werden. Sie definieren auch inventarbezogene Merchandising-Nachrichten wie Auf Lager und Nur noch wenige übrig. Diese Einstellungen stellen sicher, dass ein Produkt nicht gekauft werden kann, wenn es nicht vorrätig ist.

Dynamics 365 Commerce bietet Schätzungen zur Verfügbarkeit von Produkten. Informationen zur Berechnung der geschätzten Verfügbarkeit finden Sie unter [Berechnen Sie die Lagerverfügbarkeit für Einzelhandelskanäle](calculated-inventory-retail-channels.md).

In Commerce Site Builder können Bestandsschwellenwerte und -bereiche für ein Produkt oder eine Kategorie definiert werden. Sie bestimmen, ob der Lagerbestand als vorrätig, niedrig oder nicht vorrätig eingestuft werden kann. Einzelheiten finden Sie unter [Konfigurieren Sie Bestandpuffer und Bestandebenen](inventory-buffers-levels.md).

> [!NOTE]
> Unterstützung für Bestandsschwellen und -bereiche finden Sie in der Dynamics 365 Commerce-Version 10.0.12.

## <a name="inventory-settings"></a>Bestandeinstellungen

In Commerce werden Bestandeinstellungen unter **Seiteneinstellungen \> Erweiterungen \> Lagerverwaltung** im Site Builder definiert. Es gibt sechs Bestandseinstellungen, von denen eine veraltet ist (außer Betrieb genommen):

- **Bestandsüberprüfung in App aktivieren** – Diese Einstellung aktiviert eine Produktbestandsüberprüfung. Wenn Sie Box-, Warenkorb- und Abholmodule kaufen, wird der Produkbestand überprüft und das Hinzufügen eines Produkts zum Warenkorb nur dann ermöglicht, wenn Bestand verfügbar ist.
- **Lagerbestand basierend auf** – Diese Einstellung definiert, wie die Lagerbestände berechnet werden. Die verfügbaren Werte sind **Insgesamt verfügbar**, **Physisch verfügbar** und **Nicht verfügbar**. In Commerce Site Builder können die Bestandsschwellenwerte und -bereiche für ein Produkt oder eine Kategorie definiert werden. Die Inventar-APIs geben Produktbestandinformationen für die Eigenschaft **Insgesamt verfügbar** und **Physisch verfügbar** zurück. Der Händler entscheidet, ob der Wert **Insgesamt verfügbar** oder **Physisch verfügbar** verwendet wird, um die Anzahl der Bestände und die entsprechenden Bereiche für den Status Lagerbestand verfügbar und Lagerbestand nicht verfügbar zu bestimmen.

    Der Wert **Nicht vorrätige Schwelle** des **Lagerbestand basierend auf** Einstellungen ist ein alter (veralteter) Wert. Wenn er ausgewählt ist, wird die Bestandanzahl aus den Ergebnissen des Werts **Insgesamt verfügbar** ermittelt, aber der Schwellenwert wird durch die Einstellung **Nicht vorrätige Schwelle** numerische Einstellung definiert, die später beschrieben wird. Diese Schwellenwerteinstellung gilt für alle Produkte auf einer E-Commerce-Website. Wenn der Lagerbestand unter dem Schwellenwert liegt, gilt ein Produkt als nicht vorrätig. Ansonsten gilt es als auf Lager. Die Möglichkeiten des Werts **Nicht vorrätige Schwelle** ist begrenzt und wir empfehlen nicht, ihn in Version 10.0.12 und höher zu verwenden.

- **Bestand für mehrere Lagerorte** – Mit dieser Einstellung kann der Bestand gegen den Standardlagerort oder mehrere Lagerorte berechnet werden. Die Option **Basierend auf individuellem Lagerort** wird die Bestände basierend auf dem Standardlagerort berechnen. Alternativ kann eine E-Commerce-Seite auf mehrere Lagerorte verweisen, um die Erfüllung zu erleichtern. In diesem Fall wird die Option **Basierend auf Aggregat für Versand und Abholung Lagerorte** verwendet, um die Verfügbarkeit des Bestands anzuzeigen. Wenn ein Debitor z. B. ein Element kauft und „Versand“ als Liefermodus auswählt, kann das Element von jedem Lagerort in der Erfüllungsgruppe versendet werden, der über einen verfügbaren Bestand verfügt. Auf der Produktdetailseite (PDP) wird für den Versand die Nachricht „Auf Lager“ angezeigt, wenn ein verfügbares Versandlager in der Erfüllungsgruppe über Bestand verfügt. 

    > [!IMPORTANT] 
    > Die Einstellung **Bestandsebene für mehrere Lagerorte** ist ab der Commerce-Version 10.0.19 verfügbar. Wenn Sie ein Update von einer älteren Version von Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Anweisungen finden Sie unter [SDK- und Modulbibliotheks-Updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Inventareinstellungen für Produktlistenseiten** – Diese Einstellung definiert, wie nicht vorrätige Produkte in Produktlisten angezeigt werden, die von Produktsammlungs- und Suchergebnismodulen gerendert werden. Die verfügbaren Werte sind **In der Reihenfolge mit anderen Produkten anzeigen**, **Nicht vorrätige Produkte aus der Liste ausblenden** und **Nicht vorrätige Produkte am Ende der Liste anzeigen**. Um diese Einstellung zu verwenden, müssen Sie zunächst einige erforderliche Einstellungen in der Commerce-Zentrale konfigurieren. Weitere Informationen finden Sie unter [Produktauflistung mit Bestandserfassung](inventory-aware-product-listing.md).

    > [!IMPORTANT] 
    > Die Einstellung **Bestandseinstellungen für Produktlistenseiten** ist ab der Commerce-Version 10.0.20 verfügbar. Wenn Sie ein Update von einer älteren Version von Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Anweisungen finden Sie unter [SDK- und Modulbibliotheks-Updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Bestandsbereiche** – Diese Einstellung definiert die Bestandbereichsnachrichten, für auf lokalen Modulen angezeigt werden. Er ist nur anwendbar, wenn entweder der **Insgesamt verfügbar** oder der Wert **Physisch verfügbar** ausgewählt für die Einstellung **Lagerbestand basierend auf**. Die verfügbaren Werte sind **Alle**, **Niedrig und vergriffen** und **Ausverkauft**.

    - Wenn **Alle** ausgewählt ist, werden Meldungen für alle Bestandsbereiche angezeigt, von Auf Lager (Meldung Verfügbar) bis Nicht vorrätig (Meldung Nicht vorrätig).
    - Wenn **tief und nicht an Lager** ausgewählt ist, werden Meldungen für alle Bestandsbereiche angezeigt, ausgenommen Auf Lager (Meldung Verfügbar).
    - Wenn **Ausverkauft** ausgewählt ist, werden nur die Nachrichten Nicht vorrätig angezeigt.

- **Nicht vorrätige Schwelle** – Diese alte numerische Einstellung wird nur wirksam, wenn der Wert **Nicht vorrätige Schwelle** für die Einstellung **Lagerbestand basierend auf** ausgewählt ist.

> [!IMPORTANT] 
> Diese Einstellungen sind in Dynamics 365 Commerce 10.0.12 verfügbar. Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Module, die Bestandeinstellungen verwenden

Kaufbox, Wunschliste, Filialauswahl, Warenkorb und Warenkorbsymbolmodule verwenden Bestandeinstellungen, um die Inventarbereiche und Meldungen anzuzeigen.

In dem Beispiel in der folgenden Abbildung zeigt eine PDP die Nachricht „Auf Lager“ („Verfügbar“) an.

![Beispiel eines PDP-Moduls mit einer Nachricht „Auf Lager“.](./media/pdp-InStock.png)

Im Beispiel in der folgenden Abbildung zeigt eine PDP die Nachricht „Nicht vorrätig“ an.

![Beispiel eines PDP-Moduls mit einer Nachricht „Nicht auf Lager“.](./media/pdp-outofstock.png)

Im Beispiel in der folgenden Abbildung zeigt ein Warenkorb die Nachricht „Auf Lager“ („Verfügbar“).

![Beispiel eines Einkaufswagenmoduls mit einer Nachricht „Auf Lager“.](./media/cart-instock.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Bestandpuffer und Bestandsebenen konfigurieren](inventory-buffers-levels.md)

[Einkaufswagenmodul](add-cart-module.md)

[Kauffeldmodul](add-buy-box.md)

[Kontenverwaltungsseiten und -module](account-management.md)

[Shopauswahlmodul](store-selector.md)

[SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
