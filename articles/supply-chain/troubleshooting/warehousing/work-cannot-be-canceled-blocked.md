---
title: Arbeit kann nicht storniert werden, weil sie blockiert ist
description: Arbeit kann nicht storniert werden, weil sie blockiert ist
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722198"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Arbeit kann nicht storniert werden, weil sie blockiert ist

Fehlercode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Arbeit %1 kann nicht abgebrochen werden, weil sie durch Grundtyp %2 blockiert ist. Die Arbeit muss entsperrt werden, bevor sie storniert werden kann.

## <a name="cause"></a>Ursache

Die Arbeit ist blockiert und kann nicht abgebrochen werden.

Auf der Seite **Arbeit**, auf der Registerkarte **Allgemein**, ist die Option **Sperrung** auf *Ja* festgelegt. Diese Einstellung gibt an, dass die Arbeit blockiert ist. Die Registerkarte **Sperrgründe** zeigt an, warum die Arbeit gesperrt wurde.

## <a name="resolution"></a>Lösung

Um die Sperrung des Werks aufzuheben, wählen Sie die Registerkarte **Sperrgründe** und führen dann einen der folgenden Schritte aus:

- Wenn das Feld **Arbeitssperrungsgrund** auf *Undefinierter Grund* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Arbeitssperre aufheben**.
- Wenn das Feld **Arbeitssperrungsgrund** auf *Verarbeitungswelle* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Zugehörige Informationen** in der Gruppe **Zugehörige Informationen** die Option **Welle**. Wählen Sie dann auf der Seite **Wellen** im Aktivitätsbereich, auf der Registerkarte **Welle** in der Gruppe **Welle** die Option **Wellendaten bereinigen**.

## <a name="workaround"></a>Problemumgehung

Wenn die vorangegangenen Schritte das Problem nicht behoben haben, können Sie die Arbeit abbrechen, indem Sie diese Schritte ausführen.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.
1. Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie stornieren möchten und die derzeit einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* hat.
1. Wählen Sie **OK**.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.

Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).
