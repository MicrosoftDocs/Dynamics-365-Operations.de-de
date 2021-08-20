---
title: Sie können keine Arbeit stornieren, die auf einem Benutzer liegt
description: Sie können keine Arbeit stornieren, die auf einem Benutzer liegt
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748690"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Sie können keine Arbeit stornieren, die auf einem Benutzer liegt

Fehlercode: WAX708

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Sie können keine Arbeit stornieren, die einem Benutzer zugeordnet ist.

## <a name="cause"></a>Ursache

Die Arbeit ist von einem Benutzer gesperrt und kann nicht abgebrochen werden. Um dies zu bestätigen, öffnen Sie die Arbeits-ID und dann die Registerkarte **Allgemein**. Wenn die Arbeit gesperrt ist, wird das Feld **Arbeitsstatus** auf *In Bearbeitung* festgelegt und das Feld **Gesperrt durch** auf eine Benutzer-ID.

## <a name="resolution"></a>Lösung

Um die Arbeit abzubrechen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.
1. Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen.
1. Wählen Sie **OK**.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.

Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).
