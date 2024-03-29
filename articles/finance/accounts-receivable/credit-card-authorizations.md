---
title: Einstellungen, Autorisierung und Erfassung von Kreditkarten
description: Dieser Artikel stellt eine Übersicht der Kreditkartenautorisierung in Microsoft Dynamics 365 Finance bereit. Er umfasst Informationen darüber, wie ein Zahlungsdienst eingerichtet, eine Kreditkarte einem Auftrag hinzugefügt und eine Autorisierung storniert wird.
author: ShivamPandeymsft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84fe90e6c01d06ecbb3a1e13a9f018d385c22c0
ms.sourcegitcommit: 346a9ca833237836d5e4ca496aeb2b5b24bdb27b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9583777"
---
# <a name="credit-card-setup-authorization-and-capture"></a>Einstellungen, Autorisierung und Erfassung von Kreditkarten

[!include [banner](../includes/banner.md)]

Dieser Artikel stellt eine Übersicht der Kreditkartenautorisierung in Microsoft Dynamics 365 Finance bereit. Er umfasst Informationen darüber, wie ein Zahlungsdienst eingerichtet, eine Kreditkarte einem Auftrag hinzugefügt und eine Autorisierung storniert wird.

## <a name="setting-up-the-credit-card-payment-service"></a>Einrichten des Kreditkartenzahlungsdienstes

Um Kreditkarten zu verwenden, müssen Sie einen Zahlungsdienst auf der Seite "Zahlungsdienst" einrichten und aktivieren. Ein Zahlungsdienst fungiert als Bindeglied zwischen der juristischen Person und der Bank, die die Kreditkartengebühren eines Debitoren verarbeitet. Sie müssen mit einem Kreditkartenanbieter zusammenarbeiten, der im Feld Zahlungskonnektor aufgeführt ist, und Sie müssen ein Konto bei diesem Anbieter einrichten. Sie müssen dann die anderen Optionen auf der Seite "Zahlungsdienst" einrichten, Kreditkartentypen für American Express, Discover, MasterCard sowie Discover auf der Seite "Kreditkartentypen" einrichten und den Anbieter als Standardanbieter aktivieren. Sie müssen auch diese Schritte ausführen, um Ihre Einrichtung abzuschließen.
-   Geben Sie auf der Seite "Debitorenparameter" die Parameter für die Verwendung von Kreditkartenautorisierungen an.
-   Richten Sie auf der Seite "Zahlungsbedingungen" die Zahlungsbedingungen für Kreditkarten ein. Wählen Sie im Feld "Zahlungstyp" die Option "Kreditkarte" aus.
-   Geben Sie auf der Seite "Debitorenkreditkarten" die Kreditkarteninformationen für Debitoren ein.

## <a name="adding-a-new-credit-card"></a>Hinzufügen einer neuen Kreditkarte
Sie können neue Kreditkartendatensätze auf der Seite "Debitoren" mithilfe von "Debitor", "Einrichten", "Kreditkarte" erstellen. Sie können auch Kreditkartendatensätze erstellen, wenn Sie Aufträge auf der Seite "Auftrag" eingeben, indem Sie "Verwalten", "Debitor", "Kreditkarte", "Registrieren" verwenden.

## <a name="adding-a-credit-card-to-a-sales-order"></a>Eine Kreditkarte zu einem Auftrag hinzufügen

Sie können eine Kreditkarte einem Auftrag hinzufügen, indem Sie eine Kreditkarte in der Kreditkartensuche im Inforegister "Preis und Rabatte" auf der Seite "Auftrag" auswählen. Um des Autorisierungsprozess zu starten, wählen Sie im Aktivitätsbereich auf der Registerkarte "Verwalten" die Optionen "Kreditkarte" und "Autorisieren" aus.

## <a name="authorizing-a-credit-card"></a>Eine Kreditkarte autorisieren

Wenn eine Kreditkarte autorisiert wird, werden die Kreditkartennummer und der Name des Karteninhabers überprüft und der verfügbare Guthabensaldo bestätigt. Optional werden der Kreditkartenüberprüfungswert und die Adresse des Karteninhabers überprüft. Anschließend wird der verfügbare Guthabensaldo des Debitors um den Rechnungsbetrag verringert. Der Zahlungsservice informiert Sie, ob die Kreditkarte akzeptiert oder abgelehnt wurde. Nach der Fakturierung des Auftrags wird die Kreditkarte mit dem Rechnungsbetrag belastet (erfasst).

### <a name="card-verification-value"></a>Kartenprüfwert

Sie können den Kartenprüfwert anfordern, der manchmal als Sicherheitscode der Karte bezeichnet wird. Bei American Express handelt es sich um einen vierstelligen Wert. Bei Discover, MasterCard und Visa handelt es sich um einen dreistelligen Wert.

### <a name="address-verification"></a>Adressüberprüfung

Adressüberprüfungsinformationen werden immer an den Zahlungsbereitsteller gesendet. Sie können entscheiden, wie viele Informationen zum Akzeptieren der Buchung erforderlich sind. Achten Sie darauf, mit Ihrem Anbieter zu überprüfen, ob er diese Informationen akzeptieren kann. Hier sind die Optionen für Adressüberprüfung:
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
Wenn Sie einen Teil eines Auftrags versenden, wird der Betrag der Teilbestellung erfasst, und die Autorisierung, die für den Betrag des gesamten Auftrags galt, wird geschlossen. Anschließend wird eine neue Autorisierung für den Restbetrag des Auftrags eingereicht, der nicht geliefert wurde.

## <a name="voiding-an-authorization"></a>Autorisierung stornieren 
Um eine Kreditkartenautorisierung zu stornieren, können Sie die Zahlungsmethode zu einer anderen Methode ändern die keinen Typ von "Kreditkarte" hat.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
