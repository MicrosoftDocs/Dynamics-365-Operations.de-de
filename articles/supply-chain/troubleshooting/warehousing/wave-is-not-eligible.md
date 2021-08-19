---
title: Welle ist nicht für Bereinigung geeignet
description: Welle ist nicht für Bereinigung geeignet
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778505"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Welle ist nicht für Bereinigung geeignet

Fehlercode: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Serie %1 ist nicht für Bereinigung berechtigt.

Die Wellendaten können nicht bereinigt werden.  

## <a name="cause"></a>Ursache

Die Welle wird gerade verarbeitet, was durch eine der folgenden Bedingungen angezeigt wird:

- Das Feld **Wellenstatus** ist auf *Ausgeführt* festgelegt.
- Wenn Sie **Batchauftrag** in der Gruppe **Welle** auf der Registerkarte **Welle** des Aktivitätsbereichs wählen, ist das Feld **Status** nicht auf *Beendet*, *Fehler* oder *Abgebrochen* festgelegt. Daher wird gerade ein Batchauftrag ausgeführt.

## <a name="resolution"></a>Lösung

Wählen Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Welle** die Option **Batchauftrag**, und führen Sie dann einen der folgenden Schritte aus:

- Wenn das Feld **Status** auf *Ausgeführt* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** in der Gruppe **Batchauftrag** die Option **Ansicht Aufgaben**. Sie können den Fortschritt verfolgen, indem Sie die Seite **Batch-Aufgaben** aktualisieren.
- Wenn das Feld **Status** nicht auf *Ausführend* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** in der Gruppe **Funktionen** die Option **Status ändern**. Wählen Sie im Feld **Neuen Status wählen** die Option *Warten*. Wählen Sie dann **OK** aus.
