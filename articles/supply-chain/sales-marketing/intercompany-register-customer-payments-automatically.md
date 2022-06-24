---
title: Zahlungen für Intercompany-Debitorenrechnungen automatisch erfassen
description: In diesem Artikel wird erläutert, wie Zahlungen für Intercompany-Debitorenrechnungen automatisch registriert werden.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878786"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Zahlungen für Intercompany-Debitorenrechnungen automatisch erfassen

[!include [banner](../../includes/banner.md)]

Beim Buchen einer Intercompany-Debitorenrechnung wird von Microsoft Dynamics 365 Supply Chain Management eine Debitorenbuchung erstellt. Diese Debitorenbuchung bleibt so lange offen, bis sie ausgeglichen (also bezahlt) wird. Wenn die zugehörige Intercompany-Bestellung rechnungsaktualisiert wird, wird eine Kreditorenbuchung erstellt, die der Debitorenbuchung entspricht. Diese Kreditorenbuchung bleibt ebenfalls offen, bis sie ausgeglichen wird. Zum Minimieren des Risikos von Differenzen kann automatisch eine Debitoren-Zahlungserfassung erstellt und zusammen mit der Kreditoren-Zahlungserfassung gebucht werden.

1. Wechseln Sie zu **Vertrieb und Marketing \> Debitoren \> Alle Debitoren**.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Intercompany** aus.
1. Wählen Sie zum Einrichten der Intercompany-Debitorenzahlungen auf der Seite **Intercompany** den Link **Auftragsrichtlinien** aus.
1. Wählen Sie im Feld **Zahlungserfassung** die Debitoren-Zahlungserfassung aus, für die Intercompany-Kreditorenzahlungen erfasst werden sollen. Dies wird auf der Seite **Debitorenparameter** eingerichtet.
1. Wenn die Buchung in diese Erfassung automatisch erfolgen soll, aktivieren Sie das Kontrollkästchen **Erfassung automatisch buchen**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
