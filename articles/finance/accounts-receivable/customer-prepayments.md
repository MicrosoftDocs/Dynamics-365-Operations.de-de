---
title: Debitorenvorauszahlungen
description: In diesem Thema wird erläutert, wie Sie Debitorenvorauszahlungen (auch Debitoreneinzahlungen genannt) einrichten und verarbeiten.
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e83c8be1b397f90445230835e415ea4fcea5a8d0bf695e6cc5eadc55275ded7f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768962"
---
# <a name="customer-prepayments"></a>Debitorenvorauszahlungen

[!include [banner](../includes/banner.md)]

Debitorenvorauszahlungen werden verwendet, wenn Sie eine Zahlung von einem Kunden erhalten, es jedoch noch keine Rechnung gibt, gegen die die Zahlung abgerechnet werden kann. Solche Zahlungen werden auch als Debitoreneinzahlungen bezeichnet.

Das Einrichten und Arbeiten mit Kundenvorauszahlungen besteht aus den folgenden grundlegenden Schritten.

1. Erstellen Sie ein Debitorenbuchungsprofil für Vorauszahlungen.
2. Stellen Sie den Parameter **Buchungsprofil mit Erfassungsbeleg für Vorauszahlung** ein,
3. Erstellen Sie eine Zahlungserfassung und wählen Sie für jede Position das Kontrollkästchen **Erfassungsbeleg für Vorauszahlung** aus.
4. Dient zum Buchen der Debitorenzahlungserfassung.
5. Nachdem eine Rechnung erstellt wurde, gleichen Sie sie auf der Seite **Offene Buchungen ausgleichen** mit der Vorauszahlung aus.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Ein Debitorenbuchungsprofil für Vorauszahlungen erstellen

Wenn Sie Vorauszahlungen oder Einzahlungen von Ihren Debitoren annehmen, bevor Waren oder Dienstleistungen geliefert werden oder bevor eine Rechnung in Ihrem System vorhanden ist, müssen Sie den Zahlungseingang in der Regel als Verbindlichkeit und nicht als Aktivposten in Ihrem Kontenplan erfassen. Die Anforderungen für die Erfassung dieser Beträge in Ihrem Hauptbuch können jedoch je nach Land oder Region unterschiedlich sein. Fragen Sie daher unbedingt Ihre Buchhalter nach den jeweils geltenden Vorschriften.

Grundsätzlich ist der Prozess zum Erstellen eines Buchungsprofils, das für Vorauszahlungen verwendet werden kann, der gleiche wie zum Erstellen anderer Buchungsprofile. Der Hauptunterschied ist das Hauptkonto, das Sie im Feld **Sammelkonto** auswählen. Weitere Informationen finden Sie unter [Debitorenbuchungsprofile](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Parameter für Debitorenvorauszahlungen festlegen

Es gibt zwei Hauptparameter für Debitorenkonten, die Sie berücksichtigen müssen, wenn Sie das System für Debitorenvorauszahlungen konfigurieren. Gehen Sie folgendermaßen vor, um die Parameter zu konfigurieren:

1. Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
2. Optional: Wählen Sie auf der Registerkarte **Hauptbuch und Mehrwertsteuer** das Inforegister **Zahlung** aus und legen Sie die Option **Mehrwertsteuer auf Vorauszahlung** auf **Ja** fest.
3. Wählen Sie im Feld **Buchungsprofil mit Erfassungsbeleg für Vorauszahlung** das Debitorenuchungsprofil aus, das verwendet werden soll, wenn Debitorenvorauszahlungen gebucht werden.
4. Schließen Sie die Seite.

## <a name="create-customer-prepayment-vouchers"></a>Erfassungen für Debitorenvorauszahlungen erstellen

Wenn Sie die Debitorenzahlungserfassung erstellen, müssen Sie für jede Vorauszahlung die Option **Erfassungsbeleg für Vorauszahlung** auf der Seite **Kundenzahlungserfassung** auf **Ja** festlegen. Gehen Sie folgendermaßen vor, um eine Debitorenvorauszahlung zu erstellen.

1. Gehen Sie zu **Debitorenkonten \> Zahlungen \> Kundenzahlungserfassung**.
2. Wählen Sie **Neu** aus, um eine Erfassung zu erstellen.
3. Wählen Sie im Feld **Name** den Namen der Erfassung aus.

    > [!IMPORTANT]
    > Wenn Sie im vorherigen Verfahren die Option **Mehrwertsteuer auf Vorauszahlung** auf **Ja** festlegen, müssen Sie einen Erfassungsnamen auswählen, in dem der Parameter **Betrag enthält Mehrwertsteuer** ausgewählt ist. 

4. Optional: Sie können im Feld **Beschreibung** eine detaillierte Beschreibung eingeben.
5. Wählen Sie **Positionen** aus.
6. Wenn keine leere Position vorhanden ist, wählen Sie **Neu**, um eine Position zu erstellen.
7. Geben Sie im Feld **Datum** das Datum ein, an dem die Vorauszahlung gebucht werden soll.
8. Wählen Sie im Feld **Konto** den Debitor für die Vorauszahlung aus.
9. Optional: Sie können im Feld **Beschreibung** eine detaillierte Beschreibung der Buchung eingeben.
10. Geben Sie im Feld **Gutschrift** den Betrag der Vorauszahlung ein.
11. Wählen Sie im Feld **Gegenkonto** das Konto aus, auf das die Zahlung gegengebucht werden soll. Wählen Sie beispielsweise die Bank oder das Hauptkonto aus, auf die/das die Zahlung gebucht werden soll.
12. Wählen Sie im Feld **Zahlungsmethode** eine die Zahlungsmethode des Debitors aus.
13. Legen Sie die Registerkarte **Zahlung** die Option **Erfassungsbeleg für Vorauszahlung** auf **Ja** fest.
14. Wiederholen Sie die Schritte 7 bis 13 für jede weitere Vorauszahlung, die gebucht werden muss.
15. Wählen Sie **Buchen** aus, um die Erfassung abzuschließen.

## <a name="settle-prepayments-with-invoices"></a>Vorauszahlungen mit Rechnungen ausgleichen

Sie können den Arbeitsbereich **Debitorenzahlungen** benutzen, um Zahlungen, die noch nicht vollständig ausgeglichen wurden, einfach zu finden und auszugleichen.

1. Wählen Sie im Dashboard **Home** die Kachel **Debitorenzahlungen** aus.
2. Suchen Sie im Abschnitt **Debitorenbuchen** auf der Registerkarte **Nicht ausgeglichene Zahlungen** nach der auszugleichenden Zahlung und wählen Sie sie aus.
3. Wählen Sie **Buchungen ausgleichen**.
4. Aktivieren Sie für die Rechnung und die auszugleichende Zahlung das Kontrollkästchen **Markieren**.
5. Wählen Sie **Buchen** aus.

Weitere Informationen zum Ausgleichen offener Buchungen finden Sie unter [Übersicht über Ausgleiche](/cash-bank-management/settlement-overview.md).
