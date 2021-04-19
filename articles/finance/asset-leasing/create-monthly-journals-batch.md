---
title: Monatliche Erfassungseinträge in einem Batch erstellen
description: In diesem Thema wird erläutert, wie Sie Journaleinträge in einem Batch erstellen, um die Effizienz bei der Erfassung monatlicher Mietkosten zu steigern.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 664001dd6e9da449dec65750da53d58bd27438b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816027"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Monatliche Erfassungseinträge in einem Batch erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Journaleinträge in einem Batch erstellen, um die Effizienz bei der Erfassung monatlicher Mietkosten zu steigern. Mit der Stapelverarbeitung können Journaleinträge aus mehreren Zeitplänen erstellt werden. Diese Journaleinträge können Mietzahlungen, Amortisationen von Verbindlichkeiten, Amortisationen von Nutzungsrechten am Leasingobjekt und Aufwendungen für Nebenkosten beim Leasing umfassen. Sie können die Stapelverarbeitung auch verwenden, um die erstmalige Erfassung mehrerer Mietverträge gleichzeitig durchzuführen oder Übergangsanpassungen für mehrere Mietverträge gleichzeitig zu erstellen.

Um einen Batch-Auftrag einzurichten oder Zahlungsrechnungen, Abschreibungen oder Zinsen für mehrere Mietverträge zu verarbeiten, gehen Sie zu **Anlagenleasing \> Periodisch \> Batch-Erfassungserstellung**. Im daraufhin angezeigten Dialogfeld können Sie den Zeitplan auswählen, nach dem die Journaleinträge erstellt werden sollen. Sie können auch angeben, ob der Stapelverarbeitungsvorgang für bestimmte Entitäten, Mietvertragsgruppen oder Leasingbücher ausgeführt werden soll.

> [!NOTE]
> Nachfolgende Transaktionen, wie z. B. Tilgungspläne für Verbindlichkeiten, Zahlungen, Abschreibungen und Aufwendungen, werden erst gebucht, nachdem die erstmalige Erfassung für entsprechende Mietverträge gebucht wurde.
>
> Die Journaleinträge werden erstellt, aber erst gebucht, wenn Sie den **Ausführen**-Befehl auswählen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]