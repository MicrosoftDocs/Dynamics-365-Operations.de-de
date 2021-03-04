---
title: Kreditorenkonten – Startseite
description: Dieses Thema enthält eine Übersicht über die Kreditorenkonten.
author: ShylaThompson
manager: AnnBe
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a0195c6776b5065d98b6b1d4d9795248c6bf4c74
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972154"
---
# <a name="accounts-payable-home-page"></a>Kreditorenkonten – Startseite

[!include [banner](../includes/banner.md)]

Dieses Thema enthält eine Übersicht über die Kreditorenkonten. 

Sie können Kreditorenrechnungen manuell eingeben oder elektronisch über eine Datenentität empfangen. Nachdem Rechnungen eingegeben oder empfangen wurden, können sie mithilfe einer Rechnungsgenehmigungserfassung oder über die Seite **Kreditorenrechnung** geprüft und genehmigt werden. Sie können den Prüfungsprozess mit einem Rechnungsabgleich, Kreditorenrechnungsrichtlinien und Workflows automatisieren, sodass bestimmten Kriterien entsprechende Rechnungen automatisch genehmigt und die übrigen Rechnungen zur Prüfung durch einen autorisierten Benutzer markiert werden.

**Geschäftsprozesse**

[![Geschäftsprozessdiagramm](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Einrichten von Kreditorenkonten

Richten Sie Kreditorengruppen, Kreditorenkonten, Buchungsprofile, verschiedene Zahlungsoptionen sowie Parameter zu Kreditorenkonten, Gebühren, Lieferungen und Ziele, Solawechsel und andere Typen von Kreditorenkontendaten ein. 

[Kreditorenkonten konfigurieren – Übersicht](accounts-payable-overview.md)

[Buchhaltungsverteilungen und Journaleinträge im untergeordneten Sachkonto für Kreditorenrechnungen](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Neubewertung der Fremdwährung für Kreditorenkonten und Debitoren](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Kreditorenrechnungen konfigurieren

Verwenden Sie Kreditorenkonten, um Rechnungen und Aufwendungen an Kreditorenkonten zu verfolgen.

[Rechnungsabgleich von Kreditorenkonten – Übersicht](accounts-payable-invoice-matching.md)

[Kreditorenbuchungsprofile](vendor-posting-profiles.md)

[Überprüfung des Kreditorenkonten-Rechnungsabgleichs einrichten](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Dreiseitige Abgleichsrichtlinien](three-way-matching-policies.md)

[Rechnungsabgleich sowie Intercompany-Bestellungen](invoice-matching-intercompany-purchase-orders.md)

[Beheben von Abweichungen beim Abgleich von Rechnungssummen – Übersicht](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Standardgegenkonten für Kreditorenrechnungserfassungen und Rechnungsgenehmigungserfassungen](default-offset-accounts-vendor-invoice-journals.md)

[Mobile Rechnungsgenehmigungen](mobile-invoice-approvals.md)

[Arbeitsbereich für Kreditorkooperationsrechnungen](vendor-portal-invoicing-workspace.md)

[Kreditorenrechnungsautomatisierung](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Kreditorenzahlungen konfigurieren 

Sie können jeder beliebigen benutzerdefinierten Zahlungsmethode einen vom System definierten Zahlungstyp zuweisen, wie Scheck, elektronischer Zahlungsverkehr oder Solawechsel. Zahlungstypen sind optional. Sie sind jedoch hilfreich, wenn Sie elektronische Zahlungen überprüfen und sie schnell feststellen möchten, welcher Zahlungstyp bei einer Zahlung verwendet wird. 

[Arbeitsbereich für Kreditorenzahlungen](vendor-payments-workspace.md)

[Gebühren für Kreditorenzahlung definieren](tasks/define-vendor-payment-fees.md)

[Kreditorenzahlungsbedingungen definieren](tasks/define-vendor-payment-terms.md)

[Überblick über die positive Zahlung](positive-pay-overview.md)

[Einrichten und Generieren von Dateien für positive Zahlungen](set-up-generate-positive-pay-files.md)

[Kreditorenzahlungen unter Verwendung eines Zahlungsvorschlags erstellen](create-vendor-payments-payment-proposal.md)

[Kreditorenzahlungen für einen Teilbetrag](vendor-payments-partial-amount.md)

[Einen Rabatt in Anspruch nehmen, der höher ist, als der berechnete Rabatt für eine Kreditorenzahlung](take-discount-more-calculated-discount-vendor-payment.md)

[Ein Skonto außerhalb der Skontoperiode in Anspruch nehmen](take-cash-discount-outside-cash-discount-timeframe.md)

[Beispiel für die elektronische Berichterstellung für Kreditorenschecks](electronic-reporting-sample-vendor-checks.md)

[Stornieren einer Kreditorenzahlung](reverse-vendor-payment.md)

[Vorauszahlungsrechnungen im Vergleich zu Vorauszahlungen](prepayments-invoices-vs-prepayments.md)

[Zentralisierte Zahlungen für Kreditorenkonten](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Bedarfsdeckung

Unter den folgenden Themen finden Sie Informationen zum Verwalten von Ausgleichen. Ausgleich ist der Prozess für das Ausgleichen von Zahlungen mit Rechnungen. 

[Konfigurieren eines Ausgleichs](../cash-bank-management/configure-settlement.md)

[Ausgleich einer teilweisen Kreditorenzahlung vor dem Skontodatum mit einer abschließenden Zahlung nach dem Skontodatum](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Ausgleich einer teilweisen Kreditorenzahlung, bei der es Rabatte auf Kreditorengutschriften gibt](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Ausgleichen einer teilweisen Kreditorenzahlung, die mehrere Rabattzeiträume hat](settle-partial-vendor-payment-multiple-discount-periods.md)

[Ausgleichen einer teilweisen Kreditorenzahlung und Ausgleichen der abschließenden vollständigen Zahlung vor dem Skontodatum](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Einzelner Beleg mit mehreren Debitoren- oder Kreditorendatensätzen](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Zusätzliche Ressourcen

#### <a name="whats-new-and-in-development"></a>Neuerungen und Entwicklungen

Lesen Sie die [Microsoft Dynamics 365-Veröffentlichungspläne](https://go.microsoft.com/fwlink/?linkid=2010158), um zu erfahren, welche neuen Funktionen geplant sind. 

#### <a name="blogs"></a>Blogs

Meinungen, Neuigkeiten und weitere Informationen zu Kreditorenkonten und anderen Lösungen finden Sie im [Microsoft Dynamics 365-Blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) und dem [Microsoft Dynamics 365 Finance – Financials-Blog](https://community.dynamics.com/365/financeandoperations/b/financials).

Im [Microsoft Dynamics Operations-Partner-Community-Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) erfahren Microsoft Dynamics-Partner an zentraler Stelle alles über Neuerungen und Trends bei Dynamics 365.

#### <a name="community-blogs"></a>Communityblogs

[Verbindlichkeiten in Dynamics 365 Finance verwalten](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Aufgabenleitfäden
Weitere Hilfe finden Sie als Aufgabenleitfäden in der Anwendung. Um auf Aufgabenleitfäden zuzugreifen, klicken Sie auf einer beliebigen Seite auf die Schaltfläche „Hilfe“.

#### <a name="videos"></a>Videos

Sehen Sie in den Videos nach, die jetzt im [YouTube-Kanal zu Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) verfügbar sind.




