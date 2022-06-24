---
title: Kreditorenrechnungstermine
description: In diesem Artikel werden die Daten beschrieben, die auf Kreditorenrechnungen erscheinen. Außerdem wird erläutert, wie Sie das System so einrichten, dass es das Buchungsdatum automatisch anpasst.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 943a84407d022c2c05bc534a35a2b5d44a94653e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876411"
---
# <a name="vendor-invoice-dates"></a>Kreditorenrechnungstermine

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Daten beschrieben, die auf Kreditorenrechnungen erscheinen. Außerdem wird erläutert, wie Sie das System so einrichten, dass es das Buchungsdatum automatisch anpasst.

Auf der Seite **Ausstehende Lieferantenrechnung detailliert** zeigt der Rechnungskopf vier Daten an: das Eingangsdatum der Rechnung, das Rechnungsdatum, das Buchungsdatum und das Fälligkeitsdatum. Beim Erstellen einer Kreditorenrechnung werden standardmäßig die folgenden Daten eingegeben:

- **Rechnungseingangsdatum** – Dieses Feld wird auf das aktuelle Systemdatum gesetzt.
- **Buchungsdatum** – Dieses Feld wird auf das aktuelle Systemdatum gesetzt. 
- **Fälligkeitsdatum** – Das Datum in diesem Feld wird basierend auf dem Buchungsdatum und den Zahlungsbedingungen berechnet.
- **Rechnungsdatum** – Dieses Feld ist standardmäßig leer. Allerdings können Sie einen Wert in diesem Feld eingeben. In diesem Fall wird das Datum im Feld **Fälligkeitsdatum** basierend auf dem Rechnungsdatum und den Zahlungsbedingungen neu berechnet.

Manchmal kann sich eine Kreditorenrechnung noch lange nach Ablauf des Zeitraums im Status „Ausstehend“ befinden. Bei der Buchungsreife wird weiterhin das alte Buchungsdatum der vergangenen Buchungsperiode verwendet. Dieser Zeitraum ist nun jedoch abgelaufen. Daher muss ein Kreditorenbuchhalter alle Buchungsdaten für alle zuvor erstellten ausstehenden Rechnungen manuell in die neue Buchungsperiode ändern.

Mit der in diesem Artikel beschriebenen Funktion können Sie das System so einrichten, dass es das Buchungsdatum automatisch an die Geschäftsanforderungen anpasst.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parameter zur automatischen Anpassung des Buchungsdatums der Kreditorenrechnung

Führen Sie diese Schritte aus, damit das System das Buchungsdatum für Kreditorenrechnungen automatisch anpassen kann.

1.  Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
2.  Wählen Suie auf der Registerkarte **Hauptbuch und Umsatzsteuer** im Feld **Veröffentlichungsdatum automatisch anpassen** einen der folgenden Werte aus:

    - **Keine Änderung** – Das System ändert das Buchungsdatum beim Buchen nicht automatisch. Dieser Wert ist standardmäßig ausgewählt.
    - **Buchungsdatum immer auf Systemdatum ändern** – Das System ändert das Buchungsdatum beim Buchen automatisch auf das Systemdatum.
    - **Buchungsdatum in Systemdatum ändern, wenn Buchungsdatumsperiode geschlossen oder gesperrt ist** – Das System ändert beim Buchen das Buchungsdatum auf das Systemdatum, jedoch nur, wenn die entsprechende Periode des Buchungsdatums den Status **Abgeschlossen** oder **Gesperrt** hat.
    - **Buchungsdatum in den ersten Tag der neuen Periode ändern, wenn Buchungsdatumsperiode geschlossen oder gesperrt ist** – Das System ändert das Buchungsdatum auf den ersten Tag der neuen offenen Periode, jedoch nur, wenn die entsprechende Periode des Buchungsdatums den Status **Abgeschlossen** oder **Gesperrt** hat.

> [!NOTE]
> Liegt das automatisch angepasste neue Buchungsdatum in einem neuen Geschäftsjahr, wird das Buchungsdatum der Rechnung nicht fortgeschrieben. Der Benutzer erhält eine Fehlermeldung „Das Geschäftsjahr hat sich geändert. Bitte überprüfen Sie das Buchungsdatum und geben Sie es erneut ein.“ Das Rechnungsbuchungsdatum muss zum Buchen auf das neue Geschäftsjahrsdatum aktualisiert werden.

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
