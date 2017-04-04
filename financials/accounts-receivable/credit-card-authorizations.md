---
title: Einstellungen, Autorisierung und Erfassung von Kreditkarten
description: "Dieser Artikel enthält einen Überblick über die Kreditkartenautorisierung in Microsoft Dynamics AX. Er umfasst Informationen darüber, wie ein Zahlungsdienst eingerichtet, eine Kreditkarte einem Auftrag hinzugefügt und eine Autorisierung storniert wird."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 40d950b04511e85d05106c274d1580a3daac7af7
ms.lasthandoff: 03/31/2017


---

# <a name="credit-card-setup-authorization-and-capture"></a>Einstellungen, Autorisierung und Erfassung von Kreditkarten

Dieser Artikel enthält einen Überblick über die Kreditkartenautorisierung in Microsoft Dynamics AX. Er umfasst Informationen darüber, wie ein Zahlungsdienst eingerichtet, eine Kreditkarte einem Auftrag hinzugefügt und eine Autorisierung storniert wird.

<a name="setting-up-the-credit-card-payment-service"></a>Einrichten des Kreditkartenzahlungsdienstes
------------------------------------------

Um Kreditkarten zu verwenden, müssen Sie einen Zahlungsdienst auf der Seite "Zahlungsdienst" einrichten und aktivieren. Ein Zahlungsdienst fungiert als Bindeglied zwischen der juristischen Person und der Bank, die die Kreditkartengebühren eines Debitoren verarbeitet. Sie müssen mit einem Kreditkartenanbieter zusammenarbeiten, der im Feld Zahlungskonnektor aufgeführt ist, und Sie müssen ein Konto bei diesem Anbieter einrichten. Sie müssen dann die anderen Optionen auf der Seite "Zahlungsdienst" einrichten, Kreditkartentypen für American Express, Discover, MasterCard sowie Discover auf der Seite "Kreditkartentypen" einrichten und den Anbieter als Standardanbieter aktivieren. Sie müssen auch diese Schritte ausführen, um Ihre Einrichtung abzuschließen.
-   Geben Sie auf der Seite "Debitorenparameter" die Parameter für die Verwendung von Kreditkartenautorisierungen an.
-   Richten Sie auf der Seite "Zahlungsbedingungen" die Zahlungsbedingungen für Kreditkarten ein. Wählen Sie im Feld "Zahlungstyp" die Option "Kreditkarte" aus.
-   Geben Sie auf der Seite "Debitorenkreditkarten" die Kreditkarteninformationen für Debitoren ein.

## <a name="adding-a-new-credit-card"></a>Hinzufügen einer neuen Kreditkarte
Sie können neue Kreditkartendatensätze auf der Seite "Debitoren" mithilfe von "Debitor", "Einrichten", "Kreditkarte" erstellen. Sie können auch Kreditkartendatensätze erstellen, wenn Sie Aufträge auf der Seite "Auftrag" eingeben, indem Sie "Verwalten", "Debitor", "Kreditkarte", "Registrieren" verwenden.
Eine Kreditkarte zu einem Auftrag hinzufügen
-------------------------------------

Sie können eine Kreditkarte einem Auftrag hinzufügen, indem Sie eine Kreditkarte in der Kreditkartensuche im Inforegister "Preis und Rabatte" auf der Seite "Auftrag" auswählen. Um des Autorisierungsprozess zu starten, wählen Sie im Aktivitätsbereich auf der Registerkarte "Verwalten" die Optionen "Kreditkarte" und "Autorisieren" aus.
Eine Kreditkarte autorisieren
-------------------------

Wenn eine Kreditkarte autorisiert wird, werden die Kreditkartennummer und der Name des Karteninhabers überprüft und der verfügbare Guthabensaldo bestätigt. Optional werden der Kreditkartenüberprüfungswert und die Adresse des Karteninhabers überprüft. Anschließend wird der verfügbare Guthabensaldo des Debitors um den Rechnungsbetrag verringert. Der Zahlungsservice informiert Sie, ob die Kreditkarte akzeptiert oder abgelehnt wurde. Nach der Fakturierung des Auftrags wird die Kreditkarte mit dem Rechnungsbetrag belastet (erfasst).

### <a name="card-verification-value"></a>Kartenprüfwert

Sie können den Kartenprüfwert anfordern, der manchmal als Sicherheitscode der Karte bezeichnet wird. Bei American Express handelt es sich um einen vierstelligen Wert. Bei Discover, MasterCard und Visa handelt es sich um einen dreistelligen Wert.

### <a name="address-verification"></a>Adressüberprüfung

Adressüberprüfungsinformationen werden immer an den Zahlungsbereitsteller gesendet. Sie können festlegen, wie viele Informationen erforderlich sind, damit eine Buchung akzeptiert werden kann. Stellen Sie sicher, dass mit Ihrem um zu untersuchen, um zu bestimmen, ob er Informationen diese akzeptiert. Hier sind die Optionen für Adressüberprüfung:
-   **Buchung immer akzeptieren** – Die Transaktion wird immer akzeptiert, unabhängig von den Ergebnissen der Adressüberprüfung.
-   **Kontoinhaber** – Vergleich des Namens des Karteninhabers aus der Transaktion mit den Informationen des Kreditkartenunternehmens.
-   **Rechnungsadresse** – Vergleich des Namens des Karteninhabers und der Rechnungsadresse aus der Transaktion mit den Informationen des Kreditkartenunternehmens.
-   **Postleitzahl der Rechnungsadresse** – Vergleich des Namens des Karteninhabers, der Rechnungsadresse und der Postleitzahl aus der Transaktion mit den Informationen des Kreditkartenunternehmens.

## <a name="data-support"></a>Datenunterstützung
Für jeden Kreditkartentyp, der unterstützt wird, können Sie die Detailebene für den Datensupport angeben. Die Ebene steuert, wie viele Informationen zu einer Buchung an den Zahlungsservice übertragen werden. Achten Sie darauf, mit Ihrem Anbieter zu überprüfen, um festzustellen, ob er diese Informationen bereitstellen kann. Hier sind die Optionen für die Ebene der Datenunterstützung:
-   **Ebene 1** – Übertragen des Transaktionsdatums, des Transaktionsbetrags und der Beschreibung.
-   **Ebene 2** – Übertragen aller Informationen von "Ebene 1" sowie der Versandadresse und Einzelhändleradresse und Steuerinformationen.
-   **Ebene 3** – Übertragen aller Informationen der "Ebene 2" sowie der Auftragspositionsinformationen.

## <a name="partial-payments"></a>Teilzahlungen
Wenn Sie einen Teil eines Auftrags versenden, wird der Betrag der Teilbestellung erfasst, und die Autorisierung, die für den Betrag des gesamten Auftrags galt, wird geschlossen. Eine neue Autorisierung wird dann für den Restbetrag des Auftrags verwendet, die noch nicht geliefert wurde.

## <a name="voiding-an-authorization"></a>Autorisierung stornieren 
Um eine Kreditkartenautorisierung zu stornieren, können Sie die Zahlungsmethode zu einer anderen Methode ändern die keinen Typ von "Kreditkarte" hat.




