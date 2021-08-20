---
title: Arbeit kann nicht storniert werden, weil sie gesperrt ist
description: Arbeit kann nicht storniert werden, weil sie gesperrt ist
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755977"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Arbeit kann nicht storniert werden, weil sie gesperrt ist

Fehlercode: WAX2190

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Die Arbeit "%1" kann nicht storniert werden, weil sie den Status "%2" aufweist.

## <a name="cause"></a>Ursache

Die Arbeit kann in ihrem aktuellen Status nicht storniert werden.

Der Work-Kopf oder die Work-Zeilen haben nicht den erwarteten **Work-Status**-Wert. Das Feld **Arbeitsstatus** im Arbeitskopf ist nicht auf *Offen* oder *In Bearbeitung* festgelegt.

## <a name="resolution"></a>Lösung

Um die Arbeit abzubrechen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.
1. Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen.
1. Wählen Sie **OK**.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.

Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).
