---
title: Verbesserungen an der Leistung der Verkaufshistorienbereinigung
description: In diesem Thema wird die Funktion für Verbesserungen an der Leistung der Verkaufshistorienbereinigung und ihre Aktivierung beschrieben.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d4eeee3c1228b278fea07464f35946c295c5aea8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679054"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Verbesserungen an der Leistung der Verkaufshistorienbereinigung

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!-- GA with 10.0.24 -->

Der regelmäßige Batchauftrag **Aktualisierungshistorie für Verkauf bereinigen** kann lange dauern, wenn er in Umgebungen mit einem hohen Volumen an Verkaufsaktualisierungen nur selten ausgeführt wird. In diesen Situationen kann die Funktion *Verbesserungen an der Leistung der Verkaufshistorienbereinigung* dazu beitragen, die Laufzeit zu verkürzen und die Zuverlässigkeit zu verbessern.

Die Funktion verbessert den vorhandenen Bereinigungsauftrag auf folgende Weise:

- Sie teilt die Bereinigung in Stapel auf (Sie können die Stapelgröße durch Anpassungen ändern).
- Es läuft maximal 2 Stunden (Sie können die Dauer durch Anpassungen ändern).
- Wenn möglich werden Datenbankfunktionen genutzt, um Sperrkonflikte zu minimieren und das Verbinden von Transaktionstabellen während der Bereinigung zu vermeiden.

Nachdem Sie die Funktion aktiviert haben, wird der Batchauftrag **Aktualisierungshistorie für Verkauf bereinigen** (**Vertrieb und Marketing \> Periodische Aufgaben \> Bereinigung \> Aktualisierungshistorie für Verkauf bereinigen**) wie zuvor ausgeführt, jedoch mit besserer Leistung und für maximal 2 Stunden. Dies bedeutet, dass er möglicherweise mehrmals ausgeführt werden muss, um alle Daten für einen bestimmten Aufbewahrungszeitraum zu bereinigen.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Funktion für Verbesserungen an der Leistung der Verkaufshistorienbereinigung aktivieren

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Vertrieb und Marketing*
- **Funktionsname:** *Verbesserungen an der Leistung der Verkaufshistorienbereinigung*
