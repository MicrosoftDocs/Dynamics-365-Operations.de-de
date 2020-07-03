---
title: Übersicht
description: In Dynamics 365 Human Resources bietet der Arbeitsbereich Urlaub und Abwesenheit einen flexiblen Rahmen zum Erstellen neuer Urlaubspläne, Workflows zum Verwalten von Anfragen und eine intuitive Self-Service-Seite, auf der Mitarbeiter eine Freizeitanforderung beantragen können.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428966"
---
# <a name="overview"></a>Übersicht

Dynamics 365 Human Resources hilft Ihnen dabei, Ihren Arbeitnehmern großartige Urlaubsleistungen zu bieten. Der Arbeitsbereich **Urlaub und Abwesenheit** bietet einen flexiblen Rahmen zum Erstellen neuer Urlaubspläne, Workflows zum Verwalten von Anfragen und eine intuitive Self-Service-Seite, auf der Mitarbeiter eine Freizeitanforderung beantragen können. Mithilfe von Analysen kann Ihr Unternehmen Urlaubsguthaben und Urlaubsverwendung für Ihre Urlaubspläne messen und überwachen.

## <a name="set-up-leave-and-absence"></a>Einrichten von Urlaub und Abwesenheit

Bevor Sie Urlaubspläne für Ihre Mitarbeiter erstellen, müssen Sie einige Einrichtungsschritte ausführen:

- [Urlaub- und Abwesenheitsparameter konfigurieren](hr-leave-and-absence-parameters.md)
- [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)
- [Einen Urlaubsanforderungsworkflow erstellen](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Dient zum Erstellen und Verwalten von Abwesenheitsplänen

Bevor Sie Urlaubspläne für Ihre Mitarbeiter erstellen, müssen Sie Urlaubs- und Abwesenheitsarten erstellen. Nachdem Sie einen Urlaubsplan erstellt haben, können Sie Mitarbeiter für den Plan registrieren. Sie können auch den Abgrenzungsprozess ausführen, Warnungen erstellen und Analysen für Ihre Pläne anzeigen.

- [Urlaubs- und Abwesenheitstypen konfigurieren](hr-leave-and-absence-types.md)
- [Einen Urlaubs- und Abwesenheitsplan erstellen](hr-leave-and-absence-plans.md)
- [Eine Arbeitskraft einem Urlaubsplan zuweisen](hr-leave-and-absence-enroll.md)
- [Urlaubs- und Abwesenheitspläne antizipieren](hr-leave-and-absence-accrue.md)
- [Analyse für Urlaub und Abwesenheit anzeigen](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Freistellung beantragen und Anfragen verwalten

Ihre Mitarbeiter können Freizeitanträge einreichen und Sie können sie im Arbeitsbereich **Mitarbeiter Selbstservice** verwalten.

- [Arbeitsfreie Zeit anfordern](hr-employee-self-service-request-time-off.md)
- [Urlaubs- und Abwesenheitsanforderungen verwalten](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Urlaub und Abwesenheit bekannte Probleme

### <a name="rounding-precision"></a>Rundungsgenauigkeit

Sie können **Rundungsgenauigkeit** nicht festlegen, wenn Sie **Rundungstyp** festlegen. Sie können nur **Rundungsgenauigkeit** mithilfe der Entität **Urlaubs- und Abwesenheitstyp** festlegen. 

1. Von **Urlaubs- und Abwesenheitsarten** wählen Sie **In Excel öffnen**, um die Entität **Urlaubs- und Abwesenheitstyp** zu öffnen.

2. Nachdem die Datei geöffnet und aktiviert wurde, wählen Sie **Design**.

3. Auf der Tabelle **Urlaubs- und Abwesenheitstyp** wählen Sie in der Tabelle die zu bearbeitende Stiftoption aus.

4. Wählen **Rundungspräzision** und **RoundingType** und dann wählen Sie **Hinzufügen** zum Hinzufügen der Liste der Felder.

5. Wählen Sie **Aktualisierung** und dann **Fertig** aus.

6. Wählen Sie die **Rundungsart** für jeden Urlaubstyp aus oder geben Sie diese ein, falls sie noch nicht festgelegt wurden. 

7. Geben Sie die **Rundungsgenauigkeit** für die entsprechenden Typen ein.

8. Wählen Sie **Veröffentlichen**, um die Änderungen in die Personalabteilung zu übertragen.

## <a name="leave-and-absence-preview-features"></a>Vorschaufunktionen für Urlaub und Abwesenheit

Sie können neue Funktionen für die Vorschau von Abwesenheiten und Urlaubszeiten in einer **Sandkasten** Umgebung ausprobieren. Weitere Informationen zur Aktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

Die Vorschaufunktionen umfassen:

- **Hinterlassen Sie Rückstellungen pro Unternehmen oder Plan** – Sie können den Abgrenzungsprozess entweder für alle Unternehmen oder für ein einzelnes Unternehmen ausführen. Sie können auch den Abgrenzungsprozess für einen bestimmten Urlaubs- und Abwesenheitsplan für ein bestimmtes Unternehmen ausführen. 

- **Urlaub kaufen** – Sie können Kaufurlaubsrichtlinien aktivieren und erstellen, damit Mitarbeiter Kaufanfragen stellen können. Mitarbeiter können Kaufanfragen stellen und Salden automatisch aktualisieren lassen, um die Anfrage widerzuspiegeln.  

- **Fügen Sie genehmigten Urlaubsanträgen Anhänge hinzu** – Sie können einem Urlaubsantrag, der bereits genehmigt wurde, einen Anhang hinzufügen. 

