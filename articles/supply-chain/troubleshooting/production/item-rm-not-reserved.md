---
title: Artikel-RM kann nicht reserviert werden, wenn ein Produktionsauftrag freigegeben wird.
description: 'Beim Freigeben eines Produktionsauftrags erhalten Sie möglicherweise die folgende Fehlermeldung: „Artikel-RM konnte nicht vollständig reserviert werden.“ Stellen Sie sicher, dass die volle Menge verfügbar ist, oder reservieren Sie Artikel manuell.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476471"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Artikel-RM kann nicht vollständig reserviert werden, wenn ein Produktionsauftrag freigegeben wird.

## <a name="symptoms"></a>Symptome

Wenn bei der Freigabe eines Produktionsauftrags an einen Lagerort nicht alle Elemente der Stückliste physisch verfügbar sind und die Richtlinie **Freigeben an Lagerort** auf *Vollständige Reservierung erforderlich* festgelegt ist, erhalten Sie die folgende Fehlermeldung:

> Element RM konnte nicht vollständig reserviert werden. Stellen Sie sicher, dass die volle Menge verfügbar ist, oder reservieren Sie die Elemente manuell, wenn das Feld Reservierung in der Stückliste-Zeile auf Manuell oder Gestartet festgelegt ist. Der Auftrag konnte nicht für den Lagerort freigegeben werden, weil einige Materialien nicht reserviert werden konnten.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist gewollt und funktioniert wie erwartet. Um dieses Problem zu beheben, folgen Sie den Anweisungen in der Fehlermeldung: „Stellen Sie sicher, dass die volle Menge verfügbar ist, oder reservieren Sie die Artikel manuell, wenn das Feld „Reservierung“ in der Stücklistenzeile auf „Manuell“ oder „Gestartet“ festgelegt ist.“
