---
title: Einrichten von Wechseln
description: In diesem Thema werden die Schritte zum Einrichten von Wechseln.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4dfc6cc2fcbca18f3dde833917ae68a5f254643b
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bills-of-exchange"></a>Einrichten von Wechseln

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Schritte zum Einrichten von Wechseln.

Bei einem Wechsel handelt es sich um den schriftlichen oder elektronischen Auftrag eines Kunden, mit dem ein Dritter (üblicherweise eine Bank) angewiesen wird, einen angegebenen Betrag an das Unternehmen zu zahlen. Bei Verwendung eines Wechsels als Zahlungsmittel für eine Auftrags- oder Freitextrechnung erfolgt eine Habenbuchung auf dem Debitorenkonto. Diese Habenbuchung ist durch den Wechsel so lange gesichert, bis der Debitor den Wechsel an die Bank bezahlt. Üblicherweise wird die Rechnung zum Fälligkeitsdatum mit dem Wechsel ausgeglichen. Nachdem die Benachrichtigung über die Einlösung des Wechsels von der Bank eingegangen ist, kann der Wechsel abgeschlossen werden. Der Wechsel kann über die Bank zu jedem der folgenden Zeitpunkte gezogen werden:

-   Zum Fälligkeitsdatum. Dieser Ansatz wird auch als Inkassorimesse bezeichnet.
-   Vor dem Fälligkeitsdatum (üblicherweise zum Skontodatum, das in den vom Debitor festgelegten Zahlungsbedingungen angegeben ist). Beim Ausführen der Buchung wird der Skontobetrag auf ein Ausgabenkonto gebucht. Der Restbetrag verbleibt als Verbindlichkeit, bis die Zahlung des Debitors bei der Bank eingeht. Dieser Ansatz wird auch als Zum Diskont einreichen bezeichnet.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Einrichten von Buchungsprofilen für Wechsel
Verwenden Sie zum Einrichten von **Buchungsprofilen für Debitoren**, protestierte Wechsel, Inkassorimessen und Diskontrimessen das Formular : Wählen Sie im Feld **Sammelkonto** das Sammelkonto aus, auf das die Beträge von Wechseln gebucht werden sollen. Basierend auf dem Typ der Wechselbuchung wird dieses Konto belastet, oder auf dem Konto wird ein Betrag gutgeschrieben:
-   Wechsel: Durch die Buchung eines Wechsels erfolgt auf diesem Konto eine Sollbuchung, durch die Buchung einer Diskont- oder Inkassorimesse eine Habenbuchung.
-   Wechsel protestieren: Durch die Buchung eines protestierten Wechsels erfolgt auf diesem Konto eine Sollbuchung.
-   Inkassorimesse: Durch die Buchung einer Inkassorimesse erfolgt auf diesem Konto eine Sollbuchung.
-   Skontorimesse: Durch die Buchung einer Skontorimesse erfolgt auf diesem Konto eine Sollbuchung.

Wählen Sie im Feld **Konto ausgleichen** das Bargeldkonto aus, auf das die Beträge von Wechseln gebucht werden sollen. Dieses Konto wird durch den Ausgleich eines Wechsels belastet. Wählen Sie für den Fall, dass Vorauszahlungen per Wechsel abgewickelt werden, im Feld **Mehrwertsteuervorauszahlungen** das Sammelkonto zum Buchen von Mehrwertsteuerbeträgen aus. Wählen Sie für Diskontrimessen im Feld **Konto für Diskontverbindlichkeiten** das Konto aus, auf das der Diskontbetrag gebucht werden soll. Auf diesem Konto erfolgt beim Buchen einer Diskontrimesse eine Habenbuchung.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Einrichten von Debitorenparametern für Wechsel
Auf der Seite **Debitorenparameter** werden die standardmäßigen Buchungsprofile für Wechsel auf die Registerkarte **Sachkonto und Mehrwertsteuer** eingegeben. Nummernkreise werden auf der Registerkarte **Nummernkreise** eingegeben. Richten Sie Erfassungsnamen für Wechsel ein
------------------------------------------

Erstellen Sie auf der Seite **Erfassungnamen** mindestens fünf Journale für Wechsel. Hier sind die Erfassungstypen:
-   **Debitor zieht Wechsel** - Erstellen Sie ein Journal für die Erfassung zum Ziehen von Wechseln.
-   **Debitor protestiert Wechsel** - Erstellen Sie ein Journal für die Erfassung zum Protestien von Wechseln.
-   **Debitor zieht erneut Wechsel** - Erstellen Sie ein Journal für die Erfassung zum erneuten Ziehen von Wechseln.
-   **Debitoren-Bankrimesse** - Erstellen Sie ein Journal für die Rimesseerfassung.
-   **Debitor gleicht Wechsel aus** - Erstellen Sie ein Journal für die Erfassung zum Ausgleichen von Wechseln.

Auf der Erfassungsbelegseite für jede Wechselerfassung geben Sie Informationen zum Wechsel auf der Registerkarte **Wechsel** ein. Nachdem die Wechselerfassungspositionen gebucht wurden, können Sie diese auf der Seite **Wechselerfassungsabfrage** und der Seite **Wechselstatistik** anzeigen.
Einrichten von Zahlungsmethoden für Wechsel
-----------------------------------------------

Auf der Seite **Zahlungsmethoden** Einstellungen mindestens eine Zahlungsmethode für Wechsel. Sollten Sie Kunde bei mehreren Banken sein, richten Sie eine Zahlungsmethode ein, die dem für die jeweilige Bank erforderlichen Rimesseformat entspricht.
Einrichten von Zahlungsgebühren für Wechsel
-----------------------------------------

Bei einer Zahlungsgebühr handelt es sich um eine Belastung für das Einziehen der Zahlungen von Debitoren. Jede Zahlungsgebühr kann mit mehreren Einstellungen für Zahlungsgebühren versehen werden. Mithilfe dieser Einstellungen wird die Berechnung der Standardbeträge für Zahlungsgebühren gesteuert. Sie können beispielsweise Einstellungen für Zahlungsmethoden, Zahlungsspezifikationen, Währungen und Zeitperioden einrichten. Zudem können Sie einen Prozentsatz oder einen Betrag auch erstellen, der auf Tagesintervallen basierenden ist. Sie können beispielsweise einen Zinssatz einrichten, der auf der Zeit basiert, die, eine Zahlung überfällig ist. Erhebt eine Bank unterschiedliche Gebühren für unterschiedliche Rimessetypen (beispielsweise **Inkasso** oder **Rabatt**), muss für jeden Rimessetyp eine eigene Zahlungsgebührposition eingerichtet werden.
Einrichten von Rimessegebühren für Bankrimessedateien
------------------------------------------------

Sie haben auf der Seite **Bankkonten** die Möglichkeit zum Einrichten von Rimessegebühren, die von einer Bank für jede generierte Rimessedatei erhoben werden. Die Buchung der Rimessegebühren erfolgt, nachdem die Rimesse bestätigt wurde und die anfallenden Gebührenbeträge feststehen. Diese Rimessegebühren unterscheiden sich von den Zahlungsgebühren insofern, als letztere an von Debitoren eingezogen werden und mit Erfassungspositionen verknüpft sind.
Einrichten von Dokumentlayouts für Wechsel
---------------------------------------------

Klicken Sie auf der Seite **Bankkoknten** auf **Einrichten**, und geben Sie für jedes Bankkonto, das zum Generieren von Wechseldokumenten verwendet wird, das erforderliche Dokumentlayout an.
Einrichten von Debitoren für Wechsel
--------------------------------------

Auf der Seite **Debitoren** für jeden Debitor, der einer Bezahlung per Wechsel zugestimmt hat, kann eine Standardzahlungsmethode für Wechsel auf der Seite **Standardwerte für Zahlungen** eingerichtet werden.






