---
title: Übersicht
description: In Dynamics 365 Human Resources bietet der Arbeitsbereich Urlaub und Abwesenheit einen flexiblen Rahmen zum Erstellen neuer Urlaubspläne, Workflows zum Verwalten von Anfragen und eine intuitive Self-Service-Seite, auf der Mitarbeiter eine Freizeitanforderung beantragen können.
author: andreabichsel
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bb123b808615ff7d770c7c6b83338a32d922be3
ms.sourcegitcommit: de217452a85429675994e9cc0e06eb4821cab3e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3325764"
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

- **Urlaubsaussetzung** - Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen. Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt. Wenn die Aussetzung erfolgte, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters. Sie können auch Ursachencodes angeben, wenn Sie die Abwesenheit eines Mitarbeiters aussetzen. Die Benutzererfahrung wurde aktualisiert, um eine Aussetzung anzuzeigen. 

- **Vortragungsregel** - Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. 

- **Fügen Sie Ursachencode und Kommentare für Regulierungen hinzu** – Sie können einen Ursachencode und einen Kommentar hinzufügen, wenn Sie eine Regulierung des Urlaubsguthabens eines Mitarbeiters vornehmen. 

- **Übergang zu Urlaubs- und Abwesenheitsparametern** – Sie können jetzt nur Urlaubs- und Abwesenheitsparameter anstelle von Personalverwaltungsparametern verwenden. 
