---
title: Neuigkeiten oder Änderungen in Dynamics 365 Talent (9. April, 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a4d4de6cf28e24d1265395d6440df85edf71a0d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897855"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Neuigkeiten oder Änderungen in Dynamics 365 Talent (9. April, 2019)

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>LIfecycle Services (LCS) Integration mit "Ein Problem melden"
In Attract und Onboard erstellen Probleme, die von den Endbenutzer mithilfe der Funktion "Problem melden" erfasst werden, nun automatisch Support-Probleme im LCS Projekt des Debitors. Administratoren können anschließend die Probleme selektieren und bei Bedarf an Microsoft senden. Dies ist konsistent damit, wie Core HR Probleme von Endnutzern behandelt.

### <a name="relevance-search"></a>Relevanzsuche
In den Talentpools können Sie nun die gesamte Kandidatendatenbank nach bestimmten Fähigkeiten, Namen oder Ausbildungshintergrund durchsuchen. Sie müssen nicht mehr angegeben, welchen Bereich des Profils des Kandidaten Sie durchsuchen möchten. Attract durchsucht das gesamte Profil und hebt alle Übereinstimmungen hervor. Attract sucht auch alle Dokumente, die für einen Kandidaten verfügbar sind und ordnet die Suchergebnisse logisch an. Darüber hinaus können Sie die Ergebnisse nach Quelle oder nach Silbermedaillengewinner filtern. Weitere Informationen finden Sie unter[Kanditatenprofile suchen und anzeigen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Interessentenempfehlungen
Attract kann dabei unerstützen, die Suche für eine Stelle sofort zu starten, sobald Sie sie aktivieren, indem es intelligente Kandidatenempfehlungen aus der Kandidatendatenbank Ihrer Organisation vornimmt. Die Empfehlungen umfassen die identifizierten Qualifikationen und Ausbildungsinformationen beim Suchen nach relevanten Interessenten. Die Empfehlungen werden auf der Registerkarte **Interessenten** unter einer Stelle angezeigt, wenn sie diese für einen Stellenrekrutierungsprozess aktivieren. Weitere Informationen finden Sie unter [Interessenten-Empfehlungen](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Status über die Verfügbarkeit der Befragungspersonen
Gesprächsplaner können bald  den Status**Abwesend, Arbeit an einem anderen Standort** sehen, um Zeiten zu planen, die für die Befragungspersonen möglicherweise besser passen.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Kandidatengesprächserfahrung: Kalendereinladungen speichern
Kandidaten können nun ihre Gesprächsereignisse herunterladen und in ihren persönlichen Kalendern mithilfe einer .ics-Datei speichern, die nun der E-Mail-Zusammenfassung angehängt ist, die an den Kandidaten gesendet wird.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>LIfecycle Services (LCS) Integration mit "ein Problem melden"
In Attract und Onboard erstellen Probleme, die von den Endbenutzer mithilfe der Funktion "Problem melden" erfasst werden, nun automatisch Support-Probleme im LCS Projekt des Debitors. Administratoren können anschließend die Probleme selektieren und bei Bedarf an Microsoft senden. Dies ist konsistent damit, wie Core HR Probleme von Endnutzern behandelt.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Prozent der variablen Basispläne laden falschen Betrag
Die Freigabe dieser Woche behebt ein Problem, wenn sie variable Vergütungsprämien mithilfe der Berichterstellung Prozent der Basispläne laden.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Datums-Auswahl am letzten gearbeiteten Tag funktioniert nicht einwandfrei
Diese Änderung korrigiert das Problem: Wenn Benutzer **Beschäftigungsenddatum** bearbeitet und das Datum im Kalendersteuerelements auswählt, wird ein Tag zur Auswahl hinzugefügt.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Begrenzt persönliche Aktivitätstypen nach ausgewählter Aktivität
Diese Änderung begrenzt die Aktivitätstypen, die angezeigt werden, wenn sie bestimmte Aktivitäten ausführen. Wenn beispielsweise eine neue Position angefordert wird, stehen nur die neuen Positionsaktivitäten in der Liste von Aktivitäten bereit. Bisher erschienen neue und bearbeitete Aktivitäten. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Verschieben eines Mitarbeiters mit Kompensation in eine zweite juristische Person
Diese Version ermöglicht es, Kompensationen in einer zweiten juristischen Person zu beenden, wenn die Übertragung für eine unternehmensübergreifende Umlagerung ist.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Ausgewählte Kompensation für ein zukünftiges Beschäftigungsverhältnis während einer Übertragung kann nicht ausgewählt werden
Wird ein Mitarbeiter zu einer neuen juristischen Person übertragen wird, können Sie nun die Kompensation für die neue juristische Person während des Übertragungsprozesses festlegen.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Benutzer ist nicht in der Lage, Kompensation während der Positionszuweisung zuzuweisen
Das Hinzufügen einer neuen Positionszuweisung ermöglicht nun das Festlegen der festen Vergütungsdatensätze. 

## <a name="in-preview"></a>Vorschau

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Ermöglichen Sie, dass Ursachencodes für Sonderurlaubstypen angegeben werden können
Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen
Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit senden. Dies kann möglicherweise aufgrund der Unternehmensrichtlinie oder von gesetzlichen Vorgaben der Fall sein. Sie können nun angeben, welche Urlaubstypen einen Ursachencodes erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Freizeitanforderungen angeben.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie Urlaub- und Abwesenheitsbuchungslisten für die Personalverwaltung
Nachverfolgung von Mitarbeiterfreizeit und Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sonder stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige in den Transaktionen (Abgrenzungen, Zuschüsse, Regulierungen und Anforderungen), die die Gründe hinter den Salden anzeigen. 

## <a name="coming-soon"></a>Bald verfügbar

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Verbesserungen zur Benutzeroberfläche, um doppelten Mitarbeiter zu überprüfen
Mit dieser Änderung werden Duplikate erkannt, während Sie Namenfelder eingeben, und ein Status zeigt, wie viele Duplikate gefunden wurden. Sie können die zur Verfügung gestellte Verknüpfung aktivieren, um eine neue Seite zu öffnen, um zu prüfen, ob die gefundene Übereinstimmung verwendet werden soll. Das Duplikatsformular wird nicht automatisch geöffnet, damit die Dateneingabe nicht unterbrochen wird.

###  <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen
Durch Platform update 25 für Finance and Operations können Benutzer Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte gesendet werden, wenn dies von einem Ereignis ausgelöst wird. 
