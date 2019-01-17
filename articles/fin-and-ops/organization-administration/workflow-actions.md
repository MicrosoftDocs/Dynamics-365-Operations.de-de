---
title: "Aktivitäten in Workflow-Genehmigungsprozessen"
description: "Dieser Artikel beschreibt die Aktivitäten, die jeder Teilnehmer an einen Workflowgenehmigungsprozess ausführen kann."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 829ee16b8fd72a0808a657419524487d9c1b3123
ms.contentlocale: de-de
ms.lasthandoff: 12/18/2018

---

# <a name="actions-in-workflow-approval-processes"></a>Aktivitäten in Workflow-Genehmigungsprozessen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Aktivitäten, die jeder Teilnehmer an einen Workflowgenehmigungsprozess ausführen kann.

Ein Workflow kann mehrere Personengruppen umfassen: den Ersteller, Beauftragte für Aufgaben, Entscheidungsträger und genehmigende Personen. Im folgenden Workflow für Spesenabrechnungen ist z. B. Steffen der Ersteller, die Mitglieder der Warteschlange sind Beauftragte für Aufgaben, Jens ein Entscheidungsträger, während Frank, Saskia und Anne genehmigende Personen sind.

[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)

In den folgenden Abschnitten werden die Workflowaktivitäten erläutert, die von jeder Gruppe ausgeführt werden können.

## <a name="actions-that-an-originator-can-perform"></a>Mögliche Aktivitäten eines Erstellers

Der Ersteller startet eine Arbeitsplaninstanz, indem er ein Dokument zur Bearbeitung übermittelt. Zum Übermitteln seiner Spesenabrechnung muss Steffen z. B. auf der Seite **Spesenabrechnung** auf die Schaltfläche **Absenden** klicken.

## <a name="actions-that-a-task-assignee-can-perform"></a>Mögliche Aktivitäten eines Beauftragten für eine Aufgabe

Eine Aufgabe kann mehreren Personen oder einer von mehreren Personen überwachten Warteschlange für Arbeitsaufgaben zugewiesen werden. Allerdings kann die Aufgabe nur von einer Person ausgeführt werden. Beispielsweise hat Steffen eine Spesenabrechnung übermittelt und die Belege zur Überprüfung an die für Spesenabrechnungen zuständige Abteilung seiner Organisation weitergeleitet.

Die Mitglieder der für Spesenabrechnungen zuständigen Abteilung von Adventure Works überwachen die Warteschlange. Julia, ein Mitglied dieser Abteilung, hat die Aufgabe zur Überprüfung der Spesenabrechung und der Belege von Steffen akzeptiert. Sie kann eine der folgenden Aktivitäten nun ausführen: abschließen, ablehnen, delegieren, Änderungen anfordern, neu zuweisen oder freigeben.

> [!NOTE]
> Die verfügbaren Aktivitäten unterscheiden sich abhängig davon, wie die Aufgabe vom Softwareentwickler entworfen wurde.

### <a name="complete"></a>Abschließen

Wenn ein Benutzer eine Aufgabe abschließt, wird das Dokument, das zur Bearbeitung übermittelt wurde, dem nächsten Benutzer im Arbeitsplan zugewiesen, sofern es einen nächsten Benutzer gibt. Wenn keine weitere Verarbeitung erforderlich ist, wird der Workflowprozess beendet.

Julia, ein Mitglied der für Spesenabrechnungen zuständigen Abteilung von Adventure Works, hat die Aufgabe zur Überprüfung der Spesenabrechung und der Belege von Steffen akzeptiert. Nachdem Julia ihre Überprüfung abgeschlossen hat, wird das Dokument Jens zugewiesen.

### <a name="reject"></a>Ablehnen

Lehnt ein Benutzer ein Dokument ab, endet der Workflowprozess.

Julia, ein Mitglied der für Spesenabrechnungen zuständigen Abteilung von Adventure Works, hat die Aufgabe zur Überprüfung der Spesenabrechung und der Belege von Steffen akzeptiert. Wenn Julia die Spesenabrechnung ablehnt, endet der Workflowprozess.

Steffen kann die Spesenabrechnung erneut übermitteln. Er kann Änderungen zuerst vornehmen, oder er kann die Originalversion erneut übermitteln. Übermittelt Steffen die Spesenabrechnung erneut, beginnt der Workflowprozess mit der manuellen Überprüfungsaufgabe.

### <a name="delegate"></a>Delegat

Wenn ein Benutzer eine Aufgabe delegiert, wird diese einem anderen Benutzer zugewiesen.

Julia, ein Mitglied der für Spesenabrechnungen zuständigen Abteilung von Adventure Works, hat die Aufgabe zur Überprüfung der Spesenabrechung und der Belege von Steffen akzeptiert. Julia delegiert diese Aufgabe an Thomas, ihren Assistenten.

Thomas handelt daraufhin im Auftrag von Julia. Schließt Thomas seine Überprüfung ab, wird die Spesenabrechnung daher Jens zugewiesen – so, als ob die Aufgabe von Julia abgeschlossen worden wäre.

### <a name="request-change"></a>Änderung anfordern

Wenn ein Benutzer eine Änderung an einem übermittelten Dokument anfordert, wird das Dokument zurück an den Ersteller gesendet.

Julia, ein Mitglied der für Spesenabrechnungen zuständigen Abteilung von Adventure Works, hat die Aufgabe zur Überprüfung der Spesenabrechung und der Belege von Steffen akzeptiert. Julia stellt in der Spesenabrechnung einige Fehler fest und fordert Änderungen an. Die Spesenabrechnung wird an Steffen zurückgesendet.

Steffen kann die Spesenabrechnung erneut übermitteln. Er kann die angeforderten Änderungen zuerst vornehmen, oder er kann die Originalversion erneut übermitteln. Übermittelt Steffen die Spesenabrechnung erneut, muss ein Mitglied der Warteschlange für Arbeitsaufgaben die Abrechnung und die Belege erneut überprüfen.

### <a name="reassign"></a>Neu zuordnen

Die Mitglieder einer Warteschlange für Arbeitsaufgaben können Dokumente in dieser Warteschlange einer anderen Warteschlange neu zuweisen.

Julia, ein Mitglied der für Spesenabrechnungen zuständigen Abteilung von Adventure Works, überwacht die Warteschlange. Zur besseren Arbeitsauslastung kann sie die Spesenabrechnung und die beigelegten Belege einer anderen Warteschlange neu zuweisen.

### <a name="release"></a>Freigabe

Gelegentlich kann ein Mitglied einer Warteschlange für Arbeitsaufgaben eine Aufgabe annehmen, aber sich dann entscheiden, dass er oder sie die Aufgabe nicht abschließen kann. In diesem Fall kann die Person, die die Aufgabe angenommen hat, das Dokument zurück an die Warteschlange für Arbeitsaufgaben geben.

Julia, ein Mitglied der für Spesenabrechnungen zuständigen Abteilung von Adventure Works, hat die Aufgabe zur Überprüfung der Spesenabrechung und der Belege von Steffen akzeptiert. Falls Julia entscheidet, dass sie die Aufgabe nicht abschließen kann, kann sie das Dokument freigeben. Die Spesenabrechnung wird an die Warteschlange zurückgegeben, sodass andere Mitglieder der für Spesenabrechnungen zuständigen Abteilung von Adventure Works die Aufgabe abschließen können.

## <a name="actions-that-a-decision-maker-can-perform"></a>Mögliche Aktivitäten eines Entscheidungsträgers

Wird ein Dokument einem Entscheidungsträger zugewiesen, dann in der Regel deshalb, weil eine Frage vom Entscheidungsträger beantwortet werden muss. Die Antwort auf die Frage ist normalerweise **Ja** oder **Nein** oder **Wahr** oder **Falsch**. Falls der Entscheidungsträger keine dieser Möglichkeiten auswählt, kann er oder sie die Entscheidung delegieren.

### <a name="choice-1-or-choice-2"></a>\[Auswahl 1\] oder \[Auswahl 2\]

Ein Entscheidungsträger muss eine Frage zum Dokument beantworten. Die Antwort auf die Frage ist normalerweise **Ja** oder **Nein** oder **Wahr** oder **Falsch**. Durch die vom Entscheidungsträger ausgewählte Antwort wird bestimmt, welche Workflowverzweigung zum Verarbeiten des Dokuments verwendet wird.

Steffens Spesenabrechnung wird beispielsweise Jens zugewiesen. Jens muss entscheiden, ob die Informationen im Dokument einen Anruf beim Vorgesetzten von Steffen erfordern. Wenn Jens entscheidet, dass ein Anruf erforderlich ist, wird die Spesenabrechnung Steffi zugewiesen, die dann den Vorgesetzten von Steffen anrufen muss. Wenn Jens entscheidet, dass kein Anruf erforderlich ist, wird die Spesenabrechnung Frank zur Genehmigung zugewiesen.

### <a name="delegate"></a>Delegieren

Wird ein Entscheidungsträger eine Entscheidung delegiert, wird das Dokument einem anderen Benutzer zugewiesen, der die Entscheidung treffen muss.

Steffens Spesenabrechnung wird beispielsweise Jens zugewiesen. Jens delegiert die Entscheidung an Maria, seine Assistentin.

Maria handelt daraufhin im Auftrag von Jens. Wenn Maria entscheidet, dass ein Anruf bei Steffens Vorgesetztem erforderlich ist, wird die Spesenabrechnung Steffi zugewiesen, die dann Steffens Vorgesetzten anrufen muss. Wenn Maria entscheidet, dass kein Anruf erforderlich ist, wird die Spesenabrechnung Frank zur Genehmigung zugewiesen.

## <a name="actions-that-an-approver-can-perform"></a>Mögliche Aktivitäten einer genehmigenden Person

Wird ein Dokument einer genehmigenden Person zugewiesen, kann diese Person eine der folgenden Aktivitäten ausführen: genehmigen, ablehnen, delegieren oder Änderung anfordern.

### <a name="approve"></a>Genehmigen

Wenn eine genehmigende Person ein Dokument genehmigt, wird das Dokument dem nächsten Benutzer im Workflow zugewiesen, sofern vorhanden. Wenn keine weitere Verarbeitung erforderlich ist, wird der Workflowprozess beendet.

Beispielsweise hat Steffen eine Spesenabrechnung in Höhe von 6.000 Euro übermittelt, und dieses Dokument ist Frank zugewiesen. Wenn Frank das Dokument genehmigt, wird es Saskia zur Genehmigung zugewiesen. Wenn Saskia die Spesenabrechnung genehmigt hat, endet der Workflowprozess.

### <a name="reject"></a>Ablehnen

Wenn eine genehmigende Person ein Dokument ablehnt, wird der Arbeitsplanprozess beendet.

Beispielsweise hat Steffen eine Spesenabrechnung in Höhe von 12.000 Euro übermittelt, und dieses Dokument ist Saskia zugewiesen. Wenn Saskia die Spesenabrechnung ablehnt, endet der Workflowprozess.

Steffen kann die Spesenabrechnung erneut übermitteln. Er kann zuerst Änderungen vornehmen, oder er kann die Originalversion der Abrechnung erneut übermitteln. Übermittelt Steffen die Spesenabrechnung erneut, beginnt der Workflowprozess mit dem Genehmigungsprozess.

### <a name="delegate"></a>Delegieren

Wenn eine genehmigende Person ein Dokument delegiert, wird das Dokument zur Genehmigung einem anderen Benutzer zugewiesen.

Beispielsweise hat Steffen eine Spesenabrechnung in Höhe von 12.000 Euro übermittelt, und dieses Dokument ist Frank zugewiesen. Frank delegiert die Spesenabrechnung an Anne.

Anne handelt daraufhin im Auftrag von Frank. Wenn Anne das Dokument genehmigt, wird es daher Saskia zur Genehmigung zugewiesen – so, als wäre es von Frank genehmigt worden. Nachdem Saskia das Dokument genehmigt hat, wird es zur Genehmigung an Anne gesendet.

### <a name="request-change"></a>Änderung anfordern

Fordert eine genehmigende Person Änderungen an einem Dokument an, wird es an den Ersteller zurückgesendet.

Beispielsweise hat Steffen eine Spesenabrechnung in Höhe von 12.000 Euro übermittelt, und dieses Dokument ist Saskia zugewiesen. Wenn Saskia eine Änderung anfordert, wird die Spesenabrechnung an Steffen zurückgesendet.

Steffen kann die Spesenabrechnung erneut übermitteln. Er kann zuerst die angeforderten Änderungen vornehmen, oder er kann die Originalversion der Abrechnung erneut übermitteln. Übermittelt Steffen die Spesenabrechnung erneut, wird sie zur Genehmigung an Frank gesendet, da Frank die erste genehmigende Person im Genehmigungsprozess ist.

