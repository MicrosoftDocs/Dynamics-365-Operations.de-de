---
title: Die Melden-als-beendet-Aktualisierung schlägt mit einem Fehler bezüglich fehlender Menge fehl
description: Wenn Sie versuchen einen Produktionsauftrag zu beenden, wenn Sie die Fehlermenge melden, aber nicht die Zeit- oder Materialmenge, dir die Aktualisierung „Als beendet melden“ fehlschlagen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476415"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>Die Aktualisierung des Berichts als abgeschlossen schlägt mit einem Fehler bezüglich fehlender Menge fehl

## <a name="symptoms"></a>Symptome

Sie versuchen einen Produktionsauftrag als beendet zu melden, während Sie die Fehlermenge melden, aber nicht, während Sie die Zeit- oder Materialmenge melden. Wenn Sie versuchen, den Produktionsauftrag zu beenden, schlägt die Bericht-als-erledigt-Aktualisierung fehl, und Sie erhalten die folgende Fehlermeldung:

> Fertigmeldungsmenge fehlt.

## <a name="resolution"></a>Lösung

Wenn Sie die Fehlermenge eines Produktionsauftrags melden, müssen Sie auch die Warenmenge melden.
