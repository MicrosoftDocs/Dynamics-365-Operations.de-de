---
title: Arbeit bleibt blockiert
description: Arbeit bleibt blockiert
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924129"
---
# <a name="work-remains-blocked"></a>Arbeit bleibt blockiert

Fehlercode: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Arbeit %1 bleibt gesperrt, da der zugehörige Zyklus %2 den Status %3 hat.

## <a name="cause"></a>Ursache

Die Arbeit wird gerade auf einer Welle verarbeitet und kann nicht entsperrt werden, wie durch eine der folgenden Bedingungen angezeigt:

- Auf der Registerkarte **Sperrgründe** wird das Feld **Arbeitssperrgrund** für eine oder mehrere Zeilen auf *Verarbeitungswelle* festgelegt.
- Wenn Sie **Welle** in der Gruppe **Bezogene Informationen** auf der Registerkarte **Bezogene Informationen** des Aktivitätsbereichs auswählen, wird das Feld **Wellenstatus** auf *Verarbeitet* festgelegt.

## <a name="resolution"></a>Lösung

Wählen Sie im Aktivitätsbereich auf der Registerkarte **Zugehörige Informationen** in der Gruppe **Zugehörige Informationen** die Option **Welle**. Wählen Sie dann auf der Seite **Wellen** im Aktivitätsbereich, auf der Registerkarte **Welle** in der Gruppe **Welle** die Option **Wellendaten bereinigen**.

## <a name="workaround"></a>Problemumgehung

Wenn die vorangegangenen Schritte das Problem nicht behoben haben, können Sie die Arbeit abbrechen, indem Sie diese Schritte ausführen.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.
1. Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie stornieren möchten und die derzeit einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* hat.
1. Wählen Sie **OK**.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.

Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).
