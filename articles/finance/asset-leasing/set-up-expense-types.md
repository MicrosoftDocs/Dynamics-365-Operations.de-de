---
title: Ausgabentypen einrichten
description: In diesem Thema wird erläutert, wie Sie in Ausgabenarten im Anlageleasing einrichten.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880983"
---
# <a name="set-up-expense-types"></a>Ausgabentypen einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie in Ausgabenarten im Anlageleasing einrichten. Kosten, die nicht im Zahlungsplan enthalten sind, werden als *Ausgabenkosten* bezeichnet. Beispiele für diese Kosten sind Grundsteuern, Wartungskosten für Gemeinschaftsräume und Versicherungskosten.

## <a name="add-an-administrative-expense-type"></a>Einen Verwaltungsausgabentyp hinzufügen

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Ausgabentypen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie in die entsprechenden Felder den neuen Ausgabentyp und eine Beschreibung ein.

## <a name="assign-accounts-to-administrative-costs"></a>Konten den Verwaltungskosten zuweisen

Als Nächstes sollten Sie den Ausgabentypen Konten zuordnen. Diese Konten werden belastet, wenn Einträge des Ausgabenplans gebucht werden. Das Gegenkonto ist auf den **Zahlungsplan für Nebenkosten beim Leasing**-Zeilen auf jedem Mietvertrag angegeben.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Anlagenleasing-Parameter**.
2. Wählen Sie auf der **Konten**-Registerkarte auf dem **Nebenkosten beim Leasing Ausführungskosten**-Inforegister im **Ausgabentyp**-Feld den Ausgabentyp aus.
3. Wählen Sie **Hinzufügen** aus.
4. Wählen Sie im **Buchtyp**-Feld den Buchtyp aus, der mit den Verwaltungskosten verknüpft werden soll.

    > [!NOTE]
    > Mehrere Bucharten können mit demselben Ausgabenkonto verknüpft werden.

5. Geben Sie im Feld **Kontocode** an, auf welche Mietverträge das Buch angewendet werden soll:

    - **Alle** – Das Buch für alle Mietverträge anwenden.
    - **Gruppe** – Das Buch auf eine bestimmte Gruppe von Mietverträgen anwenden.
    - **Tabelle** – Das Buch für bestimmte Mietverträge anwenden.

6. Wenn Sie **Gruppe** oder **Tabelle** im Feld **Kontocode** gewählt haben, wählen Sie eine Kontonummer oder Gruppennummer im Feld **Konto-/Gruppennummer** aus.
7. Wählen Sie in den entsprechenden Feldern das Hauptkonto für Finanzierungsleasing und das Hauptkonto für Ausrüstungs-Leasingvertrag aus.

Wenn Sie diese Schritte ausgeführt haben, können Sie Ausgaben über **Zahlungsplan für Nebenkosten beim Leasing**-Zeilen auf der **Mietvertragsdetails**-Seite eines ausgewählten Mietvertrags hinzufügen. Alternativ können Sie beim Erstellen eines neuen Mietvertrags Kosten hinzufügen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
