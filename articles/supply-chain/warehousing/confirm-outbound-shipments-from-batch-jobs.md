---
title: Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen
description: In diesem Thema wird beschrieben, wie Sie einen Stapelverarbeitungsauftrag einrichten, der ausgehende Transportauftragslieferungen für versandfertige Ladungen automatisch bestätigt.
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838441"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie einen Stapelverarbeitungsauftrag einrichten, der ausgehende Transportauftragslieferungen für versandfertige Ladungen automatisch bestätigt. Der hier beschriebene Stapelverarbeitungsauftrag gilt nur für Transportauftragssendungen, nicht für Aufträge.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Aktivieren Sie die Funktion Ausgehende Lieferungen bestätigen in der Funktion Stapelverarbeitungsaufträge

Bevor Sie diese Funktion nutzen können, müssen Sie diese auf Ihrem System aktivieren. Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren. Die Funktion ist aufgeführt als:

- **Modul** - *Lagerortverwaltung*
- **Funktionsname** - *Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen*

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