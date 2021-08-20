---
title: Sachkontokalender ändern oder neu zuweisen
description: In diesem Thema wird erläutert, wie Sie den Kalender ändern, der einem Sachkonto derzeit zugewiesen ist, und wie Sie diesem Sachkonto einen neuen Kalender zuweisen.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16000243bc8aa76b04ac56dfb8bfbab7cd644eb3120cc68493ff066598f6cf85
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758076"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Sachkontokalender ändern oder neu zuweisen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie den Kalender ändern, der einem Sachkonto derzeit zugewiesen ist, und wie Sie diesem Sachkonto einen neuen Kalender zuweisen.

## <a name="issue"></a>Problem

Unternehmen müssen gelegentlich entweder den vorhandenen Kalender ändern, der einem Sachkonto zugeordnet ist, oder einen neuen Kalender zuweisen.

## <a name="resolution"></a>Lösung

Es gibt zwei Szenarien zum Ändern oder Neuzuweisen eines Sachkontokalenders. Das erste Szenario umfasst die Änderung eines vorhandenen Kalenders, der dem Sachkonto bereits zugeordnet ist. Das zweite Szenario besteht in der Erstellung eines neuen Kalenders und dessen Zuweisung zum Sachkonto. Beide Änderungen können jederzeit vorgenommen werden, auch nachdem Buchungen im Sachkonto gebucht wurden.

### <a name="change-an-existing-fiscal-calendar"></a>Einen vorhandenen Geschäftskalender ändern

Um einen vorhandenen Kalender zu ändern, der Ihrem Sachkonto zugewiesen ist, wechseln Sie zu **Hauptbuch \> Einrichten des Hauptbuchs \> Sachkonto** und wählen den Link für den Finanzkalender aus, um die Seite **Sachkontokalender** zu öffnen.

Es bestehen Beschränkungen bei den möglichen Änderungen eines Kalenders. Beispielsweise können Sie das Start- und Enddatum der *Perioden* in einem Jahr ändern, Sie können jedoch das Start- und Enddatum eines *Jahres* im Kalender nicht ändern.

Um die Perioden in einem Jahr zu ändern, wählen Sie den entsprechenden Kalender und das entsprechende Jahr aus. Verwenden Sie zunächst die Schaltfläche **Periode löschen** aus, um einige oder alle vorhandenen Betriebsperioden zu löschen. Alle Betriebsperioden außer der ersten können gelöscht werden. Verwenden Sie anschließend die Schaltfläche **Periode aufteilen**, um die verbleibende Periode oder Perioden in neue Perioden zu unterteilen, indem Sie ein geeignetes Startdatum für die nächste Periode eingeben.

Nachdem Sie die Perioden in einem Kalender geändert haben, müssen Sie den Prozess **Sachkontoperioden neu berechnen** für jede juristische Person (Firma) ausführen, der der Kalender zugeordnet ist. Auch wenn Sie keinen Warnhinweis zum Abschließen des Schritts erhalten, ist der Neuberechnungsprozess erforderlich, um die Periode zu aktualisieren, die jeder gebuchten Buchung im Sachkonto zugewiesen ist. Wählen Sie **Sachkontoperioden neu berechnen** auf der Seite **Einrichten des Hauptbuchs** in jeder Firma aus, um den Neuberechnungsprozess auszuführen.

Wenn der Neuberechnungsprozess nicht ausgeführt wird, werden Buchungssalden in einer Zwischenbilanz oder in Finanzabschlüssen möglicherweise fälschlicherweise in Perioden einbezogen. In diesem Fall können Sie die Salden jederzeit korrigieren, indem Sie den Neuberechnungsprozess ausführen.

### <a name="assign-a-new-fiscal-calendar"></a>Einen neuen Geschäftskalender zuweisen

Um einen neuen Geschäftskalender zuzuweisen, gehen Sie zu **Hauptbuch \> Einrichten des Hauptbuchs \> Sachkonto** und wählen dort **Bearbeiten** aus, um die Seite **Sachkonto** in den Bearbeitungsmodus zu versetzen. Wählen Sie im Feld **Geschäftskalender** anschließend einen neuen Geschäftskalender aus.

Nachdem Sie den Geschäftskalender für ein Sachkonto geändert haben, müssen Sie **Sachkontoperioden neu berechnen** ausführen. Wenn Sie einem Sachkonto einen neuen Geschäftskalender zuweisen, werden Sie in einer Nachricht daran erinnert, diesen Schritt auszuführen. Obwohl die Meldung möglicherweise darauf hinweist, dass der Neuberechnungsprozess optional ist, ist dies nicht der Fall. Es ist erforderlich, die Periode zu aktualisieren, die den einzelnen gebuchten Buchungen im Hauptbuch zugeordnet ist. Wählen Sie **Sachkontoperioden neu berechnen** auf der Seite **Einrichten des Hauptbuchs** aus, um den Neuberechnungsprozess auszuführen.

Wenn der Neuberechnungsprozess nicht ausgeführt wird, werden Buchungssalden in einer Zwischenbilanz oder in Finanzabschlüssen möglicherweise fälschlicherweise in Perioden einbezogen. In diesem Fall können Sie die Salden jederzeit korrigieren, indem Sie den Neuberechnungsprozess ausführen.
