---
title: Kreditorenrechnungsdaten
description: In diesem Thema werden die Daten beschrieben, die auf Kreditorenrechnungen erscheinen. Außerdem wird erläutert, wie Sie das System so einrichten, dass es das Buchungsdatum automatisch anpasst.
author: sunfzam
ms.date: 08/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: a066f828b47f297b8ad520b9eb0f4f311d49b111
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647890"
---
# <a name="vendor-invoice-dates"></a>Kreditorenrechnungsdaten

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Daten beschrieben, die auf Kreditorenrechnungen erscheinen. Außerdem wird erläutert, wie Sie das System so einrichten, dass es das Buchungsdatum automatisch anpasst.

Auf der Seite **Ausstehende Lieferantenrechnung detailliert** zeigt der Rechnungskopf vier Daten an: das Eingangsdatum der Rechnung, das Rechnungsdatum, das Buchungsdatum und das Fälligkeitsdatum. Beim Erstellen einer Kreditorenrechnung werden standardmäßig die folgenden Daten eingegeben:

- **Rechnungseingangsdatum** – Dieses Feld wird auf das aktuelle Systemdatum gesetzt.
- **Buchungsdatum** – Dieses Feld wird auf das aktuelle Systemdatum gesetzt. 
- **Fälligkeitsdatum** – Das Datum in diesem Feld wird basierend auf dem Buchungsdatum und den Zahlungsbedingungen berechnet.
- **Rechnungsdatum** – Dieses Feld ist standardmäßig leer. Allerdings können Sie einen Wert in diesem Feld eingeben. In diesem Fall wird das Datum im Feld **Fälligkeitsdatum** basierend auf dem Rechnungsdatum und den Zahlungsbedingungen neu berechnet.

Manchmal kann sich eine Kreditorenrechnung noch lange nach Ablauf des Zeitraums im Status „Ausstehend“ befinden. Bei der Buchungsreife wird weiterhin das alte Buchungsdatum der vergangenen Buchungsperiode verwendet. Dieser Zeitraum ist nun jedoch abgelaufen. Daher muss ein Kreditorenbuchhalter alle Buchungsdaten für alle zuvor erstellten ausstehenden Rechnungen manuell in die neue Buchungsperiode ändern.

Mit der in diesem Thema beschriebenen Funktion können Sie das System so einrichten, dass es das Buchungsdatum automatisch an die Geschäftsanforderungen anpasst.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parameter zur automatischen Anpassung des Buchungsdatums der Kreditorenrechnung

Führen Sie diese Schritte aus, damit das System das Buchungsdatum für Kreditorenrechnungen automatisch anpassen kann.

1.  Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
2.  Wählen Suie auf der Registerkarte **Hauptbuch und Umsatzsteuer** im Feld **Veröffentlichungsdatum automatisch anpassen** einen der folgenden Werte aus:

    - **Keine Änderung** – Das System ändert das Buchungsdatum beim Buchen nicht automatisch. Dieser Wert ist standardmäßig ausgewählt.
    - **Buchungsdatum immer auf Systemdatum ändern** – Das System ändert das Buchungsdatum beim Buchen automatisch auf das Systemdatum.
    - **Buchungsdatum in Systemdatum ändern, wenn Buchungsdatumsperiode geschlossen oder gesperrt ist** – Das System ändert beim Buchen das Buchungsdatum auf das Systemdatum, jedoch nur, wenn die entsprechende Periode des Buchungsdatums den Status **Abgeschlossen** oder **Gesperrt** hat.
    - **Buchungsdatum in den ersten Tag der neuen Periode ändern, wenn Buchungsdatumsperiode geschlossen oder gesperrt ist** – Das System ändert das Buchungsdatum auf den ersten Tag der neuen offenen Periode, jedoch nur, wenn die entsprechende Periode des Buchungsdatums den Status **Abgeschlossen** oder **Gesperrt** hat.

## <a name="impact-of-posting-date-changes"></a>Auswirkungen von Änderungen des Buchungsdatums

Wenn das Buchungsdatum einer offenen Kreditorenrechnung geändert wird, hat die Änderung folgende Auswirkungen:

- **Fälligkeitsdatum**

    - Wenn das Feld **Rechnungsdatum** leer ist, wird das Fälligkeitsdatum basierend auf dem neuen Buchungsdatum und den Zahlungsbedingungen neu berechnet.
    - Wenn das Feld **Rechnungsdatum** zuvor festgelegt wurde, hat die Änderung des Buchungsdatums keinen Einfluss auf das Fälligkeitsdatum.

- **Skontodatum**

    - Wenn das Feld **Rechnungsdatum** leer ist, wird das neue Buchungsdatum zur Berechnung des Skontos verwendet.
    - Wenn das Feld **Rechnungsdatum** zuvor gesetzt wurde, wird der Skonto nicht geändert.

- **Wechselkurs** – Das Wechselkursdatum wird durch die Einstellung der Option **Kreditorenbuchhaltung anhand des Rechnungsdatums aktualisieren** auf der Registerkarte **Rechnung** der Seite **Kreditorenparameter** (**Kreditoren \> Einrichtung \> Kreditorenparameter**) bestimmt.

    - Wenn diese Option auf **Ja** eingestellt ist, wird das Rechnungsdatum verwendet und die Änderung des Buchungsdatums wirkt sich nicht auf den Wechselkurs aus.
    - Wenn diese Option auf **Nein** eingestellt ist, wird das Buchungsdatum zur Berechnung des Umrechnungskurses verwendet. Wenn das Buchungsdatum aktualisiert wird, werden Buchhaltungs- und Berichtsbeträge neu berechnet. Daher muss die Übereinstimmungsvalidierung erneut durchgeführt werden.

## <a name="validation"></a>Prüfung

Zwei weitere Felder auf der Registerkarte **Rechnung** der Seite **Kreditorenparameter** (**Kreditoren \> Einrichtung \> Kreditorenparameter**) beeinflussen die Rechnungsbearbeitung:

- Wenn das Feld **Überprüfen Sie die verwendete Rechnungsnummer** auf **Dubletten innerhalb des Geschäftsjahres ablehnen** gesetzt ist, verwendet das System das Buchungsdatum, um bei der Rechnungsbuchung auf doppelte Rechnungen zu prüfen.
- Wenn das Feld **Dokumentdatum auf Kreditorenrechnung verlangen** auf **Fehleroption** gesetzt ist, ist das **Rechnungsdatum im ausstehenden Rechnungskopf** erforderlich. Wenn das Rechnungsdatum nach dem Buchungsdatum liegt, zeigt das System eine Fehlermeldung an.
