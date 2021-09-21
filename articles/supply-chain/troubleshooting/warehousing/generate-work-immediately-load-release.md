---
title: Entnahmearbeiten sofort generieren, wenn die Ladung freigegeben wird
description: Wenn bei der Freigabe der Ladung sofort Arbeit erzeugt werden muss, müssen Sie die Wellenvorlage entsprechend konfigurieren. Diese Seite führt Sie durch die Schritte.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476462"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Entnahmearbeit wird nicht sofort generiert, wenn die ausgehende Ladung freigegeben wird.

## <a name="symptoms"></a>Symptome

Sie erstellen eine ausgehende Ladung mithilfe eines Kunden- oder Umlagerungsauftrags und geben die Ladung an den Lagerort frei. Sie bemerken jedoch, dass noch keine Entnahmearbeiten erzeugt wurden.

## <a name="resolution"></a>Lösung

Wenn bei der Freigabe der Ladung sofort Arbeit erzeugt werden muss, müssen Sie die Wellenvorlage entsprechend konfigurieren. Legen Sie in der Wellenvorlage die folgenden Optionen auf *Ja* fest:

- Wellenerstellung automatisieren
- Welle bei Freigabe für Lagerort verarbeiten
- Wellenfreigabe automatisieren
