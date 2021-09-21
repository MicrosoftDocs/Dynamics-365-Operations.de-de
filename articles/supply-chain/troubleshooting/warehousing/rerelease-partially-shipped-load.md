---
title: Sie können eine teilweise ausgelieferte Ladung nicht erneut an das Lager freigeben
description: In früheren Versionen konnten Sie eine teilweise ausgelieferte Ladung nicht erneut freigeben, wenn Sie bestimmte Funktionen mit unvollständigen Reservierungen verwenden. Dieses Problem wurde behoben.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476461"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Sie können eine teilweise ausgelieferte Ladung nicht erneut an das Lagerort freigeben

## <a name="symptoms"></a>Symptome

Sie können eine teilweise ausgelieferte Ladung nicht an das Lagerort freigeben. Wenn Sie die Freigabe an den Lagerort durchführen, erscheint die Meldung „Vorgang abgeschlossen“, aber es passiert nichts, und es wird keine Arbeit für die verbleibende Menge erstellt. Dieses Problem tritt auf, wenn Sie die Transportladungsfunktionalität verwenden und es eine unvollständige Reservierung gibt.

## <a name="resolution"></a>Lösung

[KB-Problem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Teilweise versendete Ladungen können erneut versendet und verarbeitet werden“) ist in [Version 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15) behoben.
