---
title: Lagerplatz der Dimension darf nicht leer sein, wenn die Seriennummer festgelegt ist
description: Wenn dieser Fehler beim Bestätigen einer Lieferung nach dem Erstellen eines Umlagerungsauftrags für einen Serienartikel angezeigt wird, ist das Feld „Standard-Zugangslagerplatz“ leer.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476480"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Ein Fehler ist beim Bestätigen der Lieferung nach dem Anlegen eines Umlagerungsauftrags für einen Serienartikel aufgetreten.

## <a name="symptoms"></a>Symptome

Wenn Sie einen Umlagerungsauftrag für einen Serienartikel erstellen und dabei einen Lagerort verwenden, der für die erweiterte Lagerortverwaltung (WMS) aktiviert ist, und dann, nachdem die Arbeit abgeschlossen ist, versuchen, die Lieferung zu bestätigen, wird die folgende Fehlermeldung angezeigt:

> Der Lagerplatz der Dimension darf nicht leer sein, wenn die Seriennummer der Dimension festgelegt ist.

## <a name="cause"></a>Ursache

Der Grund hierfür ist, dass das Feld **Standard-Eingangsort** für ein Transitlager des „von“-Lagerorts leer ist.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, geben Sie einen Standard-Empfangsort im Transitlager an. Stellen Sie sicher, dass dieser Lagerplatz über Kennzeichnungen gesteuert wird.
