---
title: Bewegung von Bestand mit zugeordneter Arbeit in der Lagerortverwaltung
description: Mit der Bewegung von Bestand können Sie festlegen, welche Lagerortverwalter reservierten Bestand bewegen dürfen.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d996886a90037f288e839c54c8c9d932cabb21f19f2aef1552ca82b192c96a51
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736550"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Bewegung von Bestand mit zugeordneter Arbeit in der Lagerortverwaltung

[!include [banner](../includes/banner.md)]

Mit der Bewegung von Bestand können Sie festlegen, welche Lagerortverwalter reservierten Bestand bewegen dürfen. Dies bietet Flexibilität an geregelten Lagerorten, wo Sie festlegen können, dass eine Arbeitskraft nicht berechtigt ist, einen neuen Entnahmeort zu wählen, um Arbeit zu entnehmen, die bereits erledigt wurde. Es ermöglicht auch einem Lageortleiter festzulegen, welche Funktionen weniger erfahrene Arbeitskräfte haben sollen.

Die Möglichkeit, die täglichen Arbeitsgänge von Lagerortarbeitskräften zu verwalten, kann in folgenden Szenarien hilfreich sein:

## <a name="scenario-1"></a>Szenario 1

Ein Unternehmen hat einen relativ kleinen Wareneingangsbereich, der mit Paletten und Kartons verstopft ist, die auf ihre Einlagerung warten. Eine große Lieferung wird für den aktuellen Tag erwartet. Deshalb entscheidet der zuständige Sachbearbeiter, den Wareneingang zu räumen, indem er einige Palletten in einen zweiten Eingangsbereich verschiebt.

## <a name="scenario-2"></a>Szenario 2

Ein erfahrener Lagerarbeiter hat die Möglichkeit, Artikel an einem Lagerort zusammenzufassen, anstatt diese auf drei Lagerplätze in der Nähe mit jeweils geringen Mengen zu verteilen. Die Arbeitskraft möchte die Menge konsolidieren, indem Artikel von den einzelnen Lagerplätzen zu einem Lagerplatz auf demselben Ladungsträger verschoben werden.

## <a name="scenario-3"></a>Szenario 3

Eine Palette in einem Staginglagerplatz wie STAGE01, der sich in der Nähe von BAYDOOR01 befindet, soll ausgeliefert werden. Aufgrund einer Planungsänderung soll der LKW allerdings bei BAYDOOR04 eintreffen. Der Sachbearbeiter ist darüber informiert und muss sicherstellen, dass der LKW nicht bei STAGE01 auf die Ladung warten muss. Er beschließt, die Artikel der Lieferung von STAGE01 nach STAGE04 zu verschieben, da dieser näher am Ziel ist.

### <a name="current-limitations"></a>Aktuelle Einschränkungen

Die Arbeitsreservierungen, die Sie verschieben können, sind begrenzt auf Aufträge, Umlagerungsauftragsprobleme, Umlagerungsauftragszugang, Bestellungen und Wiederbeschaffungsarbeit.

Das Verschieben von Artikel ist eingeschränkt, um das Aufteilen von Arbeitspositionen zu verhindern. Das bedeutet, wenn Sie eine Arbeitsposition für 100 Stück von Artikel A am Lagerplatz Loc1 haben, können Sie nicht nur 30 Stück von Artikel A zu einem anderen Lagerplatz verschieben. Dies würde zu einer Teilung der vorhandenen Arbeitsposition in je 30 und 70 Stück führen, da die Lagerplätze unterschiedlich sind.

Bei Staging-Szenarien, bei denen der Ladungsträger, von dem Sie die Waren verschieben oder bei denen der Ladungsträger, zu dem Sie die Waren verschieben als Zielladungsträger für eine Arbeitsauftrag eingerichtet sind, sind nur Verschiebungen des ganzen Ladungsträgers zulässig, damit der Zielladungsträger nicht geteilt wird.

Nur die Ad-hoc-Bewegung wird derzeit unterstützt. Das bedeutet, dass Sie nicht in der Lage sind, reservierten Bestand durch eine Bewegung über das Vorlagenmenü des Mobilgeräts zu verschieben.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Einrichten von Berechtigungen zum Bewegen von Bestand für einzelne Arbeitskräfte

Für die Arbeitskraft, die autorisiert werden soll, Bestand zu verschieben, aktivieren Sie das Kontrollkästchen **Bewegung von Bestand mit zugeordneter Arbeit zulassen** unter **Lagerortverwaltung \> Einstellungen \> Arbeitskraft**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
