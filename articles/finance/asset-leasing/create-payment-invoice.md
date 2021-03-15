---
title: Zahlungsrechnungen erstellen
description: In diesem Thema wird erläutert, wie Sie monatliche Mietrechnungen erstellen. Sie können Rechnungen für einzelne Mietverträge erstellen oder sie mithilfe eines Stapelverarbeitungsprozesses für mehrere Mietverträge erstellen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969577"
---
# <a name="create-payment-invoices"></a>Zahlungsrechnungen erstellen

[!include [banner](../includes/banner.md)]

Sie können monatliche Rechnungen für einzelne Mietverträge erstellen oder sie mithilfe eines Stapelverarbeitungsprozesses für mehrere Mietverträge erstellen. Das folgende Verfahren zeigt, wie Sie einen individuellen Mietzahlungseintrag erstellen, wenn der **An Kreditor bezahlen**-Parameter auf der **Leasingbuch-Einrichtung**-Seite eingeschaltet ist.

1. Auf der **Mietvertragsübersicht**-Seite, wählen Sie einen Mietvertrag und dann **Bücher \> Zahlungsplan**.
2. Wählen Sie die Zahlung aus, die ausgeführt werden muss, und wählen Sie dann **Erfassung erstellen**. Sie erhalten eine Nachricht, die besagt, dass für die ausgewählte Zahlung eine Erfassung erstellt wurde.
3. Wählen Sie **Rechnungserfassungen** und dann die Rechnung aus, die bezahlt werden muss.
4. Auf der Registerkarte **Zeilen** überprüfen Sie den Journaleintrag, bevor Sie ihn im Hauptbuch buchen.

    > [!NOTE]
    > Standardmäßig verwenden die erstellten Kreditorenrechnungszeilen das Kreditorenbuchungsprofil aus der **Kreditorenparameter**-Seite.

5. Wählen Sie die korrekte Erfassung und dann die Rechnung aus, die bezahlt werden muss.

    Für dieses Beispiel ist der **An den Kreditor bezahlen**-Parameter im Leasingbuch aktiviert. Daher befindet sich die Rechnung in der Rechnungserfassung. Der **Übersicht**-Abschnitt zeigt eine Zusammenfassung des Journaleintrags, und der **Zeilen**-Abschnitt zeigt Details der tatsächlichen Erfassungszeilen.

    > [!NOTE]
    > Wenn der **An den Kreditor bezahlen**-Parameter deaktiviert ist, werden die Einträge in der Zahlungserfassung auf der **Anlagenleasing**-Seite für das Leasingbuch aufgeführt, und das System erstellt anstelle einer Rechnung einen Eintrag für das Anlagenleasing. Der Eintrag für die Mietzahlung wird auf den Erfassungsnamen gebucht, der im Feld **Monatliches Mieterfassung** angegeben ist.

6. Nachdem die Transaktion gebucht wurde, können Sie die Transaktionsinformationen und den Buchwert der Leasingverbindlichkeit anzeigen, indem Sie **Verbindlichkeitstransaktionen** im Leasingbuch auswählen.

    Im Zahlungsplan wird das Kontrollkästchen **Erfassung gebucht** aktiviert und in der Zeile wird die Rechnungserfassungsnummer angezeigt. Nachdem eine Zahlungserfassung und ein Eintrag für diese Erfassung erstellt wurden, müssen Sie den Eintrag stornieren, bevor er neu erstellt werden kann.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]