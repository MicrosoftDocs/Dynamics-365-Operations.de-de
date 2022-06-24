---
title: Kundenbestellungsabholung am POS bearbeiten
description: In diesem Artikel werden die Funktionen erläutert, die in der POS-Anwendung (Point of Sale) für die Verarbeitung von Kundenauftragsabholungen verfügbar sind.
author: Hhainesms
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0a886f156fff96f3b7e6026c405d3c8700d57f62
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910468"
---
# <a name="process-customer-order-pickups-in-pos"></a>Kundenbestellungsabholung am POS bearbeiten

[!include [banner](includes/banner.md)]

Wenn eine [Kundenbestellung](customer-orders-overview.md) für die Abholung im Geschäft erstellt wird, kann ein Ladenbenutzer mithilfe der POS-Anwendung (Point of Sale) die Abholung des Bestands starten. POS führt die endgültige Zahlungserfassung nach Bedarf durch. Es werden auch der Bestand und die Finanzbuchung für die abgeholten Mengen abgeschlossen.

Wenn Sie ein Ladenbenutzer sind, können Sie die Abholung entweder mit dem Vorgang **Bestellung zurückrufen** oder **Auftragsabwicklung** am POS durchführen. Um den **Abholen**-Vorgang verfügbar, müssen Sie zuerst einen der folgenden Schritte ausführen:

- Um den **Bestellung zurückrufen**-Vorgang zu verwenden, suchen Sie die Bestellung, die abgeholt werden soll, und wählen Sie sie aus.
- Um den **Auftragsabwicklung**-Vorgang zu verwenden, suchen Sie mindestens eine Bestellposition und wählen Sie sie aus.

Wenn die ausgewählte Bestellung oder Bestellpositionen nicht für die Abholung in diesem bestimmten Geschäft konfiguriert sind oder wenn die Bestellung bereits vollständig abgeholt wurde, ist der **Abholen**-Vorgang ist nicht verfügbar.

![Abholvorgang.](media/pickupoperation.png)

In Microsoft Dynamics 365 Commerce Version 10.0.17 und höher kann die Funktion **Verbesserte Benutzererfahrung bei der Abwicklung der Bestellungsabholung am Point of Sale** über die Funktionsverwaltung in der Commerce-Zentralverwaltung aktiviert werden. Wenn diese Funktion deaktiviert ist, können Benutzer keine Abholmengen auswählen. Standardmäßig ist die volle für die Position bestellte Menge auch die Menge, die abgeholt wird. Diese Erfahrung kann problematisch sein, da Benutzer möglicherweise vergessen, einige Artikel zur Abholung auszuwählen, wenn sie die Abholung durch Auftragserfüllung durchführen.

Die Funktion **Verbesserte Benutzererfahrung bei der Abwicklung der Bestellungsabholung am Point of Sale** bietet Benutzern mehr Kontrolle über die Auswahl der Produkte, die abgeholt werden sollen, und über die Menge der Produkte, die abgeholt werden. Benutzer müssen nicht jede Position des Kundenauftrags auf der Seite zur Auftragserfüllung auswählen, bevor sie **Abholen** auswählen. Alle Artikel, die abgeholt werden können, werden angezeigt. Benutzer können mehrere Positionen für die Abholung angeben, auch wenn nur eine Produktposition ausgewählt ist.

Wenn die Funktion **Verbesserte Benutzererfahrung bei der Abwicklung der Bestellungsabholung am Point of Sale** aktiviert ist und Sie wählen den **Abholen**-Vorgang, wird das **Abholen**-Dialogfeld angezeigt. Dort können Sie die Artikel und Mengen auswählen, die abgeholt werden sollen. Standardmäßig gilt jede bestellte Menge mit einem Lagerbestand in einem kommissionierten oder verpackten Zustand als abholfähig. Standardmäßig ist diese Menge als Abholmenge festgelegt. Sie können die eingegebene Menge ändern, vorausgesetzt, die Menge ist nicht 0 (Null) und überschreitet nicht die gesamte offene (d. h. nicht in Rechnung gestellte) Menge für die ausgewählte Position.

![Abholen-Dialogfeld.](media/pickupselect.png)

Nachdem Sie die Mengen ausgewählt haben, die abgeholt werden sollen, und dann **Abholen** auswählen, wird die Transaktionsseite angezeigt. Wenn die [Omni-Channel-Zahlungen](omni-channel-payments.md)-Funktion aktiviert ist und vorautorisierte Kreditkartenzahlungen gespeichert sind, müssen Sie die Zahlung anwenden.

Auf der Transaktionsseite berechnet das System die fälligen Beträge, indem es den Gesamtbetrag berechnet, der für die ausgewählten Abholposten fällig ist, und anschließend alle zuvor angewendeten Einzahlungen oder autorisierten Kreditkartenzahlungen abzieht. Sie müssen die Zahlung verarbeiten, um die Abholung abzuschließen. Wenn die [Bildschirmgestaltung](pos-screen-layouts.md) der Transaktionsseite so konfiguriert ist, dass sie den Vorgang **Transaktion abschließen** enthält, wenn kein Betrag fällig ist, können Sie die Transaktion abschließen, ohne eine Zahlungsmethode auszuwählen. Wenn der Vorgang **Transaktion abschließen** nicht verfügbar ist, können Sie den Link **0,00 USD Betrag fällig** im **Summe**-Bereich auswählen, um die Transaktion abzuschließen, ohne eine Zahlungsmethode auswählen zu müssen.

![Transaktionsseite für eine Kundenauftragsabholung.](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Abholpositionen oder -mengen ändern

Wenn Sie die Abholmenge ändern müssen, nachdem Sie die Artikel ausgewählt haben, die abgeholt werden sollen, können Sie **Menge festlegen** auswählen. Sie können die Abholmenge nicht auf **0** (Null) festlegen oder auf einen Wert erhöhen, der die nicht in Rechnung gestellte Menge überschreitet, die für die bestellte Position verbleibt. Wählen Sie **Transaktion stornieren** aus, um eine Abholposition aus dem Einkaufswagen der Transaktion zu entfernen. Die aktuelle Transaktion wird gestoppt und der Ablauf für den Vorgang **Abholen** wird neu gestartet.

Wenn die **Verbesserte Benutzererfahrung bei der Abwicklung der Bestellungsabholung am Point of Sale**-Funktion aktiviert ist, können Organisationen eine Schaltfläche für den Vorgang **Abholpositionen ändern** dem Bildschirmlayout der Transaktionsseite hinzufügen. Nachdem Sie den Einkaufswagen der Transaktion am POS erstellt und Artikel ausgewählt haben, können Sie **Abholpositionen ändern** auswählen, wenn Sie die Abholartikel ändern müssen, aber nicht die gesamte Transaktion stornieren möchten. In dem **Abholpositionen ändern**-Dialogfeld, das angezeigt wird, können Sie die Abholpositionen und -mengen ändern. Der Einkaufswagen der Transaktion wird dann aktualisiert, um Ihre Änderungen widerzuspiegeln.

![Dialogfeld „Abholartikel ändern“.](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]