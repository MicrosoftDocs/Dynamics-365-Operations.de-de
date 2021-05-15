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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924254"
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
