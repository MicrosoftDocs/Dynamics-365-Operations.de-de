---
title: Zusätzliche Lagerplatzzonen
description: Dieses Thema enthält eine Übersicht über die neuen Lagerplatzzonen, die Microsoft Dynamics 365 Supply Chain Management hinzugefügt wurden.
author: Mirzaab
ms.date: 07/01/2020
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
ms.openlocfilehash: dd9e97cabe5e3d3bdc261a7280930b73eb8e1419
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103837"
---
# <a name="additional-location-zones"></a>Zusätzliche Lagerplatzzonen

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management sind drei neue Zonenfelder verfügbar. Die Lagerortverwaltung kann damit zusätzliche Lagerortorganisationen oder -layouts definieren. Die neuen Zonenfelder können entweder manuell oder mithilfe des **Lagerplatz-Setup-Assistenten** festgelegt werden. Sie können in jeder Abfrage oder Filterung verwendet werden, die die Tabelle „Lagerplätze“ verwendet.

Für die Verwendung der Zonenfelder sind keine zusätzlichen Einstellungen erforderlich.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Funktion „Zusätzliche Lagerplatzzone“ ein -oder ausschalten

Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Administratoren können diese Funktionalität an- oder ausschalten, indem Sie nach der Funktion *Zusätzliche Lagerplatzzone* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

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