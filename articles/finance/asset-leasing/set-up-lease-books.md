---
title: Leasingbücher einrichten
description: In diesem Artikel werden die Informationen beschrieben, die in Leasingbüchern verwaltet werden. Leasingbücher enthalten die Rechnungslegungsgrundsätze, die bestimmen, wie ein Mietvertrag im System bilanziert wird.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ee8cb3c827d590a5eb91121fe4510fbc56c13d9a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903217"
---
# <a name="set-up-lease-books"></a>Leasingbücher einrichten

[!include [banner](../includes/banner.md)]

Leasingbücher enthalten die Rechnungslegungsgrundsätze, die bestimmen, wie ein Mietvertrag im System bilanziert wird. Neben der Bilanzierung auf Cash-Basis unterstützt Anlagenleasing die folgenden Standards:

- Allgemein anerkannte Rechnungslegungsgrundsätze in den USA (US-GAAP)
- Thema 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842)
- ASC 840
- Internationaler Financial Reporting-Standard 16 (IFRS 16)
- International Buchführungsstandard 17 (IAS 17)

Gehen Sie folgendermaßen vor, um einen Mietvertrag zu erstellen.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasingbücher**.
2. Wählen Sie **Neu** aus, um ein Buch hinzuzufügen.
3. Stellen Sie die folgenden Felder ein.

    | Name                                     | Beschreibung |
    |------------------------------------------|-------------|
    | Buchungsebene                            | Wählen Sie die zu verwendende Buchungsebene aus. Jedes Buch, das einem Mietvertrag beigefügt ist, wird für eine bestimmte Buchungsebene eingerichtet. Jede Buchungsebene hat unterschiedliche Buchungszwecke. |
    | Mietvertragstyp                               | Wählen Sie aus, ob der Mietvertrag automatisch klassifiziert werden soll oder ob es als Finanzierungsleasing oder Ausrüstungs-Leasingvertrag vordefiniert werden soll. |
    | Buchhaltungsframework                     | Wählen Sie das Framework aus dass dem Buch zugeordnet ist. |
    | Einrichten von Mietdauer/Nutzungsdauer          | Das System klassifiziert den Mietvertrag als ein Finanzierungsleasing, wenn die Mietvertragsgart auf **Automatisch** eingestellt ist und das Verhältnis der Mietdauer zur Nutzungsdauer der Anlage größer oder gleich dem im Feld eingegebenen Prozentsatz ist.  |
    | Einrichtung von Barwert/Anlagenzeitwert   | Geben Sie eine ganze Zahl ein, um den Schwellenwert zu definieren, der den Mietvertragstyp bestimmt. Wenn der Barwert zukünftiger Mindestmietzahlungen höher ist als der benutzerdefinierte Wert aus der Buchkonfiguration, und wenn die Mietvertragsklassifizierung des Buches auf „Automatisch“ eingestellt ist, klassifiziert das System den Mietvertrag als Finanzierungsleasing. |
    | Kurzfristiger Schwellenwert                     | Geben Sie die Anzahl der Monate ein, die als Schwellenwert für kurzfristige Mietverträge verwendet werden sollen. Wenn die Laufzeit des Mietvertrags kleiner oder gleich der Anzahl der Monate ist, die Sie hier eingeben, klassifiziert das System den Mietvertrag als kurzfristigen Mietvertrag, und die Behandlung der zurückgestellten Miete wird angewendet. |
    | Schwellenwert für geringen Wert                      | Geben Sie einen Betrag ein, der als Schwellenwert für Leasingobjekte mit geringem Wert verwendet werden soll. Wenn der Zeitwert der Anlage kleiner oder gleich des hier eingegebenen Werts ist, klassifiziert das System den Mietvertrag als Leasingobjekt von geringem Wert, und die Behandlung der zurückgestellten Miete wird angewendet. |
    | An Kreditor bezahlen                            | Setzen Sie diese Option auf **Ja**, damit Mietzahlungen als Rechnung auf das in jedem Mietvertrag angegebene Kreditorenkonto gebucht werden können. Wenn eine Mietzahlung gebucht wird, wird das Kreditorenkonto gutgeschrieben. Wenn diese Option auf **Nein** gesetzt ist, wird stattdessen das Konto gutgeschrieben, das für die **Mietzahlung**-Buchungsart auf der **Leasingbuchungsparameter**-Seite angegeben ist. |
    | Leasingkonvention                       | Wählen Sie die Konvention für den Beginn des Mietvertrags aus:<ul><li><b>Keine</b> – Verwenden Sie das Startdatum des Mietvertrags als Anfangsdatum.</li><li><b>Voller Monat</b> – Verwenden Sie den ersten Tag des Monats, in den das Startdatum des Mietvertrags als Anfangsdatum fällt.</li></ul><p>Wenn Sie <b>Keine</b> auswählen, besteht das Risiko, dass die Zeitpläne für die Amortisierung von Verbindlichkeiten und die Abschreibung des Leasingobjekts in der Mitte des Monats und nicht am Monatsende anfallen und Ausgaben gebucht werden. Durch die Auswahl <b>Voller Monat</b> stellen Sie sicher, dass das System am ersten Tag des Monats mit der Buchung des Mietvertrags beginnt und dass die gesamten Ausgaben des Monats am letzten Tag des Monats anfallen und gebucht werden.</p><p><strong>Hinweis:</strong> Die Funktion für Leasingkonventionen muss über die Funktionsverwaltung aktiviert werden. Suchen und wählen Sie im Arbeitsbereich <b>Funktionsverwaltung</b> die Funktion namens <b>Leasingkonvention für das Anlagenleasing</b> aus. Wählen Sie anschließend <b>Jetzt aktivieren</b> aus.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
