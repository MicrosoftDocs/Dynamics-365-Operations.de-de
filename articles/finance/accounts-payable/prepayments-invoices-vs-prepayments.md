---
title: Vorauszahlungsrechnungen im Vergleich zu Vorauszahlungen
description: Dieser Artikel erläutert und vergleicht die beiden Methoden, die Organisationen für Vorauszahlungen verwenden können. In einer Methode können Sie eine Vorauszahlungsrechnung erstellen, die einer Bestellung zugeordnet ist. In der anderen Methode erstellen Sie Erfassungsbelege für Vorauszahlungen, indem Sie Journaleinträge erstellen und diese dann als Erfassungsbelege für Vorauszahlungen markieren.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c29529aa57eb7685e36f5407f4279544fdb701
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979537"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Vorauszahlungsrechnungen im Vergleich zu Vorauszahlungen

[!include [banner](../includes/banner.md)]

Dieser Artikel erläutert und vergleicht die beiden Methoden, die Organisationen für Vorauszahlungen verwenden können. In einer Methode können Sie eine Vorauszahlungsrechnung erstellen, die einer Bestellung zugeordnet ist. In der anderen Methode erstellen Sie Erfassungsbelege für Vorauszahlungen, indem Sie Journaleinträge erstellen und diese dann als Erfassungsbelege für Vorauszahlungen markieren.

Organisationen können für Waren oder Dienstleistungen Vorauszahlungen an Kreditoren leisten, bevor die Waren geliefert oder Dienstleistungen erbracht wurden. Zwei Methoden können verwendet werden, um Vorauszahlungen an Kreditoren auszugeben. Vorauszahlungen können zur Minimierung des Risikos nachverfolgt und auf einer Bestellung definiert werden. Für diese Methode müssen Sie eine Vorauszahlungsrechnung erstellen, die einer Bestellung zugeordnet ist. Diese Methode wird als Vorauszahlungsrechnungsstellung bezeichnet. Organisationen, die nicht Vorauszahlungen als Lagerabschluss verfolgen möchten oder keine Vorauszahlungsrechnung von dem Kreditor erhalten, können Erfassungsbelege für Vorauszahlungen anstelle der Vorauszahlungsrechnungsstellungsmethode verwenden. Sie können zum Erstellen von Erfassungsbelegen für Vorauszahlungen Journaleinträge erstellen und diese dann als Erfassungsbelege für Vorauszahlungen markieren. Für diese Methode können Sie jedoch nicht nachverfolgen, welche Zahlungen an einen Kreditor für welche Bestellungen erfolgen. Allerdings können Sie eine gebuchte Vorauszahlung für den Ausgleich mit einer Bestellung markieren.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Wann Vorauszahlungsrechnungsstellung oder Vorauszahlungen verwenden

| Vorauszahlungsrechnungsstellung                                                                | Vorauszahlungen                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Vorauszahlungswerte können für eine Bestellung definiert werden,                                    | Kein Vorauszahlungswert ist für die Bestellung definiert.                    |
| Schlüssel: Eine Vorauszahlungsrechnung und eine Endabrechnung müssen gebucht werden.                       | Keine Vorauszahlungsrechnung muss gebucht werden.                                    |
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
4.  Nachdem der Kreditor die Waren oder Dienstleistungen geliefert hat und die zugehörige Kreditorenrechnung eingegangen ist, wendet der Kreditorenkoordinator den bereits geleisteten Vorauszahlungsbetrag auf die Rechnung an.
5.  Der Kreditorenkoordinator begleicht dann den verbleibenden Rechnungsbetrag.




