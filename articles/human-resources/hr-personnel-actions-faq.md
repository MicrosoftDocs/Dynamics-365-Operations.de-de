---
title: Personalaktivitäten – FAQ
description: Dieses Thema enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Ihre Organisation Mitarbeiteraktivitäten verwendet.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c952bdc95b49c92fea34aef63b57c7e193b2f09a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065150"
---
# <a name="personnel-actions-faq"></a>Häufig gestellte Fragen zu Personalaktivitäten


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Ihre Organisation Mitarbeiteraktivitäten verwendet. Mitarbeiteraktivitäten sind zusätzliche Schritte, die Sie ausführen müssen, wenn Sie bestimmte mitarbeiterbezogene Aufgaben ausführen. 

Beispiele für Aufgaben, die möglicherweise Mitarbeiteraktivitäten erfordern, sind:
 - Neue Positionen anlegen. 
 - Vorhandene Positionswerte ändern. 
 - Neue Arbeitskräfte einstellen. 
 - Arbeitskräfte versetzen. 
 - Arbeitskraftvergütung ändern. 
 - Positionszuordnungen ändern. 
 - Arbeitskräften kündigen.

> [!NOTE]
> Personalaktivitäten sind nur aktiviert, wenn **Arbeitskraftaktionen aktivieren** und **Positionsaktionen aktivieren** auf **Ja** gesetzt sind in der Registerkarte **Personalaktivitäten** auf der Seite **Freigegebene Parameter für Personalverwaltung**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Wie kann ich wissen, ob meine Organisation Mitarbeiteraktivitäten benötigt?
Mitarbeiteraktivitäten werden von der Organisation vorgegeben, wenn Sie aufgefordert werden, eine Mitarbeiteraktivität auszuwählen, wenn Sie neue Positionen erstellen, vorhandene Positionen ändern, neue Arbeitskräfte einstellen, Arbeitskräfte übertragen, Arbeitskraftvergütung ändern, Positionszuordnungen ändern, Arbeitskräfte beendenoder Urlaub für Arbeitskräfte eingeben. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Was ist der Unterschied zwischen einer Positionsaktivität und einer Arbeitskraftaktivität?
Es gibt zwei Typen von Mitarbeiteraktivitäten:

- **Position** saktivität: Eine Positionsaktivität wird auf vorhandenen Positionen oder neuen Positionen ausgeführt. Beispielsweise kann eine Positionsaktivität erforderlich sein, wenn Sie einen Wert in einer vorhandenen Position ändern, oder wenn Sie eine neue Saisonposition erstellen. 

- **Arbeitskraft** aktivität: Eine Arbeitskraftaktivität wird für einen vorhandenen Mitarbeiter oder neuen Mitarbeiter ausgeführt. Beispielsweise kann eine Arbeitskraftaktivität erforderlich sein, wenn ein neuer Mitarbeiter eingestellt wird, oder ein vorhandener Mitarbeiter höher gestuft wird. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Was bedeuten die Status der Mitarbeiteraktivitäten?
Personalaktivitäten können folgende Status haben:

- **Entwurf** – Wenn der Workflow verwendet wird, ist die Aktivität noch nicht übermittelt. Wenn kein Workflow verwendet wird, wurde die Aktivität nicht abgeschlossen.
- **Wird überprüft** – Die Personalaktivität wurde dem Workflow übermittelt, aber der Workflow ist nicht abgeschlossen.
- **Genehmigt, im Wartezustand** – Der Workflow ist abgeschlossen, doch die Änderungen sind noch in Bearbeitung. **Abgebrochen**: Der Workflow wurde abgebrochen, oder die Mitarbeiteraktivität wurde zurückgerufen. **Abgelehnt**: Die Aktivitätsanforderung wurde von der genehmigenden Person abgelehnt.
- **Verarbeitung der Aktivität** – Die Aktivitätsanforderung wurde genehmigt und die Änderungen werden verarbeitet.
- **Workflow abgeschlossen**  – Der Workflow ist abgeschlossen und die Änderungen sind verarbeitet. **Fehlgeschlagen**: Der Workflow schlug fehl, da die Informationen veraltet sind. Klicken Sie auf **Reaktivieren**, um die aktuellsten Informationen anzuzeigen und fortzufahren.
- **Abgeschlossen** – Die Position wurde erfolgreich erstellt oder geändert, oder der Mitarbeiter wurde erfolgreich eingestellt, versetzt oder gekündigt oder seine Vergütung wurde geändert. **Fehler**: Ein anderes Problem als veraltete Informationen ist aufgetreten. Öffnen Sie das **Meldungsprotokoll für Personalaktivitäten**, um die Fehlerursache zu bestimmen.
- **Verweigert** – Die Aktivitätsanforderung wurde von der genehmigenden Person abgelehnt.

## <a name="can-i-delete-a-personnel-action"></a>Kann ich eine Mitarbeiteraktivität löschen?
Ja, Sie können Personalaktivitäten löschen, die folgende Staus haben: **Entwurf**, **Fehler**, **Fehlgeschlagen** oder **Abgebrochen**. Sie können Personalaktivitäten, die den Status **Abgeschlossen** haben, nur löschen, wenn Sie die Option **Löschen abgeschlossener Arbeitskräfteaktivitäten zulassen** auf **Ja** auf der Seite **Freigegebene Personalverwaltungsparameter** eingestellt haben.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Was ist die schnellste Methode, um den Status einer Mitarbeiteraktionsaufforderung zu überprüfen?
Öffnen Sie eine der **Mitarbeiteraktivität** slistenseiten und wählen Sie eine Mitarbeiteraktivität aus.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Was ist erforderlich, wenn eine Mitarbeiteraktionsaufforderung fehlschlägt?
Wenn eine Mitarbeiteraktionsaufforderung fehlschlägt, führen Sie die folgenden Schritte aus, um den Fehler zu beheben und die Anforderung erneut zu übermitteln:

> 1. Klicken Sie im **Aktivitätsbereich** auf **Fehlertext**, um den Meldungstext anzeigen, der das Problem beschreibt.
> 
> 2. Klicken Sie im **Aktivitätsbereich** auf **Reaktivieren**, um die aktuellsten Informationen zu laden und den Status der Personalaktivität auf **Entwurf** zurückzusetzen.
> 
> 3. Beheben Sie den Fehler, und klicken Sie dann auf **Abgeschlossen** oder **Übermitteln**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Was passiert mit einer Mitarbeiteraktivität, die Workflows verwendet, wenn die die endgültige Genehmigung abgeschlossen ist?
Wenn keine Fehler vorhanden sind, wird die Mitarbeiteraktivität schreibgeschützt. (Sie können die Historie auf der Listenseite **Alle Arbeitskraftaktivitäten** anzeigen, aber Sie können die Personalaktivität nicht ändern.) Wenn der Status einer Personalaktivität **Abgeschlossen** ist, ist die Position bzw. der Arbeitskraftdatensatz bereits aktualisiert. Um die Änderungen anzeigen, die ausgeführt wurden, öffnen Sie die Listenseite **Positionen** oder **Arbeitskräfte**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Warum erhalte ich den folgenden Fehler, wenn ich einen Wert ungleich 0 im Lohnsatzfeld eingebe? „Der Wert befindet sich außerhalb des zulässigen Bereichs – er muss zwischen 0,00 und 0,00 liegen.“
Sie erhalten diese Nachricht, da das Feld **Ebene** auf der Seite **Stelle** für die Stelle leer ist, der der ausgewählten Position zugeordnet ist.

Um diesen Fehler zu beheben, führen Sie folgende Schritte aus:

> 1. Klicken Sie auf der Seite **Arbeitskraftpositionszuweisung** auf das Feld **Position**.  
> 2. Klicken Sie auf das Feld **Stelle**, um die Seite **Stelle** zu öffnen.
> 3. Klicken Sie im Aktivitätsbereich auf **Bearbeiten**.
> 4. Klicken Sie auf die Registerkarte **Vergütung**.
> 5. Wählen Sie im Feld **Ebene** eine Ebene aus.
> 6. Schließen Sie die Seite **Stelle**.
> 7. Schließen Sie die Seite **Stelle**.
> 8. Kehren Sie zurück zur Registerkarte **Vergütung** auf der Seite **Arbeitskraft**, und wählen Sie **Feste Vergütung**.  Wählen Sie **Neu** aus und geben Sie die Position des Mitarbeiters im Feld **Position** ein.  Geben Sie einen Wert in das Feld für den **Plan** ein und geben Sie im Feld **Lohnsatz** die Mitarbeitervergütung ein.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Warum kann ich das Gültigkeitsdatum in der Kopfzeile der Arbeitskraftaktivitätsseite nicht ändern?
Sie können das Gültigkeitsdatum nicht ändern, da das Feld mit dem logischsten Datum für den Aktivitätstyp ausgefüllt wird.

Beispiele:

- Das Gültigkeitsdatum in der Kopfzeile einer Aktivität **Einer Arbeitskraft kündigen** ist das Datum, das Sie im Feld **Kündigungsdatum** eingegeben haben.
- Das Gültigkeitsdatum einer Aktivität **Eine Arbeitskraft einstellen** ist das Datum, das Sie im Feld **Datum des Beschäftigungsbeginns** eingegeben haben.
- Das Gültigkeitsdatum einer Aktivität **Arbeitskraft versetzen** ist das Datum, das Sie im Feld **Anfangsdatum der Zuordnung** für die Arbeitskraft eingegeben haben.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
