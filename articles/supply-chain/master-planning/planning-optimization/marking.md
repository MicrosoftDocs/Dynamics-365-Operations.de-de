---
title: Bestandskennzeichnung mit Planungsoptimierung
description: Dieses Thema enthält Informationen über die Optionen, die für die Markierung von Beständen in umgewandelten Aufträgen zur Verfügung stehen, wenn Sie die Planungsoptimierung verwenden.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99a52c03e519384955d68d7101a7b73b7e9a7af6
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672187"
---
# <a name="inventory-marking-with-planning-optimization"></a>Bestandskennzeichnung mit Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Informationen über die Optionen, die für die Markierung von Beständen in umgewandelten Aufträgen zur Verfügung stehen, wenn Sie die Planungsoptimierung verwenden.

*Markierung* wird verwendet, um Angebot und Nachfrage zu verknüpfen. Sie ähnelt dem *Bedarfsverursacher*, der angibt, wie die Produktprogrammplanung die Nachfrage zu decken gedenkt. Aus Sicht der Planung besteht der Hauptunterschied darin, dass die Markierung dauerhafter ist als der Bedarfsverursacher.

Die Markierung wurde eingeführt, um spezielle Kalkulationsszenarien für First In, First Out (FIFO) und Last In, First Out (LIFO) zu unterstützen. Sie wird jetzt aber auch für einige Nicht-Kalkulationsszenarien verwendet. Die Markierung zwischen Angebot und Nachfrage ist optional und fast permanent. Die Markierung kann manuell von einem Benutzer entfernt werden, oder sie kann durch die Ausführung einer Verkaufsauftragszeilenauflösung entfernt werden, bei der die Option **Markierung entfernen** ausgewählt ist.

Die Bedarfsverursacher werden von der Produktprogrammplanung während der Deckung gesteuert, um die Nachfrage mit dem benötigten Angebot zu verknüpfen. Die Bedarfsverursacher können für jeden Planungslauf aktualisiert werden, um das Angebot zu optimieren, das zur Deckung der Nachfrage erforderlich ist. Wenn die Produktprogrammplanung Bedarfsverursacher-Informationen aktualisiert, berücksichtigt sie alle vorhandenen Markierungen.

Der Bedarfsverursacher beginnt mit der Einbeziehung relevanter Markierungen, Bestandsreservierungen und Bestellreservierungen in der folgenden Sequenz:

1. Markierung zwischen Bedarf und Angebot
1. Bestandsreservierungen
1. Reservierungen auf Bestellung

Wenn Sie einen Planauftrag umwandeln, bietet die Dialogbox **Umwandlung** ein Feld **Bestandsmarkierung aktualisieren**, mit dem Sie Markierungsoptionen für die Aufträge festlegen können, die während der Umwandlung erstellt werden. Wählen Sie einen der folgenden Werte aus:

- **Nein** - Es wird keine Bestandsmarkierung angewendet.
- **Standard** - Die Bestandsmarkierung wird entsprechend dem Bedarfsverursacher aktualisiert. Ein Bedarfsauftrag (Nachfrage) wird gegen einen Erfüllungsauftrag (Lieferung) markiert. Wenn eine bestimmte Menge auf dem Erfüllungsauftrag verbleibt, wird sie nicht markiert und die Referenzinformationen bleiben leer. Wenn z. B. ein Verkaufsauftrag über 100 ea gegen eine Einkaufsbestellung über 150 ea verrechnet wird, werden die Referenzinformationen nur dem Verkaufsauftrag zugewiesen.
- **Erweitert** - Sowohl der Bedarfsauftrag (Nachfrage) als auch der Erfüllungsauftrag (Lieferung) werden markiert, unabhängig von der Menge, die auf dem Erfüllungsauftrag verbleibt. Wenn z. B. ein Verkaufsauftrag über 100 ea mit einer Einkaufsbestellung über 150 ea verrechnet wird, werden die Referenzinformationen sowohl dem Verkaufsauftrag als auch der Einkaufsbestellung zugewiesen.
