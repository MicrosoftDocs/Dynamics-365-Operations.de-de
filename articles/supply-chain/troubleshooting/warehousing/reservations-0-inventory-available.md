---
title: Kann keine Bestandreservierungen vornehmen, da 0,00 verfügbar sind
description: Sie erhalten eine Fehlermeldung, das System kann keine Reservierungen vornehmen, da nur 0,00 im Inventar verfügbar sind. Dieses Problem wird wahrscheinlich durch offene Arbeit verursacht.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476475"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Das System kann keine Reservierungen vornehmen, da 0,00 im Inventar verfügbar sind

## <a name="symptoms"></a>Symptome

Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben. Möglicherweise erhalten Sie die folgende Fehlermeldung:

> Physischer Bestand Standort=%1, Lagerort=%2, Bestandsstatus=Verfügbar, Chargennummer=%3, Besitzer=%4: %5 kann nicht reserviert werden, da nur 0,00 im Bestand verfügbar sind.

## <a name="resolution"></a>Lösung

Dieses Problem wird wahrscheinlich durch offene Arbeit verursacht. Beenden Sie entweder die Arbeit oder empfangen Sie ohne Arbeitserstellung. Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren. Diese Vorgänge können z. B. offene Qualitätsaufträge, Bestandssperrungen oder Ausgabeaufträge sein.
