---
title: Migration zur Planungsoptimierung für die Produktprogrammplanung
description: Dieses Thema enthält Informationen über die neue Engine für die Produktprogrammplanung, die Planungsoptimierung, und über die Migration von der bestehenden Engine.
author: ChristianRytt
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: e9aa911ca22ca2beeffe6bec95f17f94142065e4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348756"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Migration zur Planungsoptimierung für die Produktprogrammplanung

[!include [banner](../includes/banner.md)]

Die eingebaute Produktprogrammplanung soll außer Betrieb genommen werden. Sie wird durch das Add-In „Planungsoptimierung“ für Microsoft Dynamics 365 Supply Chain Management ersetzt. Dieses Thema enthält Informationen über die Auswirkungen auf neue und bestehende Bereitstellungen. Es enthält Informationen über erforderliche Maßnahmen.

Die Planungsoptimierung ermöglicht die Berechnung der Produktprogrammplanung außerhalb des Supply Chain Managements und seiner Azure SQL-Datenbank. Zu den Vorteilen, die mit der Planungsoptimierung verbunden sind, gehören eine verbesserte Leistung und minimierte Auswirkungen auf die SQL-Datenbank bei Produktprogrammplanungsläufen. Da schnelle Planungsläufe auch während der Office-Zeiten durchgeführt werden können, können Planer sofort auf Bedarfs- oder Parameteränderungen reagieren.

Weitere Informationen zur Planungsoptimierung finden Sie unter [Übersicht zur Planungsoptimierung](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Veralterung der bestehenden Produktprogrammplanung

Microsoft ist dabei, die eingebaute Planungs-Engine zugunsten von Planungsoptimierung obsolet zu machen. Diese Änderung betrifft alle Cloud-Umgebungen. Lokale Installationen sind nicht betroffen. Ab Version 10.0.16 erhalten Sie eine Fehlermeldung, wenn Sie die integrierte Produktprogrammplanung ausführen, ohne geplante Produktionsaufträge zu generieren. Der Lauf der Produktprogrammplanung wird jedoch trotz der Fehlermeldung erfolgreich abgeschlossen.

Weitere Informationen über die Veralterung der eingebauten Planungs-Engine finden Sie in den Ankündigungen unter [Entfernte oder außer Betrieb genommene Funktionen in Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Migration, Meldungen und Ausnahmen

Besitzer bestehender Umgebungen, die die eingebaute Produktprogrammplanung betreiben, ohne geplante Produktionsaufträge zu generieren, erhalten eine E-Mail, die Details über den Ausnahmeprozess enthält. Wir empfehlen, dass Sie mit einem Partner zusammenarbeiten, um die Migration zur Planungsoptimierung zu bewerten und zu planen.

Wie bereits erwähnt, erhalten Sie ab Version 10.0.16 eine Fehlermeldung, wenn Sie die eingebaute Produktprogrammplanung ausführen, ohne geplante Produktionsaufträge zu generieren. Diese Fehlermeldung enthält Hinweise zur Migration und Anweisungen zur Beantragung einer Ausnahme.

### <a name="new-deployments"></a>Neue Bereitstellungen

Die Planungsoptimierung sollte als Standard-Masterplanungs-Engine für alle neuen Bereitstellungen in der Cloud betrachtet werden. Im Allgemeinen sollte die Planungsoptimierung für alle neuen Bereitstellungen verwendet werden, die keine geplanten Produktionsaufträge während der Produktprogrammplanung erzeugen. Wenn eine neue Bereitstellung von Funktionen abhängt, die von der Planungsoptimierung derzeit nicht unterstützt werden, können Sie eine Ausnahme beantragen, damit Sie weiterhin die integrierte Produktprogrammplanung verwenden können.

### <a name="existing-deployments"></a>Bestehende Bereitstellungen

Besitzer bestehender Cloud-basierter Bereitstellungen, die von der Produktprogrammplanung abhängen, sollten eine Migration zu Planungsoptimierung planen. Wenn Ihre Implementierung von Funktionen abhängt, die von der Planungsoptimierung derzeit nicht unterstützt werden, können Sie eine Ausnahme beantragen, damit Sie weiterhin die eingebaute Masterplanungs-Engine verwenden können.

Für Umgebungen, die derzeit Produktprogrammplanungsprozesse verwenden, die veraltet sind, sendet Microsoft eine E-Mail an den Administrator der Umgebung. Diese E-Mail enthält Informationen über die Aktionen, die erforderlich sind, um zu migrieren oder eine Ausnahme zu beantragen.

## <a name="the-exception-process"></a>Der Ausnahmeprozess

Sie können eine Ausnahme beantragen, wenn Sie weiterhin die integrierte Produktprogrammplanung verwenden müssen, weil Ihre Geschäftsprozesse stark von mindestens einer Funktion abhängen, die derzeit nicht in der Planungsoptimierung implementiert ist. Eine Liste der verfügbaren Funktionen finden Sie unter [Anpassungsanalyse der Planungsoptimierung](planning-optimization/planning-optimization-fit-analysis.md).

Derzeit sind Ausnahmen für die Migration der Planungsoptimierung nur dann relevant, wenn Ihr Masterplanungsprozess keine Produktion beinhaltet (d.h. geplante Produktionsaufträge, die von der Produktprogrammplanung generiert werden) und Sie die integrierte Masterplanungs-Engine über die Version 10.0.15 hinaus benötigen.

Nachdem die erforderlichen Funktionen verfügbar sind, gewährt Microsoft eine Gnadenfrist, bis die Ausnahme ausläuft. Der Admin der Umgebung wird informiert, wenn die erforderlichen Funktionen verfügbar geworden sind und die Schonfrist begonnen hat.

Das folgende Flussdiagramm fasst die Informationen in diesem Thema zusammen, damit Sie schnell herausfinden können, ob Sie eine Ausnahme anfordern sollten. Wenn Sie eine Ausnahme anfordern müssen, füllen Sie bitte den [Fragebogen zur Migration und zu Ausnahmen zur Planungsoptimierung](https://go.microsoft.com/fwlink/?linkid=2144962) aus und senden Sie ihn ab.

![Ausnahmenflussdiagramm.](media/exception-diagram.png "Ausnahmenflussdiagramm")

> [!NOTE]
> Sie können eine Ausnahme nur für Mandanten anfordern, die derzeit eine Produktionsumgebung enthalten oder enthalten werden, nicht nur für Mandanten mit Sandbox-Umgebungen. Wenn Sie den Ausnahmefehler für die Planungsoptimierung in einer Infrastruktur-as-a-Service (IaaS)-Sandbox-Umgebung deaktivieren müssen, führen Sie die SQL-Abfrage aus, die unter [Sandbox-Umgebungen](#faq-sandbox) bereitgestellt wird.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Sandbox-Umgebungen

Kann ich die integrierte Produktprogrammplanung in meiner Sandbox-Umgebung verwenden? Benötige ich eine Ausnahme?

**Antwort:** Ausnahmen sind für Sandbox-Umgebungen normalerweise nicht relevant, da der Ausnahmefehler Planungsoptimierung die eingebaute Produktprogrammplanung nicht daran hindert, erfolgreich zu laufen. Wenn Sie die Fehlermeldung jedoch stört, können Sie sie in einer IaaS- (nicht Service Fabric-) Sandbox-Umgebung deaktivieren, indem Sie die folgende Abfrage in Ihrer Datenbank ausführen:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Vor-Ort-Umgebungen

Meine Umgebung ist lokal. Benötige ich eine Ausnahme?

**Antwort:** Nein. Eine Ausnahme ist für lokale Umgebungen nicht erforderlich. Sie können weiterhin die eingebaute Produktprogrammplanung verwenden. Ihr Admin der Umgebung wird informiert, wenn eine Aktion erforderlich ist.

### <a name="production-scenarios"></a>Produktionsszenarien

Wir verwenden geplante Produktionsaufträge, aber ich mache mir Sorgen, was passiert, wenn wir auf Version 10.0.16 aktualisieren. Sollte ich irgendwelche Maßnahmen ergreifen?

**Antwort:** Sie sollten sich keine Sorgen machen. Sie können die eingebaute Produktprogrammplanung in Version 10.0.16 weiterhin verwenden. Wir empfehlen Ihnen jedoch zu evaluieren, ob die Migration zur Planungsoptimierung mit der aktuellen Funktionalität beginnen kann. Außerdem empfehlen wir, dass Sie sich über neue Funktionen informieren.

### <a name="email-from-microsoft"></a>E-Mail von Microsoft

Unser Admin in der Umgebung hat eine E-Mail von Microsoft erhalten. In dieser E-Mail steht, dass wir auf die Planungsoptimierung migrieren oder eine Ausnahme beantragen sollen. Muss ich irgendwelche Maßnahmen ergreifen?

**Antwort:** Ja. Ihre Umgebung wird betroffen sein, wenn Sie die Anweisungen in der E-Mail nicht befolgen. Sie können entweder bis zum angegebenen Datum auf die Planungsoptimierung migrieren oder eine Ausnahme anfordern, indem Sie den Link in der E-Mail verwenden. Dieser Link öffnet einen Fragebogen. Nachdem Sie diesen Fragebogen ausgefüllt und gesendet haben, erhalten Sie eine Antwort per E-Mail. Obwohl dieser Prozess manuell ist, versucht Microsoft, innerhalb einer Woche nach dem Senden des Fragebogens zu antworten.

### <a name="error-messages"></a>Fehlermeldungen

Ich verwende Version 10.0.16 oder höher und erhalte die folgende Fehlermeldung, wenn ich die Produktprogrammplanung ausführe. Ist die Produktprogrammplanung blockiert?

> Sie erhalten diese Fehlermeldung, weil die eingebaute Produktprogrammplanung für Szenarien verwendet wurde, die von der Planungsoptimierung unterstützt werden. Sie sollten jetzt zur Planungsoptimierung migrieren, da die derzeitige eingebaute Produktprogrammplanung außer Betrieb genommen wird. Beachten Sie, dass dieser Lauf der Produktprogrammplanung erfolgreich abgeschlossen wurde.
>
> Falls Ihre Migration starke Abhängigkeiten von anstehenden Funktionen hat, kann eine Ausnahme zur weiteren Verwendung der eingebauten Produktprogrammplanung beantragt werden.
>
> Bitte füllen Sie dazu den folgenden Fragebogen aus und beantragen Sie ggf. eine Ausnahme von der Migration zur Planungsoptimierung.

**Antwort:** Nein, die Produktprogrammplanung ist nicht blockiert. Ihre Produktprogrammplanung wurde erfolgreich abgeschlossen, und Sie können das Ergebnis wie gewohnt verwenden. Um jedoch zu vermeiden, dass Sie diese Fehlermeldung bei zukünftigen Läufen der Produktprogrammplanung erhalten, müssen Sie entweder sofort zur Planungsoptimierung migrieren oder eine Ausnahme über den Link in der Fehlermeldung anfordern.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
