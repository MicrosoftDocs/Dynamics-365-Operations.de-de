---
title: Übersicht der Einkaufswagen- und Auschecken-Seiten
description: Dieses Thema bietet eine Übersicht über Einkaufskorb- und Auschecken-Seiten in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a9b7fe1722c366eb504882c61a337a95500c92ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000508"
---
# <a name="cart-and-checkout-pages-overview"></a>Übersicht der Einkaufswagen- und Auschecken-Seiten

[!include [banner](includes/banner.md)]

Dieses Thema bietet eine Übersicht über Einkaufskorb- und Auschecken-Seiten in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Übersicht

Auf der Einkaufskorbseite einer E-Commerce-Website werden alle Artikel angezeigt, die ein Kunde dem Einkaufskorb hinzugefügt hat. Die Einkaufskorbseite wird mithilfe des Einkaufskorbmoduls erstellt. Ein Einkaufskorbmodul ist ein Container, der verwendet wird, um alle Module zu hosten, die erforderlich sind, um Artikel im Einkaufskorb anzuzeigen. Das Einkaufskorbmodul kann auch andere Module verwenden, um die Bestellzusammenfassung und alle auf die Kundenbestellung angewendeten Aktionscodes anzuzeigen.

Auf der Auschecken-Seite einer E-Commerce-Website wird ein schrittweiser Ablauf dargestellt, in dem Kunden alle Informationen eingeben, die für die Abgabe einer Bestellung erforderlich sind. Ein Auschecken-Modul kann Module enthalten, die die Versandadresse, die Versandart, die Fakturierungsdaten, Auftragszusammenfassung und andere Informationen bearbeiten, die Kundenaufträgen zugeordnet sind.

## <a name="cart-page"></a>Einkaufskorbseite

Die Einkaufskorbseite dient als Einkaufstasche und enthält alle Artikel, die dem Einkaufskorb hinzugefügt wurden.

Die folgende Abbildung zeigt ein Beispiel für eine Einkaufskorbseite, die mit der Modulbibliothek und dem Design „Fabrikam“ erstellt wurde.

![Beispiel einer Einkaufskorbseite](./media/cart2.PNG)

Der Hauptteil der Einkaufskorbseite zeigt alle Artikel, die der Kunde dem Warenkorb hinzugefügt hat. Alle anwendbaren Rabatte werden dargestellt. Diese Rabatte umfassen komplexe Rabatte. Zu den Beispielen zählen „3 Artikel kaufen und 10 % Rabatt erhalten“ oder „Flasche und Rucksack kaufen und 10 % Rabatt erhalten“. Das Bestellzusammenfassungsmodul zeigt den Betrag an, der fällig ist, nachdem Rabatte, Versand, Steuern usw. angewendet wurden. Es gibt auch ein Werbecode-Modul, mit dem der Kunde Werbecodes anwenden oder entfernen kann.

Ein Kunde kann anonym oder als angemeldeter Benutzer einkaufen. Wenn ein Kunde angemeldet ist, bleiben die Artikel im Einkaufskorb zwischen den Sitzungen erhalten. Auf diese Weise kann der Kunde weiterhin von mehreren Geräten aus einkaufen.

Über den Einkaufskorb kann der Kunde zur Kasse gehen. Ein Kunde kann den Checkout als Gastbenutzer oder als angemeldeter Benutzer starten.

Weitere Informationen zum Erstellen einer Einkaufskorbseite erhalten Sie unter [Ein Einkaufskorbmodul einer Seite hinzufügen](add-cart-module.md).

## <a name="checkout-page"></a>Auschecken-Seite

Auf der Auschecken-Seite geben Kunden die Informationen ein, die für den Auftrag erforderlich sind.

Die folgende Abbildung zeigt ein Beispiel für die Auschecken-Seite, die mit der Modulbibliothek erstellt wurde.

![Beispiel der Auschecken-Seite](./media/Checkout.PNG)

Im Hauptteil der Auschecken-Seite werden alle Auftragsinformationen gesammelt. Zu diesen Informationen gehören die Versandadresse, die Lieferoptionen und die Zahlungsinformationen. Das Auschecken wird schrittweise ausgeführt, da die Informationen in einer bestimmten Reihenfolge eingegeben werden müssen, um verarbeitet zu werden. Beispielsweise muss die Versandadresse eingegeben werden, bevor die Versandkosten berechnet und die Zahlung autorisiert werden kann.

### <a name="shipping-address"></a>Versandadresse

Eine Versandadresse ist erforderlich, wenn Artikel versendet werden müssen. Das Format der Versandadressen für jedes Gebietsschema kann in Dynamics 365 Commerce konfiguriert werden. Wenn die Artikel beispielsweise in die USA versendet werden, muss die Versandadresse eine Straße, ein Bundesland und eine Postleitzahl enthalten. Einige grundlegende Eingabevalidierungen werden für Versandadressfelder durchgeführt, z. B. die Validierung für alphanumerische Zeichen, maximale Länge und Zahlen. Obwohl die Gültigkeit der Adresse selbst nicht überprüft wird, kann diese Überprüfung mithilfe von benutzerdefinierten Diensten von Drittanbietern durchgeführt werden.

Die Lieferadresse wird auf alle Artikel im Einkaufskorb angewendet, für die die Option „Versand“ ausgewählt ist. Wenn Sie den in der Modulbibliothek angegebenen Auschecken-Ablauf verwenden, können einzelne Einkaufskorbartikel nicht an verschiedene Adressen versendet werden. Wenn Sie diese Funktion benötigen, kann sie durch Anpassung der Auschecken-Module implementiert werden.

Nachdem die Versandadresse angegeben wurde, werden die Versandmethoden, die über den Dynamics 365 Commerce-Online-Store verfügbar sind, angezeigt. Die Versandarten und die von ihnen unterstützten Adressen können in Commerce konfiguriert werden.

### <a name="payment"></a>Zahlung

Der nächste Schritt im Auschecken-Ablauf ist die Zahlung. In E-Commerce können mehrere Zahlungsmethoden verwendet werden, um Bestellungen aufzugeben, z. B. Kreditkarten, Geschenkkarten und Treuepunkte. Eine Kombination dieser Zahlungsmethoden kann ebenfalls verwendet werden. Abhängig von den verwendeten Zahlungsmethoden können zusätzliche Informationen erforderlich sein. Beispielsweise erfordert eine Kreditkartenzahlung eine Rechnungsadresse. Kreditkartenzahlungen werden über den Adyen Payment Connector abgewickelt.

#### <a name="loyalty-points"></a>Treuepunkte

Während des Auschecken-Ablaufs kann ein Kunde, der Mitglied eines Treueprogramms ist und Treuepunkte gesammelt hat, diese Treuepunkte für eine Bestellung einlösen. Das Treuepunkte-Modul wird nur angezeigt, wenn der Kunde bereits eine Treue-Mitgliedschaft besitzt. Für Nichtmitglieder und Gastnutzer ist dieses Modul ausgeblendet.

#### <a name="gift-cards"></a>Geschenkkarten

Mit der Modulbibliothek können interne Geschenkkarten für eine Bestellung eingelöst werden. Um eine interne Geschenkkarte zu beantragen, muss der Kunde angemeldet sein. Für zusätzliche Sicherheit empfehlen wir, dass Sie den Ablauf anpassen, indem Sie eine persönliche Identifikationsnummer (PIN) für interne Geschenkkarten verwenden.

### <a name="signed-in-and-guest-users"></a>Angemeldete und Gastbenutzer

Der Debitor kann den Auschecken-Prozess als Gastbenutzer oder angemeldeter Benutzer abschließen. Wenn sich der Debitor anmeldet, werden Kontoinformationen wie gespeicherte Lieferadressen und gespeicherte Kreditkartendaten automatisch abgerufen.

### <a name="order-summary"></a>Auftragszusammenfassung

Das Ausschecken zeigt eine Zusammenfassung der Positionen im Einkaufskorb an, damit der Kunde die Bestellung überprüfen kann, bevor er sie aufgibt. Die Positionen können während des Auschecken-Vorgangs nicht bearbeitet werden. Es wird jedoch ein Link zum Einkaufskorb bereitgestellt, falls der Benutzer zurückkehren und Positionen bearbeiten möchte.

Nachdem der Debitor Versand- und Rechnungsinformationen angegeben hat, zeigt die Bestellübersicht den Betrag an, der fällig ist, nachdem Treuepunkte, Geschenkkarten und andere Zahlungen abgezogen wurden.

### <a name="order-confirmation-and-email"></a>Auftragsbestätigung und E-Mail

Wenn der Debitor eine Bestellung aufgibt, wird eine Bestätigungsnummer bereitgestellt. Zu diesem Zeitpunkt wurde die Zahlung autorisiert, aber nicht belastet. Die Zahlung wird erst belastet, wenn die Bestellung erfüllt ist (d. h. wenn sie entweder versendet oder abgeholt wird).

Nachdem ein Auftrag erstellt wurde, wird eine Auftragsbestätigungs-E-Mail an den Debitor gesendet.

Weitere Informationen zum Erstellen einer Auschecken-Seite erhalten Sie unter [Einer Seite ein Auschecken-Modul hinzufügen](add-checkout-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht der Startseite](quick-tour-home-page.md)

[Übersicht der Produktdetailseiten](quick-tour-pdp.md)

[Übersicht der Kontenverwaltungsseiten](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]