---
title: Entnahmearbeiten wegen nicht abgeschlossener Wiederbeschaffungsarbeiten blockiert
description: Die Entnahmearbeiten können wegen abhängiger Wiederbeschaffungsarbeiten blockiert werden. Schließen Sie die Wiederbeschaffungsarbeiten ab und verarbeiten Sie dann die Entnahmearbeiten.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476490"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Die Blockade der Entnahmearbeiten kann wegen nicht abgeschlossener Wiederbeschaffungsarbeiten nicht aufgehoben werden.

## <a name="symptoms"></a>Symptome

Bei Verwendung der Wellenbedarfs-Wiederbeschaffung können Entnahmearbeiten wegen abhängiger Wiederbeschaffungsarbeiten blockiert werden. Wenn für einen Lagerplatz eine Wiederbeschaffung erforderlich ist, um den Bedarf des Quellauftrags zu erfüllen, erstellt das System sowohl die Wiederbeschaffungsarbeiten als auch die Entnahmearbeiten. Die Entnahmearbeiten werden jedoch blockiert, bis die Wiederbeschaffungsarbeiten abgeschlossen sind und Sie die folgende Fehlermeldung erhalten:

> Die Sperrung der Arbeit %1 kann nicht aufgehoben werden, da nicht abgeschlossene Wiederbeschaffungsarbeit vorliegt.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt, da der Entnahmeort nicht über genug Bestand verfügt, solange die Wiederbeschaffungsarbeiten nicht abgeschlossen sind. Schließen Sie die Wiederbeschaffungsarbeiten ab und verarbeiten Sie dann die Entnahmearbeiten.
