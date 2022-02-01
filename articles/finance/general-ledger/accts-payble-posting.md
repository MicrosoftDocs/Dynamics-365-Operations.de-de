---
title: Kreditorenkontenbuchungen
description: In diesem Thema wird erläutert, wie Buchungen in der Kreditorenbuchhaltung konfiguriert werden, und es werden Beispiele für Buchungskonfigurationen bereitgestellt.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb3ebad31c9f41e405b9fc31a0f71df05fa1cc60
ms.sourcegitcommit: 10b85a09e8a550155a69aa2a8877a7c88b887242
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/20/2022
ms.locfileid: "8014468"
---
# <a name="accounts-payable-posting"></a>Kreditorenkontenbuchung

[!include [banner](../includes/banner.md)]

Das primäre Buchungsprofil für das **Kreditorenkonten**-Modul ist das Kreditorbuchungsprofil. Dieses Buchungsprofil bestimmt das Summenkonto, das verwendet wird, wenn Kreditorensalden in das Hauptbuch gebucht werden. Ein Sammelkonto ist ein Hauptkonto. Es wird auch als Handelskonto für Kreditorenkonten bezeichnet.

Weitere Informationen finden Sie unter [Kreditorenbuchungsprofile](../accounts-payable/vendor-posting-profiles.md).

Neben dem Kreditorenbuchungsprofil sind mehrere Buchungskonfigurationen in der Kreditorenbuchhaltung verfügbar. Die folgenden Abschnitte enthalten mehr Informationen zu diesen anderen Buchungskonfigurationen.

## <a name="methods-of-payment-posting-accounts"></a>Buchungskonten für Zahlungsmethoden

Zahlungsmethoden definieren, wie eine Zahlung im Hauptbuch gebucht wird. Sie steuern auch das Verhalten der Zahlungsausgabe. In der Regel wird eine Zahlungsmethode für jeden Zahlungstyp erstellt, den Ihre Organisation ausführt (z. B. Bargeld, Scheck, Kreditkarte, Zahlungsanweisung und Überweisung).

Die Felder im **Buchung**-Abschnitt im Inforegister **Allgemein** auf der **Zahlungsmethode**-Seite (**Kreditorenbuchhaltung > Zahlungseinstellungen > Zahlungsmethoden**) steuern, wie eine Zahlung im Hauptbuch gebucht wird. Sie müssen zuerst einen Wert im Feld **Kontotyp** auswählen. Der ausgewählte Kontotyp steuert das Verhalten des **Zahlungskonto**-Felds. Wir empfehlen **Bank** im **Kontotyp** Feld und dann das Bankkonto im **Zahlungskonto**-Feld auszuwählen. Der Vorteil dieses Ansatzes besteht darin, dass das System die Zahlung im Nebenbuch der Bank verbucht, was die Abstimmung und andere bargeldbezogene Prozesse unterstützt. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils, wenn Sie das **Bargeld- und Bankmanagement**-Modul verwenden.

| Buchungstyp | Kontotyp | Zahlungskonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank of America | Bankkonto, das mit einer Analge verknüpft ist | Belastung | Nein | Geben Sie für jede Zahlungsmethode das Hauptkonto im **Zahlungskonto**-Feld ein. |

Wenn Sie die Bargeld- und Bankverwaltung nicht verwenden möchten, sollten Sie **Hauptbuch** im **Kontotyp**-Feld und dann das Hauptkonto im **Zahlungskonto**-Feld auswählen. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils, wenn Sie **Bargeld- und Bankmanagement** nicht verwenden.

| Buchungstyp | Kontotyp |Zahlungskonto-Beispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Unternehmen | Unternehmen | 100100: Bank of America | Anlage | Belastung | Nein | Geben Sie für jede Zahlungsmethode das Hauptkonto im **Zahlungskonto**-Feld ein. |

## <a name="bridging-accounts"></a>Transferkonten

Die Transferbuchung ist ein zweistufiger Prozess, der verwendet wird, wenn Zahlungen gebucht werden. Es handelt sich um eine optionale Funktion, die beispielsweise bei Bankkonten mit Nullsaldo verwendet werden kann. Er kann dazu beitragen, einen reibungsloseren und zeitnaheren Bankabstimmungsprozess zu gewährleisten. Im ersten Schritt wird eine Zahlung auf ein temporäres Konto (das Transferkonto) gebucht. Im zweiten Schritt wird die gebuchte Buchung storniert und auf das Bankkonto gebucht, wenn die Zahlung von der Bank verrechnet wird. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils für die Transferbuchung.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Erstellte Journale | 130725 | Nicht verrechnetes Bargeld | Passivposten | Belastung | Ja | Geben Sie für jede Zahlungsmethode das Hauptkonto im **Transferkonto**-Feld ein. |

Weitere Informationen finden Sie unter [Transferzahlungen einrichten und verarbeiten](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Debitoren-Skontobuchungskonten

Wenn Ihre Organisation Skonti von Kreditoren als Gegenleistung für eine schnelle Zahlung erhält, müssen Sie Skontocodes konfigurieren und angeben, wie die Skonti im Hauptbuch gebucht werden sollen. Für die Angabe des Hauptkontos, über das ein Debitorenskonto gebucht wird, stehen mehrere Möglichkeiten zur Verfügung.

Weitere Informationen finden Sie unter [Skonti](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Buchungskonten für Zahlungsgebühren

Mit Zahlungsgebühren können Sie einer Kreditorenzahlung automatisch eine Gebühr hinzufügen, wenn eine Reihe von Bedingungen zutrifft. Zahlungsgebühren können an den Kreditor gezahlt oder als Aufwand auf Ihr Bankkonto gebucht werden. Im Folgenden finden Sie einige Beispiele hierfür:

- Ein Anbieter berechnet Ihnen 3 Prozent des Gesamtbetrags der Zahlung, wenn Sie mit einer Kreditkarte bezahlen.
- Ihre Bank berechnet Ihnen 1,00 USD für jede Überweisung, die Sie verarbeiten, und die Überweisungsgebühr wird als Aufwand verrechnet.

Wenn Sie eine Kreditorenzahlungsgebühr konfigurieren, wenn Sie das **Gebühr**-Feld auf **Kreditor** festlegen, ist das **Hauptkonto** nicht verfügbar, und das System verwendet das Kreditorenbuchungsprofil, um die Gebühr zu buchen. Wenn Sie das **Belastung**-Feld auf **Sachkonto** festlegen, müssen Sie das **Hauptkonto**-Feld auf das Hauptkonto festlegen, wo die Zahlungsgebühr gebucht wird. Dieses Hauptkonto ist in der Regel ein Ausgabenkonto. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils für die Zahlungsgebührbuchung.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Erstellte Journale | 618190 | Bankgebührausgaben | Ausgaben | Belastung | Nein | Wenn **Sachkonto** im **Gebuhr**-Feld ausgewählt wurde, wählen Sie dieses Konto im **Hauptkonto**-Feld auf der Seite **Zahlungsgebühr** aus. |

Weitere Informationen finden Sie unter [Kreditorenzahlungsübersicht definieren](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Buchungskonten für Belastungscodes

Wenn Sie Kaufbeträge oder Einkaufsbeträge zusätzlich zu den Positionsartikeln nachverfolgen müssen, können Sie Belastungscodes verwenden. Beispielsweise kann Ihr Kreditor Ihnen Fracht- und Bearbeitungsgebühren in Rechnung stellen oder einige Fracht- und Bearbeitungsgebühren intern in Rechnung stellen. Sie können angeben, ob diese Beträge in Ausgabenkonten gebucht oder ob den Kosten der Artikel hinzugefügt werden sollen.

Sie können Belastungscodes für Debitoren und Kreditorenkonten erstellen. Wenn Sie einen Belastungscode konfigurieren, müssen Sie die Buchung definieren. Die Buchung steuert sowohl das Sollkonto als auch das Habenkonto. Wenn Sie Gebührencodes erstellen, können Sie den Buchungstyp auswählen, die für jeden Belastungscode verwendet wird. Die folgende Tabelle zeigt Beispiele für typische Belastungscodes für Kreditorenkonten auf der **Belastungscodes**-Seite.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Einkaufsgebühren | Lassen Sie das Feld leer. | Nicht zutreffend | Artikel | Belastung | Nein | **Beispiel für eine Kaufgebühr für einen Artikel:** </p><ul><li>**Solltyp**-Feld = **Artikel**</li><li>  **Habentyp**-Feld = **Debitor/Kreditor**.</li><li> Die Artikelbuchung verwendet das Hauptkonto aus dem Bestandsbuchungsprofil. |
| Auftrag, Fracht | 600120 | Frachteingang | Umsatzerlös | Belastung | Nein | **Beispiel für Fracht, die an einen Kreditoren bezahlt wird:** </p><ul><li>**Solltyp**-Feld = **Sachkonto**</li><li> **Habentyp**-Feld = **Debitor/Kreditor** |
| Rückvergütung\* | 503160 | Kreditorrabatt (Kontra COGS)| Ausgaben | Gutschrift | Nein | **Beispiel für einen Kreditorrabatt:**</p><ul><li>**Solltyp**-Feld = **Debitor/Kreditor**</li><li>**Habentyp**-Feld = **Sachkonto** |

\* Beim Rabattbeispiel wird die Buchung nur verwendet, wenn ein Belastungscode zu einem Bestellkopf oder einer Position hinzugefügt wird. Die erweiterte Rabattfunktion, die in Microsoft Dynamics 365 Supply Chain Management verfügbar ist, bietet mehr Kontrolle und Automatisierung von Rabatten. Weitere Informationen finden Sie unter [Kreditorenrabatte](../../supply-chain//procurement/vendor-rebates.md).

Die vorstehende Tabelle zeigt drei typische Beispiele für Buchungstypen, die für Belastungscodes verwendet werden können. Sie soll als Richtlinie und Musterauswahl dienen. Sie bietet keine umfassende Liste aller möglichen Kombinationen oder Buchungstypen, die verwendet werden können.

Weitere Informationen finden Sie unter [Belastungscodes erstellen](../accounts-receivable/create-charges-codes.md).
