---
title: Ausgehende Lieferungen aus Batchaufträgen bestätigen
description: In diesem Artikel wird beschrieben, wie Sie einen Stapelverarbeitungsauftrag einrichten, der ausgehende Transportauftragslieferungen für versandfertige Ladungen automatisch bestätigt.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875100"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Ausgehende Lieferungen aus Batchaufträgen bestätigen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie einen Stapelverarbeitungsauftrag einrichten, der ausgehende Transportauftragslieferungen für versandfertige Ladungen automatisch bestätigt. Der hier beschriebene Stapelverarbeitungsauftrag gilt nur für Transportauftragssendungen, nicht für Aufträge.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Die Funktion „Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen“ ein- oder ausschalten

Um die Funktionalität zu verwenden, die in diesem Artikel beschrieben wird, die Funktion *Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen* für Ihr System eingeschaltet werden. Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.25 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="process-outbound-shipments"></a>Ausgehende Lieferungen verarbeiten

Um einen geplanten Stapelverarbeitungsauftrag einzurichten, um die Bestätigung für eine ausgehende Lieferung für versandfertige Ladungen auszuführen:

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Ausgehende Sendungen verarbeiten**.
1. Das Dialogfeld **Lieferung bestätigen** wird geöffnet. Wählen Sie auf der Seite **Einschließende Datensätze** Inforegister die Option **Filter**.
1. Das Abfrage-Editor-Dialogfeld öffnet sich. Fügen Sie in der Registerkarte **Bereich** eine Zeile mit den folgenden Werten hinzu:
    - **Tabelle** - *Ladungen*
    - **Abgeleitete Tabelle** - *Ladungen*
    - **Feld** - *Ladungsstatus*
    - **Kriterien** - *Geladen*
1. Wählen Sie **OK**, um zum Dialogfeld **Lieferung bestätigen** zurückzukehren.
1. Im Inforegister **Im Hintergrund ausführen** setzen Sie **Stapelverarbeitung** auf **Ja**.
1. Wählen Sie im Inforegister **Im Hintergrund ausführen** **Serie**.
1. Das Dialogfeld **Serie festlegen** öffnet sich. Legen Sie den passenden Zeitplan für Ihr Unternehmen fest.
1. Wählen Sie **OK**, um zum Dialogfeld **Lieferung bestätigen** zurückzukehren.
1. Wählen Sie **OK** im Dialogfeld **Lieferung bestätigen**, um den Stapelverarbeitungsauftrag der Wartestelle hinzuzufügen.

Weitere Informationen finden Sie unter [Stapelverarbeitung – Übersicht](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]