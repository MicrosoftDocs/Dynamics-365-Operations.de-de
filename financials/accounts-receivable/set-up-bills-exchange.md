---
title: Einrichten von Wechseln
description: In diesem Thema werden die Schritte zum Einrichten von Wechseln.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Einrichten von Wechseln

In diesem Thema werden die Schritte zum Einrichten von Wechseln.

Bei einem Wechsel handelt es sich um den schriftlichen oder elektronischen Auftrag eines Kunden, der angibt, mit dem ein Dritter, normalerweise eine Bank, einen angegebenen Betrag an das Unternehmen zu zahlen. Bei Verwendung eines Wechsels als Zahlungsmittel für eine Auftrags- oder Freitextrechnung erfolgt eine Habenbuchung auf dem Debitorenkonto. Diese Habenbuchung ist durch den Wechsel so lange gesichert, bis der Debitor den Wechsel an die Bank bezahlt. Normalerweise Gleichen Sie die Rechnung zum Fälligkeitsdatum mit dem Wechsel ausgeglichen. Nachdem die Benachrichtigung über die Einlösung des Wechsels von der Bank eingegangen ist, kann der Wechsel abgeschlossen werden. Sie können eines Wechsels von der Bank zu jedem der folgenden Zeitpunkte gezogen werden:

-   Zum Fälligkeitsdatum. Durch diesen Ansatz Fall wird auch als Inkassorimesse bezeichnet.
-   Vor dem Fälligkeitsdatum (üblicherweise zum Skontodatum, das in den Zahlungsbedingungen angegeben wird, die für den Debitor eingerichtet werden. Beim Ausführen der Buchung wird der Skontobetrag auf ein Ausgabenkonto gebucht. Der Restbetrag verbleibt als Verbindlichkeit, bis die Zahlung des Debitors bei der Bank eingeht. Durch diesen Ansatz Fall wird auch als Zum Diskont einreichen.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Einrichten von Buchungsprofilen für Wechsel
Verwenden Sie die Seite ** Debitoren-Buchungsprofile **, um Buchungsprofile einrichten, die Sie für Wechsel, protestierte Wechsel, Inkassorimessen und Skontorimessen zum Diskont verwenden können. ** Sammelkonto ** Wählen Sie im Feld das Sammelkonto aus, auf das die Beträge von Wechseln gebucht werden sollen. Dieses Konto wird, abhängig vom Typ der Wechsel buchung belastet oder gutgeschrieben:
-   Für Wechsel wird dieses Konto belastet, wenn ein Wechsel gebucht wird, und es wurde eine Gutschrift, wenn die Buchung einer Diskont- oder Inkassorimesse erfolgt auf diesem Konto eine Sollbuchung.
-   Wechsel protestieren: Durch die Buchung eines protestierten Wechsels erfolgt auf diesem Konto eine Sollbuchung.
-   Inkassorimesse: Durch die Buchung einer Inkassorimesse erfolgt auf diesem Konto eine Sollbuchung.
-   Skontorimesse: Durch die Buchung einer Skontorimesse erfolgt auf diesem Konto eine Sollbuchung.

Auf dem Bankkonto ** ** Feld das Bargeldkonto aus, um Beträge von Wechseln gebucht werden sollen. Dieses Konto wird durch den Ausgleich eines Wechsels belastet. ** Mehrwertsteuervorauszahlungen ** Wählen Sie im Feld das Sammelkonto aus, auf das die Mehrwertsteuerbeträge gebucht werden, wenn ein Wechsel für Vorauszahlungen verwendet werden. Wählen Sie im ** Verbindlichkeiten für Diskontverbindlichkeiten ** Feld das Konto aus, auf das der Skontobetrag für Diskontrimessen gebucht werden. Auf diesem Konto erfolgt beim Buchen einer Diskontrimesse eine Habenbuchung.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Einrichten von Debitorenparametern für Wechsel
** Debitorenparameter ** Auf der Seite werden die standardmäßigen Buchungsprofilen für Wechsel auf die ** Sachkonto und Mehrwertsteuer ** Registerkarte eingegeben. Nummernkreise werden Nummernkreise ** ** auf der Registerkarte definiert.
Einrichten von Journalen für Wechsel
------------------------------------------

** Erfassungsnamen ** Auf der Seite erstellen Sie mindestens fünf Journale ein, die für Wechsel verwendet wird. Hierbei gelten die Erfassungstypen:
-   ** Debitorenziehenwechsel ** - Erstellen Sie ein Journal für die Erfassung zum Ziehen von Wechseln.
-   ** Debitorenprotestwechsel ** - Erstellen Sie ein Journal für die Erfassung.
-   ** Debitor gezogene Wechsel ** – Dient zum Erstellen eines Journals für die neu gezogene Wechsel erneut.
-   ** Debitorenbankrimesse ** - Erstellen Sie ein Journal für die Rimesseerfassung.
-   ** Debitorenbankwechsel ** - Erstellen Sie ein Journal für die. Erfassung für ausgeglichene Wechsel

Auf der Erfassungsbelegseite für jede Wechselerfassung, geben Sie Informationen zum Wechsel ** ** Wechsel auf der Registerkarte ein. Nachdem die Wechselerfassungspositionen gebucht wurden, können Sie auf der Wechselerfassungsabfrage ** ** Seite und der ** Wechselstatistik ** Seite anzeigen.
Einrichten von Zahlungsmethoden für Wechsel
-----------------------------------------------

** Zahlungsmethoden ** auf der Seite Einstellungen mindestens eine Zahlungsmethode für Wechsel. Sollten Sie Kunde bei mehreren Banken sein, richten Sie eine Zahlungsmethode ein, die dem Rimesseformat entspricht, das jeder Bank für Wechsel sind.
Einrichten von Zahlungsgebühren für Wechsel
-----------------------------------------

Bei einer Zahlungsgebühr handelt es sich um eine Belastung für das Einziehen der Zahlungen von Debitoren. Mehreren zugeordnet werden können Zahlungsgebühreneinstellungspositionen jede Zahlungsgebühr. Zudem können Sie verwenden, um zu steuern, wie Standardbeträge für Zahlungsgebühren berechnet werden. Sie können beispielsweise Einstellungen für Zahlungsmethoden, Zahlungsspezifikationen, Währungen und Zeitperioden einrichten. Zudem können Sie einen Prozentsatz oder einen Betrag auch erstellen, der auf Tagesintervallen basierenden ist. Sie können beispielsweise einen Zinssatz einrichten, der auf der Zeit basiert, die, eine Zahlung überfällig ist. Erhebt eine Bank unterschiedliche Gebühren für unterschiedliche Rimessetypen, z ** Inkasso ** oder ** Rabatt **, muss für jeden Rimessetyp eine eigene Zahlungsgebührposition eingerichtet.
Einrichten von Rimessegebühren für Bankrimessedateien
------------------------------------------------

** Bankkonten ** Auf der Seite können Sie die Möglichkeit zum Einrichten von Rimessegebühren Bankgebühren dieses für jede Rimessedatei, die generiert wird. Die Buchung der Rimessegebühren erfolgt, nachdem die Rimesse bestätigt wurde und die anfallenden Gebührenbeträge feststehen. Rimessegebühren unterscheiden sich von den Zahlungsgebühren, die von Debitoren eingezogen werden und mit Erfassungspositionen verknüpft.
Einrichten von Dokumentlayouts für Wechsel
---------------------------------------------

** ** Bankkonten auf der Seite klicken Sie ** ** Einstellungen, und geben Sie auf das erforderliche Dokumentlayout an für jedes Bankkonto, erforderlich, das zum Generieren von Wechseldokumenten verwendet.
Einrichten von Debitoren für Wechsel
--------------------------------------

** ** Debitoren auf der Seite für jeden Debitor, der einer Bezahlung zugestimmt hat, indem Sie einen Wechsel verwendete, kann eine Standardzahlungsmethode für Wechsel Zahlungsausfälle ** ** auf der Registerkarte einrichten.




