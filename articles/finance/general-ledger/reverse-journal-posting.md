---
title: Buchungserfassung stornieren
description: In diesem Thema wird die Funktion beschrieben, mit der Belege von der Belegbuchungsliste oder von Finanzerfassungen storniert werden können.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248584"
---
# <a name="reverse-journal-posting"></a>Buchungserfassung stornieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Funktion von Microsoft Dynamics 365 Finance beschrieben, die es Ihnen ermöglicht, eine gesamte Erfassung zu stornieren oder eine oder mehrere Belege aus der Belegbuchungsliste unabhängig von ihrem Ursprung umzukehren. 

## <a name="reversing-journals"></a>Stornieren von Erfassungen

Sie können Erfassungspositionen einzeln stornieren. Mit Rückerfassungsbuchung können Sie eine gesamte Finanzerfassung auch stornieren. So stornieren Sie eine Erfassung 
- Öffnen Sie die Finanzerfassung und filtern Sie die gebuchten Erfassungen
- Klicken Sie im Menü „Stornieren“ oben auf der Seite.
- Sie sehen die Gesamtanzahl von Belegen und Belegpositionen sowie den Gesamtbetrag der Positionen, die storniert werden
- Wählen Sie die Option „Ja“ aus, um ein vorhandenes Buchungsdatum zu verwenden, oder „Nein“, um ein neues zu verwenden. In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.
- Wenn Sie „Nein“ ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein. 
- Geben Sie einen Kommentar ein, der der Stornobuchung hinzugefügt werden soll
- Klicken Sie auf die Schaltfläche „Stornieren“.

Die Buchungen werden storniert. 

Wenn die Anzahl der Belegpositionen 100 übersteigt, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt. Sie können die Ergebnisse einer Stornierung überprüfen, indem Sie die Kommentare im Stapelverarbeitungsauftrag anzeigen, der ausgeführt wurde. Alle Fehler werden in der Historie vermerkt.

Wenn die Anzahl der Belegpositionen 100 oder weniger beträgt, wird der Umkehr-Prozess sofort ausgeführt. Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte. Um das Dialogfeld zu schließen, klicken Sie auf „OK“.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Stornieren von Belegen mit der Belegbuchungsliste. 

Sie können alle Belege von der **Belegbuchungsliste** in allen untergeordneten Sachkonten stornieren. Darüber hinaus können Sie mehrere Belege gleichzeitig stornieren. 

So stornieren Sie einen oder mehrere Belege: 
- Klicken Sie im Menü „Stornieren“ oben auf der Seite.
- Sie sehen die Gesamtanzahl von Belegen und Belegpositionen sowie den Gesamtbetrag der Positionen, die storniert werden
- Wählen Sie die Option „Ja“ aus, um ein vorhandenes Buchungsdatum zu verwenden, oder „Nein“, um ein neues zu verwenden. In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.
- Wenn Sie „Nein“ ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein. 
- Geben Sie einen Kommentar ein, der der Stornobuchung hinzugefügt werden soll
- Klicken Sie auf die Schaltfläche „Stornieren“.

Die Buchungen werden storniert. 

Wenn die Anzahl der Belegpositionen 100 übersteigt, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt. Sie können die Ergebnisse einer Stornierung überprüfen, indem Sie die Kommentare im Stapelverarbeitungsauftrag anzeigen, der ausgeführt wurde. Alle Fehler werden in der Historie vermerkt.

Wenn die Anzahl der Belegpositionen 100 oder weniger beträgt, wird der Umkehr-Prozess sofort ausgeführt. Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte. Um das Dialogfeld zu schließen, klicken Sie auf „OK“.

