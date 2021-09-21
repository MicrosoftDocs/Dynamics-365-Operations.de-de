---
title: Das Konto „Auf Belastungskonto im Sachkonto buchen“-Einstellung ist nicht aktiviert
description: Dieses Problem tritt auf, wenn eine Bestellung in Rechnung gestellt wird, wenn die „Auf Belastungskonto im Sachkonto buchen“-Option auf der „Rechnung“-Registerkarte der „Lieferantenparameter“-Seite auf „Ja“ festgelegt ist
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476464"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Das Konto „Auf Belastungskonto im Sachkonto buchen“-Einstellung ist nicht aktiviert

## <a name="symptoms"></a>Symptome

Dieses Problem tritt auf, wenn eine Bestellung in Rechnung gestellt wird, wenn die **Auf Belastungskonto im Sachkonto buchen**-Option auf der **Rechnung**-Registerkarte der **Lieferantenparameter**-Seite auf *Ja* festgelegt ist.

## <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
1. Legen Sie auf der **Rechnung**-Registerkarte die **Auf Belastungskonto im Sachkonto buchen**-Option auf *Ja* fest.
1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Buchung \> Buchung**.
1. Stellen Sie auf der **Bestellung**-Registerkarte sicher, dass Sie alle Positionen in den Kaufausgaben für das Produkt gelöscht haben.
1. Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.
1. Erstellen einer Bestellung. Wählen Sie in dem **Lieferantenkonto**-Feld *1001 Acme Büromaterial* aus.
1. Fügen Sie eine Bestellung mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *D0011 Laserprojektor*
    - **Standort:** *1*
    - **Lagerort:** *11*
    - **Menge** *4*

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kauf** in der Gruppe **Aktion** auf **Bestätigen**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Empfangen** in der Gruppe **Generieren** auf **Produktzugang**.
1. Geben Sie im **Buchen des Produktzugangs**-Dialogfeld im **Produktzugang**-Feld eine beliebige Zahl ein und wählen Sie dann **OK**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
1. Geben Sie im **Nummer**-Feld eine beliebige Nummer als Rechnungsnummer ein.
1. Status des Abgleichs aktualisieren und buchen.
1. Beachten Sie, dass Sie jetzt die folgende Fehlermeldung erhalten, wenn Sie eine Rechnung aus einer Bestellung erstellen: „Kontonummer für den Transaktionstyp Einkaufsausgaben für Produkt ist nicht vorhanden.“

## <a name="resolution"></a>Lösung

Dies hängt von den Parametereinstellungen für Rechnungen und Rechnungsgruppen ab. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Buchhaltung für Einkaufskosten und Bestandsabweichungen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
