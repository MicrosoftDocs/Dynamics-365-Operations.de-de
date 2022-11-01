---
title: Vorauszahlungsrechnungen im Vergleich zu Vorauszahlungen
description: Dieser Artikel erläutert und vergleicht die beiden Methoden, die Organisationen für Vorauszahlungen verwenden können.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f828b93075c134778da280243c0875edf99300
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715828"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Vorauszahlungsrechnungen im Vergleich zu Vorauszahlungen

[!include [banner](../includes/banner.md)]

Dieser Artikel erläutert und vergleicht die beiden Methoden, die Organisationen für Vorauszahlungen verwenden können. In einer Methode wird eine Vorauszahlungsrechnung erstellt, die einer Bestellung zugeordnet ist. In der anderen Methode werden Erfassungsbelege für Vorauszahlungen erstellt, indem Sie Journaleinträge erstellen und diese dann als Erfassungsbelege für Vorauszahlungen markieren.

Organisationen können für Waren oder Dienstleistungen Vorauszahlungen an Kreditoren leisten, bevor die Waren geliefert oder Dienstleistungen erbracht wurden. Zwei Methoden können verwendet werden, um Vorauszahlungen an Kreditoren auszugeben. Vorauszahlungen können zur Minimierung des Risikos nachverfolgt und auf einer Bestellung definiert werden. Für diese Methode müssen Sie eine Vorauszahlungsrechnung erstellen, die einer Bestellung zugeordnet ist. Diese Methode wird als Vorauszahlungsrechnungsstellung bezeichnet. Organisationen, die nicht Vorauszahlungen als Lagerabschluss verfolgen möchten oder keine Vorauszahlungsrechnung von dem Kreditor erhalten, können Erfassungsbelege für Vorauszahlungen anstelle der Vorauszahlungsrechnungsstellungsmethode verwenden. Sie können zum Erstellen von Erfassungsbelegen für Vorauszahlungen Journaleinträge erstellen und diese dann als Erfassungsbelege für Vorauszahlungen markieren. Für diese Methode können Sie jedoch nicht nachverfolgen, welche Zahlungen an einen Kreditor für welche Bestellungen erfolgen. Allerdings können Sie eine gebuchte Vorauszahlung für den Ausgleich mit einer Bestellung markieren.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Wann Vorauszahlungsrechnungsstellung oder Vorauszahlungen verwenden

| Vorauszahlungsrechnungsstellung                                                                | Vorauszahlungen                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Vorauszahlungswerte können für eine Bestellung definiert werden,                                    | Kein Vorauszahlungswert ist für die Bestellung definiert.                    |
| Eine Vorauszahlungsrechnung und eine Endabrechnung müssen gebucht werden.                       | Keine Vorauszahlungsrechnung muss gebucht werden.                                    |
| Verbindlichkeiten für die Vorauszahlung werden im Vorauszahlungskonto, nicht im Kreditorenkonto vorgesehen. | Verbindlichkeiten für die Vorauszahlung werden im Kreditorenkonto vorgesehen.                  |
| Der Kreditorensaldo spiegelt nicht den Vorauszahlungswert beim Ausführen des Prozesses wider.     | Der Kreditorensaldo spiegelt den Vorauszahlungswert beim Ausführen des Prozesses wider. |
| Vorauszahlungsrechnungsstellung ist nur in den Kreditoren verfügbar.                         | Vorauszahlungen sind in Kreditoren und Debitoren verfügbar.    |

## <a name="overview-of-the-prepayment-process"></a>Überblick über den Vorauszahlungsprozesses
Die Buchführungsmethoden in vielen Ländern/Regionen verlangen, dass Vorauszahlungen von einem Debitor oder an einen Kreditor nicht in den üblichen Debitoren- oder Kreditorensammelkonten gebucht werden. Diese Vorauszahlungen werden stattdessen in speziellen Sachkonten für Vorauszahlungen gebucht. Wenn ein Auftrag oder eine Bestellung erstellt, wird für den Debitor oder vom Kreditor eine Rechnung ausgestellt. Nachdem die Rechnung beglichen wurde, werden der Erfassungsbeleg für die Vorauszahlung und der Beleg der Mehrwertsteuervorauszahlung storniert und die Rechnungsbeträge werden automatisch in den üblichen Sammelkonten gebucht. Gehen Sie folgendermaßen vor, um eine Vorauszahlung zu erstellen.

1.  Buchungsprofile für Vorauszahlungen einrichten.
2.  In den Debitorenparametern und in den Kreditorenparametern unter **Sachkonto und Mehrwertsteuer** das neue Buchungsprofil aus, indem Sie den Parameter **Buchungsprofil für Zahlungserfassung mit Vorauszahlung** verwenden.
3.  Erstellen Sie eine Zahlungserfassung, und erstellen Sie dann die neue Zahlung.
4.  Sie können die Zahlung als Vorauszahlung kennzeichnen. Wenn eine Zahlung als Vorauszahlung gekennzeichnet ist, wird die Zahlung an den Sachkonten gebucht, die im Buchungsprofil definiert werden, das Sie in den Schritten 1 und 2 einrichten. Darüber hinaus, wenn die Zahlung als Vorauszahlung gekennzeichnet ist, werden Steuern berechnet. Einige Regierungen verlangen, dass Steuern gezahlt werden, wenn eine Vorauszahlung erfasst wird, selbst wenn keine Rechnung vorliegt.
5.  Buchen Sie die Vorauszahlung.
6.  Optional: Sie können die Vorauszahlung für die Bestellung bzw. den Auftrag ausgleichen, bevor Sie die Rechnung erstellen. Auf der Auftrags- oder Bestellungsseite im Aktivitätsbereich, verwendet **Bankbuchungen**.
7.  Nachdem der Kreditor die Waren oder Dienstleistungen geliefert hat, erfassen Sie die Rechnung. Wenn Sie die Vorauszahlung für die Bestellung oder den Verkaufsauftrag in Schritt 6 ausgeglichen haben, wird die Vorauszahlung automatisch mit der Rechnung ausgeglichen, die Sie erstellt haben. Wenn Sie die Vorauszahlung nicht für die Bestellung bzw. den Auftrag ausgeglichen haben, können Sie sie anhand der Rechnung manuell ausgleichen, indem Sie **Buchungen ausgleichen** der Debitoren- oder Kreditorenseite verwenden. Der Vorauszahlungsbetrag wird dann aus dem temporären Debitoren-/Kreditoren-Sachkonto storniert. Darüber hinaus, wenn Steuern berechnet wurden, werden sie storniert, da die Rechnung die tatsächlichen Steuern hat.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Überblick über den Vorauszahlungsrechnungsstellungsprozesses
Vorauszahlungsrechnungen sind eine allgemeine Geschäftspraktik. Ein Kreditor gibt Vorauszahlungsrechnungen aus, um eine Einzahlung auf dem Einkauf zu erfordern, bevor die Bestellung erfüllt wurde. Beispielsweise verlangen einige Kreditoren kann eine Vorauszahlung für angepasste Waren oder Dienstleistungen. Wenn ein Kreditor einer Rechnung abgeglichen werden, die eine Vorauszahlung fordert, können Sie die Funktion zur Vorauszahlungsrechnungsstellung verwenden. Ein Vorauszahlungswert kann auf der Bestellung definiert werden, eine Vorauszahlungsrechnung wird erfasst und bezahlt, und die Vorauszahlungsrechnung wird auf die Endabrechnung angewendet. Gehen Sie folgendermaßen vor, um eine Vorauszahlung zu erstellen.

1.  Die Bestellung, für die der Kreditor eine Vorauszahlung angefordert hat, wird vom Einkaufsvertreter erstellt, bestätigt und gesendet. Der Vorauszahlungswert wird auf der Bestellung als Teil der Vereinbarung definiert.
2.  Der Kreditor übermittelt eine Vorauszahlungsrechnung.
3.  Der Kreditorenkoordinator erfasst die Vorauszahlungsrechnung für die Bestellung, und dann wird die Vorauszahlungsrechnung bezahlt.
4.  Der Lieferant sendet eine Zahlungsaufforderung, die als Standard-Kreditorenrechnung bezeichnet wird. Nachdem der Kreditor die Waren oder Dienstleistungen geliefert hat und die zugehörige Standard-Kreditorenrechnung eingegangen ist, wendet der Kreditorenkoordinator den bereits geleisteten Vorauszahlungsbetrag auf die Standardrechnung an.
5.  Der Kreditorenkoordinator begleicht dann den verbleibenden Betrag der Standardrechnung.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Einrichten von Parametern, um den Rechnungsstellungsprozess für Vorauszahlungen zu aktivieren
Auf der Registerkarte **Bestellung** der Seite **Lagerbuchung** (**Lagerverwaltung \> Einrichtung \> Buchung \> Buchung**) muss ein Vorauszahlungskonto definiert sein. Das Vorauszahlungskonto wird aktualisiert, normalerweise belastet, wenn die Vorauszahlungsrechnung gebucht wird. Der Saldo auf dem Vorauszahlungskonto wird storniert, wenn die Standardrechnung, die auf die Vorauszahlungsrechnung angewendet wird, gebucht wird. Wenn Sie die Vorauszahlungsrechnung nicht mit einer Zahlung abrechnen, bevor Sie die Vorauszahlungsrechnung auf die Standardrechnung anwenden, werden die Buchhaltungseinträge aus der gebuchten Vorauszahlungsrechnung storniert, wenn die Standardrechnung gebucht wird.

Das Gegenkonto für die Verbindlichkeiten aus Lieferungen und Leistungen ist im Profil **Kreditorenbuchung** definiert. Klicken Sie auf **Kreditorenkonten \>Einrichtung \> Kreditorenkontenparameter \>Registerkarte „Sachkonto und Mehrwertsteuer“ \> Buchungsprofil mit Vorauszahlung für Kreditorenrechnung**, um das Standardbuchungsprofil zu definieren.

Die **Vorauszahlungsantragsrichtlinie** gibt an, ob das System automatisch abgerechnete Vorauszahlungsrechnungen auf die manuell erstellte endgültige Rechnung anwendet. Rechnungen, die mit einer Datenentität erstellt wurden, beziehen sich nicht auf die **Vorauszahlungsantragsrichtlinie**. Sie müssen abgerechnete Vorauszahlungsrechnungen manuell auf Rechnungen anwenden, die mit einer Datenentität erstellt wurden. Gehen Sie zu **Kreditorenkonten \>Einrichtung \> Kreditorenkontenparameter \> Registerkarte „Sachkonto und Mehrwertsteuer“ \> Vorauszahlungsantragsrichtlinie**, um die Richtlinie zu definieren. Wenn das Feld **Vorauszahlungsantragsrichtlinie** auf **Automatisch** gesetzt ist, wird die Vorauszahlungsrechnung automatisch für die Begleichung mit der Schlussrechnung markiert. Wenn das Feld auf **Benachrichtigung** eingestellt ist, wird ein visueller Hinweis angezeigt, dass eine Vorauszahlungsrechnung für die Anwendung verfügbar ist, wenn die endgültige Rechnung erstellt wird.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Erstellen einer Bestellung, die Informationen zur Vorauszahlungsrechnung enthält
Wenn ein Lieferant Ihnen mitteilt, dass für Waren und Dienstleistungen, die in einer Bestellung enthalten sind, eine Vorauszahlung erforderlich ist, müssen Sie den Vorauszahlungswert für die zugehörige Bestellung definieren. Gehen Sie zu **Kreditorenkonten \> Allgemein \> Bestellungen \> Alle Bestellungen** und finden Sie die Bestellung des Lieferanten. Wählen Sie im Aktivitätsbereich die Registerkarte **Kauf** und dann **Vorauszahlung** aus. Geben Sie Informationen zur Vorauszahlung ein, einschließlich einer Beschreibung, der Höhe der Vorauszahlung, ob es sich um einen festen Betrag oder einen Prozentsatz handelt, sowie einer Kennung für die Vorauszahlungskategorie. 

Beachten Sie, dass mehrere Vorauszahlungsdefinitionen in einer Bestellung nicht zulässig sind. Wenn Sie mehrere Vorauszahlungen für eine Bestellung zulassen müssen, buchen Sie die Zahlungen über die Zahlungserfassung anstelle einer Vorauszahlungsrechnung.

Die Vorauszahlung kann aus der Bestellung entfernt werden, es sei denn, Sie haben bereits eine Zahlung mit der gebuchten Vorauszahlungsrechnung verrechnet oder die Standardrechnung gebucht. Wählen Sie **Kreditorenkonten \> Allgemein \> Bestellungen \> Alle Bestellungen** aus und finden Sie die Bestellung des Lieferanten, um eine Vorauszahlungsinformation aus der Bestellung zu entfernen. Wählen Sie im Aktivitätsbereich die Registerkarte **Kauf** und dann **Vorauszahlung entfernen** aus.

## <a name="create-and-post-a-prepayment-invoice"></a>Erstellen und buchen einer Vorauszahlungsrechnung
Um die Vorauszahlungsrechnung des Lieferanten zu erfassen, gehen Sie zur Seite **Kreditorenrechnung** durch Auswahl der Option **Vorauszahlungsrechnung** auf der Seite **Bestellungen** (**Kreditorenkonten \> Allgemein \> Bestellungen \> Alle Bestellungen \> Registerkarte „Rechnung“ \> Vorauszahlungsrechnung**). Geben Sie Informationen zur Vorauszahlungsrechnung ein, einschließlich der Rechnungsnummer. Die Mengen für eine Vorauszahlungsrechnung können nicht geändert werden. Wenn der Lieferant einen Teilbetrag des in der Bestellung definierten Vorauszahlungswerts in Rechnung gestellt hat, können Sie den Stückpreis aktualisieren, um den Teilwert widerzuspiegeln.

Wenn die Vorauszahlungsrechnung gebucht wird, werden der Kreditorensaldo und das Vorauszahlungskonto aktualisiert. Der Wert **Vorauszahlungsantrag** der in der Bestellung enthaltenen Vorauszahlungsdefinition wird ebenfalls aktualisiert. Die Standardeinträge für die Finanzdimension des gebuchten Vorauszahlungsbelegs werden den Kopfinformationen auf der Bestellung entnommen.

Wenn die **Finanzdimensionen in Rechnungspositionen auf Kreditorenvorauszahlungsrechnungen sperren** Funktion auf der **Funktionsverwaltung** aktiviert ist, können die Dimensionen in der Vorauszahlungskopfzeile oder in den Zeilen nicht aktualisiert werden. 

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Buchen und Begleichen von Zahlungen für die Vorauszahlungsrechnung
Als nächstes wird die Vorauszahlungsrechnung von der Seite **Zahlungserfassung** aus bezahlt. Klicken Sie auf **Kreditorenrechnungen \> Erfassungen \> Zahlungen \> Zahlungserfassungen**, um auf Zahlungserfassungen zuzugreifen. Nach Buchung des Ausgleichs der Zahlung auf die Vorauszahlungsrechnung wird der Wert **Vorauszahlungsantrag verbleibend** der Bestellung aktualisiert.

Bevor Sie die Standardrechnung für die Vorauszahlungsrechnung buchen, können Sie die Abwicklung der Zahlung aus der Vorauszahlungsrechnung stornieren. Nachdem Sie eine Standardrechnung auf die Vorauszahlungsrechnung angewendet haben, kann die Zahlungsabwicklung jedoch nicht aus der Vorauszahlungsrechnung storniert werden.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Buchen der Standardkreditorenrechnung für die Bestellung und Anwenden der Vorauszahlungsrechnung auf die Standardrechnung
Erfassen Sie die vom Lieferanten erhaltene Standardrechnung. Im Rahmen dieses Vorgangs können Sie die abgerechnete Vorauszahlungsrechnung auf die Lieferantenrechnung anwenden, sodass sich der Rechnungswert um den bereits bezahlten Betrag verringert. Durch Anwenden der Vorauszahlungsrechnung auf die Kreditorenrechnung wird sichergestellt, dass Buchhaltungseinträge aus der Vorauszahlungsrechnung storniert werden.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Anwendung der Vorauszahlungsrechnung nach Buchung der Standardrechnung
Wenn Sie vergessen haben, die Vorauszahlung zum Zeitpunkt der Buchung der Kreditorenrechnung auf die Standardkreditorenrechnung anzuwenden, steht die abgerechnete Vorauszahlung zur Verfügung, um sie auf andere Rechnungen dieses Lieferanten über die Seite **Kreditor** anzuwenden (**Kreditorenkonten \> Allgemein \> Kreditoren \> Alle Kreditoren \> Registerkarte „Rechnung“ \> Anwenden**).

## <a name="reversal-of-the-prepayment-application-process"></a>Stornierung des Vorauszahlungsantragsverfahrens
Wenn Sie den Antrag einer Vorauszahlungsrechnung aus einer Standardrechnung stornieren oder dessen Begleichung rückgängig machen müssen, wählen Sie die Aktion **Stornieren** auf der Seite **Kreditoren** aus (**Kreditorenkonten \> Allgemein \> Kreditoren \> Alle Kreditoren \> Registerkarten „Rechnung“ \> Stornieren**). Nachdem der Vorauszahlungsantrag storniert wurde, können Sie die Vorauszahlung auf eine andere Standardrechnung anwenden. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
