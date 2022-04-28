---
title: Fälligkeitsdatenspeicher für Debitoren
description: In diesem Thema wird der Prozess der Verwendung von externem Speicher für Kundenalterungsdaten beschrieben. Sie können den Prozess zur Speicherung von Kundenalterungsdaten ausführen, um die Ausgabe für den Export in ein externes System bereitzustellen.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 497d49da84f4df90877908bef3031e079bc36066
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557877"
---
# <a name="customer-aging-data-storage"></a>Fälligkeitsdatenspeicher für Debitoren

[!include [banner](../includes/banner.md)]


In diesem Thema wird der Prozess der Verwendung von externem Speicher für Kundenalterungsdaten beschrieben. Sie können in Microsoft Dynamics 365 Finance den Prozess zur Speicherung von Kund\*innenalterungsdaten ausführen, um die Ausgabe für den Export in ein externes System bereitzustellen. Wenn Sie den Prozess ausführen, stehen den externen Systemen dieselben Fälligkeitsberichtsoptionen zur Verfügung, die im System verfügbar sind. Die Details sind immer in den exportierten Daten enthalten.

Es kann hilfreich sein, Kundenalterungsdaten einem externen System zur Speicherung zur Verfügung zu stellen, wenn die Ausgabe viele Kunden und/oder viele Transaktionen enthält. Wenn die vorhandene **Alterung des Kunden** Zeitüberschreitungen meldet, da zu viele Daten zum Drucken vorhanden sind, bietet diese Funktion eine alternative Möglichkeit, dieselben Daten abzurufen.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Aktivieren Sie die Datenspeicherungsfunktion für Kundenalterung

Bevor Sie diese Funktion nutzen können, müssen Sie sie auf Ihrem System aktivieren. Administratoren können mit den Einstellungen Funktionsverwaltung den Status der Funktion überprüfen und ggf. aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** Kredit und Inkasso
- **Funktionsname**: Aktivieren Sie die Datenspeicherung für Kundenalterung

## <a name="run-the-customer-aging-data-storage-process"></a>Führen Sie den Datenspeicherungsprozess für Kundenalterung aus

1. Wechseln Sie zu **Kredit und Inkasso \> Abfragen und Berichte \> Kunde \> Datenspeicherung für Kundenalterung**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** einen Namen für den Prozess ein.
4. Stellen Sie die restlichen Parameter nach Bedarf ein.

    > [!NOTE]
    > Transaktionsdetails sind immer enthalten und die Verarbeitung erfolgt immer in einem Batchauftrag.

5. Wählen Sie **OK** aus.
6. Aktualisieren Sie die **Datenspeicherung der Kundenalterung**-Seite, um die Werte **Batchname** und **Batch-Laufzeit** zu sehen, die zusammen mit dem **Bearbeitungsstatus**-Wert angezeigt werden. Wenn der Batchauftrag abgeschlossen ist, wird das **Bearbeitungsstatus**-Feld auf **Beendet** gesetzt und das **Anzahl der Alterungslinien** wird festgelegt. Wenn sich der Batchauftrag wiederholt, wird das **Bearbeitungsstatus**-Feld ist auf **Warten** gesetzt.
7. Wählen Sie die **Filter**-Schaltfläche neben dem **Anzahl der Alterungslinien**-Feld aus, um die Filter zu überprüfen, die für den Batchauftrag hinzugefügt wurden.

Die **Datenspeicherung der Kundenalterung**-Seite enthält keine Ergebnisse. Allerdings können Sie mit der **Datenspeicherung der Kundenalterung**-Datenentität die Ausgabe in ein beliebiges Format exportieren, das von der Datenverwaltung unterstützt wird.

> [!NOTE]
> Fügen Sie vor dem Exportieren einen Filter hinzu, um die exportierten Ergebnisse auf die neueste Alterung zu beschränken. Fügen Sie beispielsweise die folgenden Kriterien hinzu, um die letzten Batchausführung zurückzugeben:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> Fügen Sie wahlweise beispielsweise die folgenden Kriterien hinzu, um die letzten Batchausführung für den aktuellen Benutzer zurückzugeben:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
