---
title: Für diesen Lagerplatz muss eine Kennzeichnung angegeben werden.
description: Wenn dieser Fehler nach dem Erstellen eines Umlagerungsauftrags für einen WMS-fähigen Lagerort angezeigt wird, ist das Feld für ein Transitlager leer.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476411"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Ein Fehler ist bei der Kennzeichenspezifikation während der Versandbestätigung für einen Transportauftrag aufgetreten.

## <a name="symptoms"></a>Symptome

Wenn Sie einen Umlagerungsauftrag unter Verwendung eines Lagerorts erstellen, der für die erweiterte Lagerortverwaltung (WMS) aktiviert ist, und dann nach Abschluss der Arbeit versuchen, die Lieferung zu bestätigen, erhalten Sie möglicherweise die folgende Fehlermeldung:

> Für diesen Lagerplatz muss ein Ladungsträger angegeben werden.

## <a name="cause"></a>Ursache

Der Grund hierfür ist, dass das Feld **Standard-Eingangsort** für ein Transitlager des „von“-Lagerorts leer ist.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, geben Sie einen Standard-Empfangsort im Transitlager an. Stellen Sie sicher, dass dieser Lagerplatz über Kennzeichnungen gesteuert wird.
