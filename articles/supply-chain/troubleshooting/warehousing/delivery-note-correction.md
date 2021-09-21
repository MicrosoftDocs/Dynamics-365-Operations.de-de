---
title: Lieferscheinkorrektur kann nicht bearbeitet werden
description: Wenn Sie versuchen, einen Lieferschein nach der Buchung zu korrigieren, erhalten Sie eine Fehlermeldung. Auf dieser Seite wird erläutert, wie Sie gebuchte Lieferscheine für Artikel korrigieren, die für WMS aktiviert sind.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476470"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Lieferscheinkorrektur kann nicht bearbeitet werden

## <a name="symptoms"></a>Symptome

Nachdem Sie einen Lieferschein gebucht haben, können Sie ihn nicht stornieren, da die Schaltfläche **Stornieren** nicht verfügbar ist. Sie können den Lieferschein auch nicht korrigieren. Wenn Sie es versuchen, erhalten Sie die folgende Fehlermeldung:

> Die Lieferscheinkorrektur kann nicht bearbeitet werden. Der Lieferschein enthält nur Artikel, die den Prozessen der Lagerortverwaltung unterliegen, da diese von der Lieferscheinkorrektur nicht unterstützt werden.

## <a name="resolution"></a>Lösung

Um gebuchte Lieferscheine für Elemente zu korrigieren, die für die erweiterte Lagerortverwaltung (WMS) aktiviert sind, müssen Sie die Buchung aus der Ladung heraus vornehmen, nicht direkt aus dem Auftrag.
