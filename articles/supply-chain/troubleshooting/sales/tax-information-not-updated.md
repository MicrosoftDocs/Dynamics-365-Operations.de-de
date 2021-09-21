---
title: Steuerinformationen werden nicht aktualisiert, wenn der Standort in einem Auftrag geändert wird
description: Wenn der Standort, das Lager oder die Lieferadresse entweder in einem Auftragskopf oder auf Positionsebene geändert wird, werden die Fallsteuerinformationen für die Positionen nicht automatisch aktualisiert. Sie müssen dies manuell tun.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476448"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>Steuerinformationen werden nicht aktualisiert, wenn der Standort in einem Auftragskopf geändert wird.

## <a name="symptoms"></a>Symptome

Wenn der Standort, das Lager oder die Lieferadresse entweder in einem Auftragskopf oder auf Positionsebene geändert wird, werden die Fallsteuerinformationen für die Positionen nicht automatisch aktualisiert.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Das Problem tritt auf, weil die Lieferadresse, der Standort und das Lager nicht auch automatisch auf Positionsebene geändert werden. Sie müssen sie manuell aktualisieren.
