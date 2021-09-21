---
title: Warehouse Management Prozesse werden derzeit verwendet
description: Beim Reservieren oder Freigeben von Arbeit erhalten Sie möglicherweise eine Meldung, dass derzeit Lagerverwaltungsprozesse verwendet werden. Beheben Sie das Problem mit einem dieser Schritte.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476396"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Arbeit kann nicht reserviert oder freigegeben werden, da derzeit Prozesse verwendet werden

## <a name="symptoms"></a>Symptome

Beim Arbeiten mit diskreter Fertigung erhalten Sie die folgende Fehlermeldung:

> Warehouse Management Prozesse werden derzeit verwendet. Wenn Arbeitszeilen noch nicht registriert sind, können Sie die erstellte Arbeit und alle Lade- oder Versandzeilen stornieren und dann mit dem Kommissionier- oder Versandprozess fortfahren.

## <a name="cause"></a>Ursache

Dieses Problem tritt auf, wenn Sie versuchen, Arbeit für eine Zeile zu reservieren oder freizugeben, aber die Bestandstransaktion den Status *Entnommen* hat, was bedeutet, dass das Material entnommen wurde.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, führen Sie einen der folgenden Schritte aus.

- Ändern Sie den Status des Produktionsauftrags zurück auf *Geschätzt* oder *Freigegeben*.
- Öffnen Sie die Detailseite für den betreffenden Produktionsauftrag. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Anhalten** die Option **Anhalten und Entnehmen**, um alle entnommenen Transaktionen zu entnehmen. Wählen Sie dann **Stopp entfernen**, um den Produktionsauftrag zu bearbeiten.

Hier eine Erklärung der Funktionen *Auspicken* und *Stopp*:
  
- **Entnehmen** - Diese Funktion kehrt den Status von Bestandstransaktionen für Stücklisten- und Formelzeilen um, die einen Status von *Kommissioniert* bis *Auf Bestellung* haben. Wenn die Arbeit für die Rohmaterialkommissionierung abgeschlossen ist, wird der Status der Zeilen auf *Kommissioniert* festgelegt. Dieser Status verhindert, dass der Produktionsauftrag auf den Status *Erstellt* zurückgesetzt wird. In diesem Fall können Sie die Funktion *Entnahme rückgängig machen* verwenden, um die Vorgänge aus dem Status *Entnahme rückgängig machen* zurückzusetzen und dann den Produktionsauftrag auf den Status *Created* zurückzusetzen.
- **Anhalten** - Diese Funktion legt ein **Angehalten** Flag für den Produktionsauftrag fest, um jede Statusaktualisierung des Auftrags zu verhindern. Sie finden das Flag **Angehalten** auf dem Inforegister **Lagerort** der Detailseite des Produktionsauftrags.

> [!NOTE]
>
> - Die Schaltflächen sind nur sichtbar, wenn der Produktionsauftrag für Elemente erstellt wird, die für Lagerprozesse aktiviert sind.
> - Die Gruppe **Anhalten** ist nur auf der Registerkarte **Lagerort** im Aktivitätsbereich der Seite mit den Produktionsauftragsdetails sichtbar. Sie ist auf dem Inforegister **Lagerort** der Listenseite **Produktionsaufträge** nicht sichtbar.
