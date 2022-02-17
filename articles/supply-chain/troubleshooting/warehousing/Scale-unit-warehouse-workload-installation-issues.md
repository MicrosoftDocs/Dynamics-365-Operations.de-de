---
title: Probleme bei der Verarbeitung treten auf, nachdem eine Scale-Unit Lager Workload installiert wurde
description: Dieses Thema beschreibt Probleme, die kurz nach der Installation eines Scale-Unit Lager Workloads auftreten können, und gibt Hinweise zu deren Behebung.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071632"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Probleme bei der Verarbeitung treten auf, nachdem eine Scale-Unit Lager Workload installiert wurde

Dieses Thema beschreibt Probleme, die kurz nach der Installation eines Scale-Unit Lager Workloads auftreten können, und gibt Hinweise zu deren Behebung.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Problem 1: Fehler nach der Freigabe einer Ladung aus einer Ladungsplanungs-Workbench

### <a name="symptoms-of-issue-1"></a>Symptome von Problem 1

Wenn Sie eine Ladung von der Seite **Lastplanungs-Workbench** oder **Ausgehende Lastplanungs-Workbench** freigeben, erhalten Sie eine Fehlermeldung mit folgendem Formular:

> Beim Buchen der Ladung %1 wurde eine Ausnahmefestgestellt. Die Ladung konnte nicht freigegeben werden.
> 
> whsshipmenttable festlegen aktualisieren ...
> 
> Ein Datensatz in Sendungen (WHSShipmentTable) kann nicht bearbeitet werden. Sendungs-ID: ...

Hier ist ein aktuelles Beispiel, das Beispieldaten enthält:

> Bei der Buchung der Ladung USMF-000033 wurde eine Ausnahme festgestellt, die Ladung konnte nicht freigegeben werden.
Sitzung 5133 (Admin)
>
> update whsshipmenttable set ordernum=?,recversion=?,modifieddatetime=?,modifiedby=? WO ((RECID=?) UND (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Scale Unit @@ hat versucht, Datensätze zu aktualisieren, die der Scale Unit @A gehören.  
> Object Server Azure:
>
> Ein Datensatz in Sendungen (WHSShipmentTable) kann nicht bearbeitet werden. Sendungs-ID: USMF-000031, USMF-000033. Die SQL-Datenbank hat einen Fehler gemeldet.

### <a name="cause-of-issue-1"></a>Ursache von Problem 1

Dieses Problem kann auftreten, wenn die folgende Kombination von Bedingungen bei der Installation des Scale-Unit Lager Workloads vorliegt:

- Das System enthält eine nicht freigegebene Ladung, bei der mehrere Zeilen mit verschiedenen Aufträgen verbunden sind, und einige Zeilen der Ladung sind nicht mit einer Sendung verbunden.
- Das System ist so festgelegt, dass es die Transportkonsolidierung verwendet.

Beim Bereitstellen einer verteilten hybriden Topologie wird jeder Datensatz für Ladungen und Sendungen als Eigentum einer bestimmten Scale-Unit oder eines Hubs gekennzeichnet. Wenn Sie eine Ladung von der Seite **Ladungsplanung Workbench** aus freigeben, ändert das System den zugewiesenen Eigentümer. Aufgrund der zuvor aufgeführten Bedingungen kann das System jedoch möglicherweise die Dateneigentümerschaft nicht auflösen. Daher kann sie die Ladung zum Lager nicht freigeben.

### <a name="resolution-of-issue-1"></a>Auflösung von Ausgabe 1

Teilen Sie die Ladung in zwei kleinere Ladungen auf, bevor Sie sie für das Lager freigeben.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>Problem 2: Fehler bei der Verarbeitung einer Welle in einer Scale-Unit

### <a name="symptoms-of-issue-2"></a>Symptome von Problem 2

Wenn Sie eine Welle auf einer Scale-Einheit verarbeiten, erhalten Sie eine Fehlermeldung mit folgendem Formular:

> Sie können die Zeile mit der Ladung RecId = %1, load id= %2 nicht ändern, da sie noch dem Enterprise Hub gehört. Vergewissern Sie sich, dass die entsprechende ausgehende Ladung an eine Scale-Unit freigegeben und damit Lagerbestellungszeilen erstellt wurden.

Hier ist ein aktuelles Beispiel, das Beispieldaten enthält:

> Infolog für den Auftrag Welle ausführen USMF-000000012 (9223377668365210)  
> Infolog für Aufgabe Execute Wave USMF-000000012 (9223377668370462)  
> Sie können die Zeile mit RecId = 68719478242, load id= USMF-000034 nicht ändern, da sie immer noch dem Enterprise Hub gehört. Vergewissern Sie sich, dass die entsprechende ausgehende Ladung an eine Scale-Unit freigegeben und damit Lagerbestellungszeilen erstellt wurden.

### <a name="cause-of-issue-2"></a>Ursache von Problem 2

Bei der Bereitstellung einer verteilten Hybridtopologie wird das Eigentum an den Ladungs- und Versanddaten einer bestimmten Scale-Unit oder einem Hub zugewiesen. Als Teil der Verarbeitung der Daten wird erwartet, dass das Eigentum an den Daten einer Scale-Unit zugewiesen wird.

Wenn Sie einen Scale-Unit-Workload installieren und eine offene Ladung mit einer Welle verknüpft ist, kann das System das Dateneigentum nicht steuern. Daher schlägt die Verarbeitung der Welle auf der Scale-Unit fehl.

### <a name="resolution-of-issue-2"></a>Lösung von Problem 2

Geben Sie die Ladung zum Lager vom Hub aus frei.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Problembehandlung durch Anzeige des Eigentums und des Ziels eines Datensatzes

In einer verteilten hybriden Topologie werden viele Arten von Datensätzen als Eigentum einer bestimmten Scale-Unit oder eines Hubs gekennzeichnet. Nachdem Sie zu einer verteilten hybriden Topologie gewechselt und/oder einen neuen Scale-Unit Workload festgelegt haben, weist das System jedem relevanten Datensatz das Eigentum zu. Dieser Prozess kann manchmal zu Fehlern oder unerwarteten Ergebnissen führen. Daher können Ihnen die Informationen über die Eigentümerschaft eines Datensatzes und das Übertragungsziel bei der Behebung von Problemen helfen, die auftreten, nachdem Sie diese Arten von Änderungen vorgenommen haben.

Führen Sie die folgenden Schritte aus, um den Besitz und das Übertragungsziel eines Datensatzes anzuzeigen.

1. Öffnen Sie den entsprechenden Datensatz.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Optionen** in der Gruppe **Datensatzinfo** die Option **Alle Felder anzeigen**.
1. Auf der angezeigten Seite werden die Werte für alle Felder angezeigt, die für den ausgewählten Datensatz verfügbar sind. Überprüfen Sie die folgenden Felder:

    - **SYSSCALEUNITID** - Dieses Feld zeigt den aktuellen Besitzer des Datensatzes an.
    - **SYSTARGETSCALEUNITID** - Dieses Feld zeigt die Scale-Unit-ID des Hubs oder der Scale-Unit an, auf die der Datensatz übertragen wird, wenn der aktuelle Besitzer die Arbeit mit ihm beendet hat. Der Wert dieses Feldes wird von Batchaufträgen verwendet, die diese Art von Prozess verwalten. Obwohl dieses Feld nicht direkt mit den Eigentumsverhältnissen zusammenhängt, können sich die Eigentumsverhältnisse ändern, wenn der Datensatz übertragen wird. In einigen Fällen wird dieses Feld leer sein.
