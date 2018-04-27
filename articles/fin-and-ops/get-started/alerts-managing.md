---
title: "Chargenausführung für Warnungen"
description: "Dieses Thema enthält allgemeine Informationen über die Stapelverarbeitung von Warnungen in Microsoft Dynamics 365 for Finance and Operations."
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: f4c874c148dc10ac658f659896009981962a5802
ms.contentlocale: de-de
ms.lasthandoff: 03/23/2018

---

# <a name="batch-processing-for-alerts"></a>Stapelverarbeitung für Warnungen
[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [banner](../includes/pre-release.md)]

Warnungen werden mit der Stapelverarbeitungsfunktion Microsoft Dynamics 365 for Finance and Operations verarbeitet. Sie müssen die Stapelverarbeitung einrichten, bevor Warnungen übermittelt werden können.

Finance and Operations unterstützt zwei Typen von Ereignissen:

- Ereignisse, die durch änderungsbasierte Ereignisse ausgelöst werden. Diese Ereignisse werden auch als Erstellungs-/Lösch- und Aktualisierungsereignisse bezeichnet.
- Ereignisse, die durch Fälligkeitsdaten ausgelöst werden.

Sie können für beide Ereignistypen Stapelverarbeitungsvorgänge einrichten.
        
## <a name="batch-processing-for-change-based-events"></a>Chargenverarbeitungen für änderungsbasierte Ereignisse
Finance and Operations liest alle änderungsbasierten Ereignisse, die aufgetreten sind, seit die Stapelverarbeitung zuletzt ausgeführt wurde. änderungsbasierte Ereignisse umfassen Aktualisierungen von Feldern, das Löschen von Datensätzen und die Erstellung von Datensätzen. Diese Ereignisse werden mit den Bedingungen verglichen, die in Warnregeln eingerichtet wurden. Wenn ein Ereignis den Regelbedingungen entspricht, erzeugt die Stapelverarbeitung eine Warnung.

### <a name="frequency-for-change-based-events"></a>Einrichten der Stapelverarbeitungshäufigkeit für änderungsbasierte Ereignisse
Für änderungsbasierte Ereignisse können Sie eine Stapelverarbeitung einrichten, die die Verarbeitung eines Ereignisses auslöst, kurz nachdem das System das Ereignis protokolliert hat. Wenn Sie den Stapelverarbeitungsauftrag so einrichten, dass er häufiger ausgeführt wird, erhalten Benutzer Warnungen eher, nachdem eine Änderung eintritt. Eine häufige Stapelverarbeitung kann sich jedoch nachteilig auf die Leistung des Systems auswirken.

Umgekehrt kann eine weniger häufig ausgeführte Stapelverarbeitung, die für Zeiten geplant ist, wenn die Systemlast gering ist, dazu beitragen, die Systemleistung zu verbessern. Eine geringere Häufigkeit der Stapelverarbeitung erfüllt jedoch möglicherweise nicht die Anforderungen der Benutzer für fristgerechte Warnungen.

Daher müssen Sie für die Einstellung der Stapelverarbeitungshäufigkeit von änderungsbasierten Ereignissen einen Kompromiss zwischen dem zeitgerechten Senden von Warnungen und der Leistung des Gesamtsystem finden. Diese Überlegungen werden umso wichtiger, je mehr Benutzer es gibt, die Warnregeln erstellen. Die Häufigkeit wirkt sich nicht auf die Anzahl der Ereignisse aus, die verarbeitet werden müssen. Wenn jedoch mehr Benutzer Regeln erstellen, müssen mehrere Prüfungen ausgeführt werden. Diese Art des Datenverkehrs kann sich auf die Systemleistung auswirken.

#### <a name="the-risks-of-low-batch-frequency"></a>Die Risiken einer niedrigen Chargenfrequenz
Wenn Sie die Stapelverarbeitung für änderungsbasierte Ereignisse auf eine niedrige Häufigkeit festlegen, kann es vorkommen, dass Warnungen verloren gehen, weil sich Daten, die für die Warnregelbedingungen entscheidend sind, geändert haben, bevor die Stapelverarbeitung ausgeführt wurde. Daher verlieren Sie möglicherweise Warnungen.

Beispielsweise ist eine Warnregel so eingerichtet, dass sie eine Warnung auslöst, falls das Ereignis "**Debitorenkontakt ändert sich**" ist und die Bedingung **Debitor = BB** ist. Wenn sich also der Debitorenkontakt für Debitor BB ändert, wird das Ereignis protokolliert. Allerdings ist das Stapelverarbeitungssystem so eingerichtet, dass die Stapelverarbeitung weniger häufig als die Dateneingabe auftritt. Wenn der Debitorennamen sich von **BB** zu **AA** ändert, bevor das Ereignis verarbeitet wird, entsprechen die Daten in der Datenbank nicht mehr die Bedingung in der Regel **Debitor = BB** ab. Wenn das Ereignis schließlich verarbeitet wird, wird daher keine Warnung generiert.

### <a name="set-up-processing-for-change-based-alerts"></a>Einrichten der Verarbeitung von änderungsbasierten Warnungen
1. Gehen sie z &gt; Sie **Systemverwaltung** **Periodische Aufgaben** &gt; **Warnungen** &gt; **Änderungsbasierte Warnungen**.
2. Im Dialogfeld **Änderungsbasierte Warnungen** geben Sie die entsprechenden Informationen ein.

## <a name="batch-processing-for-due-date-events"></a>Chargenverarbeitungen für Ereignisse vom Typ "Fälligkeitsdatum"
Finance and Operations  erfasst alle Ereignisse, die durch Fälligkeitstermine ausgelöst werden, und gleicht diese Ereignisse mit den Bedingungen ab, die in den Warnregeln festgelegt sind. Die Stapelverarbeitung erzeugt eine Warnungen, wenn ein Ereignis den Regelbedingungen entspricht.

### <a name="frequency-for-due-date-events"></a>Festlegen der Häufigkeit für Ereignisse vom Typ "Fälligkeitsdatum"
Für Ereignisse vom Typ "Fälligkeitsdatum" bietet es sich an, Stapelverarbeitungen einzurichten, die nachts oder zu bestimmten Tageszeiten ausgeführt werden, um die Systemlast zu verteilen. Es wird empfohlen, dass Sie den Batchauftrag so einrichten, dass er mindestens einmal pro Tag ausgeführt wird. Sollen Warnungen so früh wie möglich gesendet werden, sollte die Stapelverarbeitung ausgeführt werden, sobald sich das Systemdatum geändert hat. Wenn Sie Warnungen für Ereignisse vom Typ "Fälligkeitsdatum" erzeugen möchten, die auftreten, nachdem eine Stapelverarbeitung bereits Warnungen verarbeitet hat, können Sie die Stapelverarbeitung am selben Tag erneut ausführen.

Beispielsweise wurde ein Stapelverarbeitungsauftrag an einem bestimmten Tag ausgeführt. Dann erstellen Sie eine Bestellung mit einem Fälligkeitsdatum, das eine Warnung für denselben Tag auslösen soll. Um die Warnung an diesem Tag zu erhalten, müssen Sie den Batchauftrag erneut ausführen, nachdem die Bestellung erstellt wurde. Wenn Sie die Stapelverarbeitung an diesem Tag nicht erneut ausführen, erfasst die Stapelverarbeitung am nächsten Tag alle nicht verarbeiteten Ereignisse des Typs "Fälligkeitsdatum", die nicht am Vortag verarbeitet wurden.

> [!NOTE]
> Selbst wenn eine Stapelverarbeitung pro Tag mehrfach ausgeführt wird, werden Warnungen für dasselbe Ereignis vom Typ "Fälligkeitsdatum" und für dieselben Bedingungen nicht mehrfach erzeugt. Warnungen werden nur für Daten erzeugt, die wegen Änderungen im System, die nach dem Ausführen der letzten Stapelverarbeitung aufgetreten sind, zu einem Fälligkeitsdatum geworden sind.

### <a name="batch-processing-window"></a>Stapelverarbeitungsfenster
Die Verarbeitung von Warnregeln in einem Unternehmen kann aus unterschiedlichen Gründen beendet werden. Zu diesen Ursachen zählen Urlaub, Systemfehler oder andere Probleme, die eine Zeit lang verhindern, dass Batchaufträge ausgeführt werden.

Um zu verhindern, dass Fälligkeitswarnungen veralten, da der Batchauftrag während einiger Tage nicht ausgeführt wurde, können Sie ein Stapelverarbeitungsfenster einrichten. Ein Stapelverarbeitungsfenster ermöglicht es, dass eine Stapelverarbeitung für eine bestimmte Anzahl von Tagen nicht ausgeführt wird.

Wenn ein Stapelverarbeitungsfenster eingerichtet wurde, wird eine Warnung gesendet, wenn die Warnregel verarbeitet wird, auch wenn die Warnung das Zeitlimit überschreitet, das in den Fälligkeitskriterien definierte wurde. Eine Warnung wird weiterhin gesendet, solange die Periode, die durch dieses Zeitlimit plus das Stapelverarbeitungsfenster definiert ist, nicht überschritten wird. Wenn die Periode, die durch das Zeitlimit plus Stapelverarbeitungsfenster definiert ist, überschritten wird, wird keine Warnung mehr übermittelt.

### <a name="set-up-processing-for-due-date-alerts"></a>Einrichten der Verarbeitung von Fälligkeitswarnungen
1. Gehen Sie zu **Systemverwaltung** &gt; **Periodische Aufgaben** &gt; **Warnungen** &gt; **Änderungsbasierte Warnungen**.
2. Im Dialogfeld **Warnung Fälligkeitsdatum** geben Sie die entsprechenden Informationen ein.

