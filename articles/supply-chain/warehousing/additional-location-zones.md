---
title: Zusätzliche Lagerplatzzonen
description: Dieser Artikel enthält eine Übersicht über die neuen Lagerplatzzonen, die Microsoft Dynamics 365 Supply Chain Management hinzugefügt wurden.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336514"
---
# <a name="additional-location-zones"></a>Zusätzliche Lagerplatzzonen

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management sind drei neue Zonenfelder verfügbar. Die Lagerortverwaltung kann damit zusätzliche Lagerortorganisationen oder -layouts definieren. Die neuen Zonenfelder können entweder manuell oder mithilfe des **Lagerplatz-Setup-Assistenten** festgelegt werden. Sie können in jeder Abfrage oder Filterung verwendet werden, die die Tabelle „Lagerplätze“ verwendet.

Für die Verwendung der Zonenfelder sind keine zusätzlichen Einstellungen erforderlich.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Funktion „Zusätzliche Lagerplatzzone“ ein -oder ausschalten

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.25 ist die Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.29 ist die Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.29 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Zusätzliche Lagerplatzzone* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="use-location-zones"></a>Verwenden von Lagerplatzzonen

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatz-Setup-Assistent**.
2. Legen Sie die folgenden Werte fest:

    - Im Feld **Lagerort** wählen Sie _62_ aus.
    - Im Feld **Zonen-ID** wählen Sie _FLOOR_ aus.
    - Im Feld **Zusätzliche Zone 1** wählen Sie _PICKZONE1_ aus.
    - Im Feld **Zusätzliche Zone 2** wählen Sie _WEBSHOP1_ aus.
    - Im Feld **Lagerplatzprofilkennung** wählen Sie _FLOOR_ aus.

3. Wählen Sie die Zeile **Stockwert** aus.
4. Geben Sie im Feld **Von-Nummer** den Wert _1_ ein. Geben Sie im Feld **An-Nummer** den Wert _3_ ein.
5. Wählen Sie die Zeile **Gang** aus.
6. Geben Sie im Feld **Von-Nummer** den Wert _1_ ein. Geben Sie im Feld **An-Nummer** den Wert _5_ ein.
7. Wählen Sie **Erstellen** aus.
8. Sie erhalten Nachrichten, dass neue Lagerplätze hinzugefügt wurden. Wählen Sie die Schaltfläche **Nachrichten anzeigen** aus, um die Nachrichten anzuzeigen.
9. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplätze**. Die neuen Lagerplätze werden in der Liste angezeigt und alle Zonenfelder sind verfügbar (d. h. das vorhandene Zonenfeld und die neuen zusätzlichen Zonenfelder).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]