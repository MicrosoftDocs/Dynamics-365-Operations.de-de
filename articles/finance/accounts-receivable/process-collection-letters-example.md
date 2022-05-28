---
title: Mahnschreiben verarbeiten – Beispiel
description: In diesem Thema wird ein Beispiel vorgestellt, das den Prozess des Erstellens, Druckens und Versendens von Mahnschreiben zeigt.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1bb1889e9450685f7b6a5000e2ef81d1a65f1b51
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721814"
---
# <a name="process-collection-letters-example"></a>Mahnschreiben verarbeiten – Beispiel

[!include [banner](../../includes/banner.md)]

In diesem Thema wird ein Beispiel vorgestellt, das den Prozess des Erstellens, Druckens und Versendens von Mahnschreiben zeigt. Das Beispiel basiert auf der Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** in Kredit und Inkasso. Es werden Daten des USMF-Demounternehmens und eines neuen Kunden, US-045, verwendet.

Rufen Sie zu Beginn **Debitorenkonten \> Debitoren \> Alle Debitoren** auf. Wählen Sie die Option **Neu** aus, und geben Sie dann die erforderlichen Informationen ein, um den Debitoren US-045 zu erstellen.

Wenn Sie fertig sind, führen Sie die folgenden Schritte aus.

1. Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreibensequenz einrichten** auf, und richten Sie die Mahnschfreibensequenz wie in der folgenden Tabelle gezeigt ein, die dem Debitorenbuchungsprofil zugewiesen ist.

|     Mahnschreibencode      |     Beschreibung                           |     Währung      |     Hauptkonto        |     Gebühren in Währung     |     Minimum über        |     Zu sperrende Tage      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Mahnschreiben 1         |     Zweite Benachrichtigung mit Gebühr        |     USD           |                           |     0,00                  |     0,00                  |     2                 |
|     Mahnschreiben 2         |     Zweite Benachrichtigung mit Gebühr        |     USC           |     403150                |     20.00                 |     10.00                 |     3                 |
|     Inkasso                    |     Letzte Benachrichtigung mit Gebühr         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

Die folgende Abbildung zeigt die Informationen in der Tabelle so, wie sie auf der Seite **Mahnschreiben** dargestellt würden. 

[![Einrichten von Mahnschreibensequenzen.](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Sie müssen jetzt die beiden Parameter einstellen, die für dieses Beispiel erforderlich sind.

2. Rufen Sie **Kredit und Inkasso \> Einrichtung \> Debitorenparameter** auf, und befolgen Sie diese Schritte:

    1. Stellen Sie auf der Registerkarte **Inkasso** die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Ja** ein.
    2. Vergewissern Sie sich, dass das Feld **Erstellen eines Mahnschreibens pro** auf **Debitor** eingestellt ist.

    [![Einstellen von Debitorenparametern für Kredite und Inkassos.](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Rufen Sie **Debitoren \> Rechnungen \> Alle Freitextrechnungen** auf, wählen Sie **Neu** aus, und befolgen Sie dann diese Schritte:

    1. Wählen Sie im Feld **Debitorenkonto** die Option **US-045** aus.
    2. Geben Sie im Feld **Rechnungsdatum** **1/15/2021** ein.
    3. Geben Sie im Feld **Fälligkeitsdatum** den Wert **1/16/2021** ein.
    4. Geben Sie auf der Registerkarte **Rechnungspositionen** im Feld **Hauptkonto** den Wert **401100** ein.
    5. Geben Sie im Feld **Einzelpreis** die Zahl **500.00** ein.
    6. Wählen Sie **Buchen** aus.

    Sie müssen jetzt zwei Gutschriften für den Debitoren eingeben.

4. Wählen Sie **Hinzufügen** aus, und befolgen Sie die folgenden Schritte:

    1. Wählen Sie im Feld **Kundenkonto** die Option **US-045** aus.
    2. Geben Sie im Feld **Rechnungsdatum** **1/15/2021** ein.
    3. Geben Sie im Feld **Fälligkeitsdatum** den Wert **1/16/2021** ein.
    4. Geben Sie auf der Registerkarte **Rechnungspositionen** im Feld **Hauptkonto** den Wert **401100** ein.
    5. Geben Sie im Feld **Preis je Einheit** die Zahl **-100,00** ein.
    6. Wählen Sie **Buchen** aus.

5. Wiederholen Sie Schritt 4, aber geben Sie **-200,00** im Feld **Preis je Einheit** ein.
6. Rufen Sie **Debitorenkonten \> Debitoren \> Alle Debitoren** auf, und wählen Sie Debitor **US-045** aus. Wählen Sie dann im Aktionsbereich die Option **Transaktionen \> Transaktionen** aus, um die Debitortransaktionen zu überprüfen, die Sie zuvor gebucht haben.

    [![Überprüfen der gebuchten Debitortransaktionen.](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Nun müssen Sie Mahnschreiben für Debitor US-045 erstellen.

7. Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben erstellen** auf, und befolgen Sie diese Schritte:

    1. Stellen Sie die Optionen **Rechnung** und **Gutschrift** auf **Ja** ein.

        Standardmäßig sollte das Feld **Mahnschreiben** auf **Mahnung pro Debitor** eingestellt sein.

    2. Geben Sie im Feld **Datum des Mahnschreibens** den Wert **1/19/2021** ein.
    3. Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter** aus, und fügen Sie dann im Feld **Debitorenkonto** den Debitor **US-045** hinzu.
    4. Wählen Sie **OK**.
    5. Wählen Sie **OK** aus, um Mahnschreiben zu erstellen.

8. Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben prüfen und verarbeiten** auf, und befolgen Sie diese Schritte:

    1. Beachten Sie, dass der Mahnschreibencode sowohl in der Kopfzeile als auch in den Transaktionspositionen **Mahnschreiben 1** lautet, da es sich bei diesem Mahnschreiben um das erste Mahnschreiben in der Sequenz handelt. (Um sich die Transaktionspositionen anzeigen zu lassen, müssen Sie möglicherweise das Inforegister **Transaktionen** auswählen.)

   [![Sicherstellen, dass in der Kopfzeile und den Positionen derselbe Mahnschreibencode angezeigt wird.](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Wählen Sie im Aktionsbereich **Buchen** aus.
    3. Geben Sie im Feld **Buchungsdatum** den Wert **1/19/2021** ein.

    Nun müssen Sie erneut Mahnschreiben für Debitor US-045 erstellen.

9. Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben erstellen** auf, und befolgen Sie diese Schritte:

    1. Stellen Sie die Optionen **Rechnung** und **Gutschrift** auf **Ja** ein.

        Standardmäßig sollte das Feld **Mahnschreiben** auf **Mahnung pro Debitor** eingestellt sein.

    2. Geben Sie im Feld **Datum des Mahnschreibens** den Wert **1/23/2021** ein.
    3. Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter** aus, und fügen Sie dann im Feld **Debitorenkonto** den Debitor **US-045** hinzu.
    4. Wählen Sie **OK**.
    5. Wählen Sie **OK** aus, um Mahnschreiben zu erstellen.

10. Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben prüfen und verarbeiten** auf, und befolgen Sie diese Schritte:

    1. Beachten Sie, dass der Mahnschreibencode in der Kopfzeile **Mahnschreiben 1** lautet. Der Code in den Transaktionspositionen lautet jedoch **Mahnschreiben 2**.

   [![Sicherstellen, dass in der Kopfzeile und den Positionen verschiedene Mahnschreibencodes angezeigt werden.](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Die Codes sind unterschiedlich, da die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Ja** eingestellt ist.

  2. Buchen Sie nicht dieses Mahnschreiben.

11. Rufen Sie **Kredit und Inkasso \> Einrichtung \> Debitorenparameter** auf, und stellen Sie dann auf der Registerkarte **Inkasso** die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Nein** ein.

    [![Einstellen der Option „Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren“ auf „Nein“.](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Nun müssen Sie erneut Mahnschreiben für Debitor US-045 erstellen.

12. Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben erstellen** auf, und befolgen Sie diese Schritte:

    1. Stellen Sie die Optionen **Rechnung** und **Gutschrift** auf **Ja** ein.

        Standardmäßig sollte das Feld **Mahnschreiben** auf **Mahnung pro Debitor** eingestellt sein.

    2. Geben Sie im Feld **Datum des Mahnschreibens** den Wert **1/23/2021** ein.
    3. Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter** aus, und fügen Sie dann im Feld **Debitorenkonto** den Debitor **US-045** hinzu.
    4. Wählen Sie **OK**.
    5. Wählen Sie **OK** aus, um Mahnschreiben zu erstellen.

13. Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben prüfen und verarbeiten** auf, und beachten Sie, dass der Mahnschreibencode sowohl in der Kopfzeile als auch in den Transaktionspositionen **Mahnschreiben 2** lautet.

    [![Erneutes Anzeigen, dass in der Kopfzeile und den Positionen derselbe Mahnschreibencode angegeben ist.](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Derselbe Code erscheint an beiden Stellen, da die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** jetzt auf **Nein** eingestellt ist.
