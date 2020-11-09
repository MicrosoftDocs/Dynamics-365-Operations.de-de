---
title: Zusätzliche Lagerplatzzonen
description: Dieses Thema enthält eine Übersicht über die neuen Lagerplatzzonen, die Microsoft Dynamics 365 Supply Chain Management hinzugefügt wurden.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016307"
---
# <a name="additional-location-zones"></a>Zusätzliche Lagerplatzzonen

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management sind drei neue Zonenfelder verfügbar. Die Lagerortverwaltung kann damit zusätzliche Lagerortorganisationen oder -layouts definieren. Die neuen Zonenfelder können entweder manuell oder mithilfe des **Lagerplatz-Setup-Assistenten** festgelegt werden. Sie können in jeder Abfrage oder Filterung verwendet werden, die die Tabelle „Lagerplätze“ verwendet.

Für die Verwendung der Zonenfelder sind keine zusätzlichen Einstellungen erforderlich.

## <a name="turn-on-the-additional-location-zone-feature"></a>Aktivieren der Funktion „Zusätzliche Lagerplatzzone“

Bevor Sie die Funktion *Zusätzliche Lagerplatzzone* verwenden können, muss sie in Ihrem System aktiviert sein. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Zusätzliche Lagerplatzzone*

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
