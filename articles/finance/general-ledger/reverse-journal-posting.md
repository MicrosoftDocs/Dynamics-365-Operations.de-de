---
title: Buchungserfassung stornieren
description: In diesem Artikel wird die Funktion beschrieben, mit der Belege von der Belegbuchungsliste oder von Finanzerfassungen storniert werden können.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.form: LedgerTransVoucher, LedgerJournalTable
ms.openlocfilehash: 8912409ec0d2016ea4af12843319febda98663c5
ms.sourcegitcommit: e700528679a821237e644b3e21058c36ae1323c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2022
ms.locfileid: "9680383"
---
# <a name="reverse-journal-posting"></a>Buchungserfassung stornieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird die Funktion von Microsoft Dynamics 365 Finance beschrieben, die es Ihnen ermöglicht, eine gesamte Erfassung zu stornieren oder ein oder mehrere Belege aus der Belegbuchungsliste unabhängig von ihrem Ursprung umzukehren. 

Bevor Sie eine der beschriebenen Funktionen verwenden können, müssen Sie sie in Ihrem System aktivieren. Administratoren können mit der Einstellung **Funktionsverwaltung** den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:
 - Modul: Hauptbuchmodul
 - Funktionsname: **Massenstornos für mehrere Belege**

## <a name="reversing-journals"></a>Stornieren von Erfassungen

Sie können Erfassungspositionen einzeln stornieren. Mit Rückerfassungsbuchung können Sie eine gesamte Finanzerfassung auch stornieren. So stornieren Sie eine Erfassung 

- Filtern Sie nach den gebuchten Erfassungen und öffnen Sie die Ansicht **Zeilen** in der Erfassung.
- Wählen Sie das Menü **Gesamte Erfassung stornieren** oben auf der Seite.
- Sie sehen die Gesamtanzahl von Belegen und Belegpositionen sowie den Gesamtbetrag der Positionen, die storniert werden.
- Wählen Sie die Option **Ja** aus, um ein vorhandenes Buchungsdatum zu verwenden, oder **Nein**, um ein neues zu verwenden. In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.
- Wenn Sie **Nein** ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein. 
- Geben Sie einen Kommentar ein, der der Stornobuchung hinzugefügt werden soll.
- Wählen Sie die Schaltfläche **Stornieren**.

Die Buchungen werden storniert. 

Wenn der Beleg mehr als 100 Positionen enthält, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt. Sie können die Ergebnisse überprüfen, indem Sie die Kommentare im Batchauftrag anzeigen, der ausgeführt wurde. Alle Buchungen, die nicht storniert werden konnten, werden in der Historie des Batchauftrags aufgeführt.

Wenn der Beleg 100 oder weniger Positionen enthält, wird der Umkehr-Prozess sofort ausgeführt. Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Stornieren von Belegen mit der Belegbuchungsliste. 

Sie können alle Belege von der **Belegbuchungsliste** in allen untergeordneten Sachkonten stornieren. Darüber hinaus können Sie mehrere Belege gleichzeitig stornieren. 

So stornieren Sie einen oder mehrere Belege: 

- Wählen Sie das Menü **Gesamte Erfassungs-Dropdownliste stornieren** oben auf der Seite.
- Sie sehen die Gesamtanzahl von Belegen und Belegpositionen und den Gesamtbetrag der Positionen, die storniert werden.
- Wählen Sie die Option **Ja** aus, um ein vorhandenes Buchungsdatum zu verwenden, oder **Nein**, um ein neues zu verwenden. In einigen Fällen wird die Periode der ursprünglichen Buchung unter Umständen abgeschlossen und Sie müssen ein neues Buchungsdatum für die Stornierung eingeben.
- Wenn Sie **Nein** ausgewählt haben, geben Sie das Buchungsdatum für die Stornierung ein. 
- Geben Sie einen Kommentar ein, um die Stornobuchung zu beschreiben.
- Wählen Sie die Schaltfläche **Stornieren**.

Die Buchungen werden storniert. 

Wenn der Beleg mehr als 100 Positionen enthält, wird der Umkehr-Prozess mithilfe der Stapelverarbeitung ausgeführt. Sie können die Ergebnisse überprüfen, indem Sie die Kommentare im Batchauftrag anzeigen, der ausgeführt wurde. Alle Buchungen, die nicht storniert werden konnten, werden in der Historie des Batchauftrags aufgeführt.

Wenn die Anzahl der Belegpositionen 100 oder weniger beträgt, wird der Umkehr-Prozess sofort ausgeführt. Die Ergebnisse werden in einem Dialogfeld angezeigt, das Belege, die nicht storniert werden konnten, und den Grund anzeigt, warum nicht storniert werden konnte. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.

Buchungen können nur storniert werden, wenn sie die Geschäftsregeln für das Zurücksetzen sie gelten. Kreditorenzahlungen können nicht mithilfe der Funktion storniert werden, die in diesem Artikel beschrieben wird. Kreditorenzahlungen müssen storniert werden, indem die Schritte unter [Stornieren einer Kreditorenzahlung](../accounts-payable/reverse-vendor-payment.md) ausgeführt werden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
