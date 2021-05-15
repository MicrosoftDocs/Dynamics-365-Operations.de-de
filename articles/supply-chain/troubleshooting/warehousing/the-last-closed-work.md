---
title: Die letzte geschlossene Arbeitszeile muss ein PUT sein
description: Die letzte geschlossene Arbeitszeile muss ein PUT sein
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
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924374"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Die letzte geschlossene Arbeitszeile muss ein PUT sein

Fehlercode: WAX1285

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Die letzte geschlossene Arbeitszeile muss ein PUT sein.

## <a name="cause"></a>Ursache

Die Arbeit kann in ihrem aktuellen Status nicht storniert werden.

In der letzten Arbeitszeile ist das Feld **Arbeitsstatus** auf *Geschlossen* festgelegt, aber das Feld **Arbeitstyp** ist nicht auf *Put* festgelegt.

## <a name="resolution"></a>Lösung

Um die Arbeit abzubrechen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.
1. Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen.
1. Wählen Sie **OK**.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.

Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).
