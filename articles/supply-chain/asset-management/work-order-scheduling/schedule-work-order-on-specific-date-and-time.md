---
title: Planen Sie den Arbeitsauftrag auf ein bestimmtes Datum und eine bestimmte Uhrzeit.
description: In diesem Abschnitt wird erläutert, wie Sie einen Arbeitsauftrag zu einem bestimmten Datum und einer bestimmten Uhrzeit im Anlagenmanagement einplanen.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 827f4ca16341d29413f1b1d928965aa1919abf59
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822514"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Planen Sie den Arbeitsauftrag auf ein bestimmtes Datum und eine bestimmte Uhrzeit.

[!include [banner](../../includes/banner.md)]

 

Wenn ein Arbeitsauftrag zu einem bestimmten Datum *und* Uhrzeit terminiert werden muss, können Sie die Standardterminierung in der Anlagenverwaltung übersteuern und einen bestimmten Zeitplan für einen Arbeitsauftrag erstellen.

1. Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Klicken Sie in der Arbeitsauftragsliste auf die Arbeitsauftrags-ID in der Spalte **Auftrag**.

3. Klicken Sie auf **Bearbeiten**.

4. Fügen Sie in den Feldern **Arbeitsauftragskopf** FastTab Start- und Enddaten und -zeiten in die Felder **Erwarteter Start** und **Erwartetes Ende** ein.

    ![Abbildung 1](media/05-work-order-scheduling.png)

5. Klicken Sie auf der Registerkarte **Allgemein** auf **Terminplan**, um den Standardplanungsprozess zu verwenden, oder klicken Sie auf **Terminierung**, wenn Sie den Arbeitsauftrag einem bestimmten Mitarbeiter zuweisen möchten.

6. Um vorhandene Kapazitätsreservierungen zu überschreiben, um sicherzustellen, dass der Arbeitsauftrag im erwarteten Zeitraum terminiert wird, treffen Sie die Auswahl wie in der folgenden Abbildung im Abschnitt **Arbeitsauftrag terminieren** Dialog > **Endliche Kapazität** gezeigt. Dies bedeutet, dass der Terminierungsprozess bestehende Kapazitätsreservierungen ignoriert, da der Arbeitsauftrag zum erwarteten Startzeitpunkt beginnen muss.

    ![Abbildung 2](media/06-work-order-scheduling.png)

7. Klicken Sie auf **OK**, um die Planung zu starten.

8. Wenn die Terminierung zu Doppelbuchungen führt, erhalten Sie eine Meldung auf dem Bildschirm und können die zugehörigen Arbeitsaufträge anpassen.

>[!NOTE]
>Um einen Instandhalter für den Arbeitsauftrag zu planen, muss dieser zum erwarteten Starttermin verfügbar sein. Die Verfügbarkeit der Mitarbeiter wird im [Arbeiterkalender](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md) eingestellt. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]