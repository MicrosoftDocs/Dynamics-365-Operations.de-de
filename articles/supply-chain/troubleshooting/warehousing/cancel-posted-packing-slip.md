---
title: Lieferschein kann nicht storniert werden, nachdem er aus einem Auftrag gebucht wurde
description: Wenn Kommissionier- und Versandprozesse für WMS aktiviert sind, können Sie einen Lieferscheins nicht stornieren, nachdem er aus einem Verkaufsauftrag gebucht wurde. Diese Seite zeigt eine Problemumgehung.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476497"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Sie können einen Lieferschein nicht stornieren, nachdem er aus einem Auftrag gebucht wurde.

## <a name="symptoms"></a>Symptome

Wenn Kommissionier- und Versandprozesse für die erweiterte Lagerortverwaltung (WMS) aktiviert sind, können Sie einen Lieferschein nicht stornieren, nachdem er aus einem Auftrag gebucht wurde.

## <a name="resolution"></a>Lösung

Um gebuchte Lieferscheine für Artikel, die für WMS aktiviert sind, zu korrigieren, muss die Buchung aus der Ladung erfolgen, nicht aus dem Auftrag. Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt.  

Im Allgemeinen kann der Lieferschein eines Auftrags, der durch Lagerortverwaltungsprozesse kommissioniert und versandt wurde, über die Ladung oder den Versand sowie über den Auftragsbeleg selbst aktualisiert werden. Wenn Sie den Lieferschein eines Auftrag jedoch über den Auftragsbeleg aktualisieren, kann die Stornierung des Lieferscheins immer noch nicht über die Ladung oder den Auftrag erfolgen. Daher empfehlen wir Ihnen, die Lieferscheinbuchung aus der Ladung heraus zu verwenden. In diesem Fall wird die Stornierung, die von der Ladung aus erfolgen muss, aktiviert.
