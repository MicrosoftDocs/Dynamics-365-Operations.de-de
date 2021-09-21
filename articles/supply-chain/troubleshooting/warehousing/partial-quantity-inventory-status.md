---
title: Bestandsstatusänderung für Teilmengenarbeiten machen
description: Auf dieser Seite wird erläutert, wie Sie einen Menüeintrag mit den entsprechenden Einstellungen erstellen, damit Mitarbeiter eine Bestandsstatusänderung für eine Teilmenge einer Charge vornehmen können.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476394"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>Bestandsstatusänderung für Teilmengenarbeiten aktivieren

## <a name="symptoms"></a>Symptome

Sie müssen eine Bestandsstatusänderung für eine Teilmenge einer Charge durchführen.

## <a name="resolution"></a>Lösung

Um den Arbeitskräften diese Änderung zu ermöglichen, können Sie einen Menüpunkt für die Warehouse Management Mobile App erstellen. Erstellen (oder bearbeiten) Sie auf der Seite **Mobilgeräte-Menüpunkte** einen Menüpunkt, der die folgenden Einstellungen hat:

- **Modus:** *Arbeit*
- **Vorhandene Arbeit verwenden:** *Nein*
- **Arbeitserstellungsprozess:** *Bewegung*
- **Status des Bestands anzeigen:** *Ja*

Sie können weitere Felder auf der Seite nach Bedarf festlegen.
