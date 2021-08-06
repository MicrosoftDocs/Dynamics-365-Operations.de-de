---
title: Konfigurieren Sie die Rolle des Abwesenheitsmanagers
description: In diesem Thema wird erläutert, wie Sie die Rolle Abwesenheitsmanager für die Verwaltung von Mitarbeiterurlaub einrichten.
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639605"
---
# <a name="configure-the-absence-manager-role"></a>Konfigurieren Sie die Rolle des Abwesenheitsmanagers

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

In einigen Organisationen verwalten Personalmanager den Urlaub für ihr Team möglicherweise nicht. Stattdessen könnte ein Abwesenheitsmanager diesen Prozess für Teammitglieder über mehrere Abteilungen und Teams hinweg abwickeln. Abwesenheitsmanager verfügen über die folgenden Funktionen für das Urlaubsmanagement:

- Überprüfen und genehmigen Sie Freizeit basierend auf einer alternativen Hierarchie.
- Zeigen Sie die Salden der Teammitglieder an.
- Sehen Sie sich den Abwesenheitskalender an.

## <a name="turn-on-the-feature"></a>Aktivieren Sie die Funktion

1. Wechseln Sie zu **Systemverwaltung** Arbeitsbereiche **Funktionsverwaltung**.

2. Auf der **Funktionsverwaltung** Registerkarte, aktivieren Sie die **(Vorschau) Abwesenheitsmanager zur Verwaltung des Urlaubs** darstellen.

## <a name="define-a-custom-hierarchy"></a>Definieren Sie eine benutzerdefinierte Hierarchie

Die Abwesenheitsmanagerfunktionalität verwendet eine benutzerdefinierte Hierarchie, die konfiguriert werden muss.

1. Im **Organisationsverwaltung** Arbeitsbereich wählen Sie **Typen der Positionshierarchie** aus.

2. Erstellen Sie einen Positionshierarchietyp mit dem Namen **Urlaub**.

3. Im **Urlaub und Abwesenheit** Arbeitsbereich, unter **Links** wählen Sie **Abwesenheits- und Abwesenheitsparameter**.

4. Auf der **Allgemein** Registerkarte in der **Abwesenheitshierarchie** Dropdown-Liste, wählen Sie den Hierarchietyp **Urlaub**, den Sie zuvor erstellt haben. Diese Zuordnung der Abwesenheitshierarchie muss für jede juristische Person ausgefüllt werden, bei der die Abwesenheitsmanagerfunktionalität verwendet wird.

Nachdem der Hierarchietyp definiert wurde, muss der Planstellenhierarchiebericht der Planstelle zugeordnet werden.

1. Im **Organisationsverwaltung** Arbeitsbereich wählen Sie **Alle Positionshierarchien** aus.

2. Wählen Sie die Position aus, der diese Urlaubshierarchie hinzugefügt werden soll.

3. Wählen Sie auf der Registerkarte **Beziehung** **Hinzufügen** aus.

4. Wählen Sie im Feld **Hierarchiename** die Option **Urlaub** aus.

5. Wählen Sie im Feld **Positionsberichte** eine Position aus. Der Name des Arbeiters wird automatisch ausgefüllt, nachdem Sie eine Position ausgewählt haben.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Weisen Sie einem Benutzer die Rolle des Benutzers  zu

Die Rolle des Abwesenheitsmanagers muss Mitarbeitern zugewiesen werden, damit sie Abwesenheitsanträge genehmigen oder ablehnen können.

1. Im **Systemadministrator** Arbeitsbereich **Verknüpfungen** auswählen.

2. Im **Benutzer** Bereich wählen Sie die **Benutzer** Verknüpfung aus.

3. Wählen Sie in der Liste der Benutzer den Benutzer aus, dem Sie die Rolle des Abwesenheitsmanagers zuweisen möchten.

4. Wählen Sie auf der Registerkarte **Rollen des Benutzers** **Rollen zuweisen** aus.

5. Wählen Sie in der Liste die **Abwesenheitsmanager** Rolle aus. Wählen Sie dann **OK** aus.

    > [!IMPORTANT]
    > Stellen Sie sicher, dass dem Benutzer, dem Sie die Rolle des Abwesenheitsmanagers zuweisen, auch die Mitarbeiterrolle zugewiesen wurde. Andernfalls kann die Arbeitskraft die Funktion nicht verwenden.

6. Nachdem Sie die Abwesenheitshierarchie erstellt haben, können Sie sie wie folgt anzeigen:

    1. Im **Organisationsverwaltung** Arbeitsbereich wählen Sie **Positionshierarchie** aus.
    
    2. Wählen Sie im Feld **Hierarchietyp** die Option **Urlaub** aus.

## <a name="absence-manager-workspace"></a>Arbeitsbereich des Abwesenheitsmanagers

Im **Mitarbeiter Selbstservice** Arbeitsbereich der **Abwesenheitsmanager** Registerkarte werden die Abwesenheitsinformationen der Mitarbeiter angezeigt, die dem Abwesenheitsmanager in der Abwesenheitshierarchie zugeordnet sind.

Auf der **Urlaub und Abwesenheit** Registerkarte stehen für jeden Mitarbeiter folgende Optionen zur Verfügung:

- **Freizeit** – Zeigen Sie Salden, genehmigte Freizeit und Urlaubsanträge für den ausgewählten Mitarbeiter an.
- **Urlaubssaldi** – Zeigen Sie eine Liste der Salden für die verschiedenen Urlaubspläne für den ausgewählten Mitarbeiter an.

## <a name="approve-time-off-requests"></a>Abwesenheitsanträge genehmigen

Abwesenheitsmanager können Urlaubsanträge für Mitarbeiter genehmigen oder ablehnen. Sie können bei Bedarf auch Anfragen im Namen von Mitarbeitern erstellen.

> [!IMPORTANT]
> Bevor Abwesenheitsmanager Urlaubsanträge genehmigen oder ablehnen können, muss der Abwesenheitsantrag für Arbeitselemente so konfiguriert werden, dass ihnen Urlaubsantrags-Arbeitselemente zur Überprüfung zugewiesen werden.
>
> 1. Auf der **Personal-Workflows** Seite den Abwesenheitsantrag-Workflow auswählen oder erstellen.
> 2. Wählen Sie die **Assoziierte Hierarchie** Option aus und wählen Sie dann im Feld **Hierarchiename** **Urlaub** aus.
> 3. Aktualisieren Sie den Workflow im Workflow-Designer. Unter **Zuweisungstyp** wählen Sie die Option **Hierarchie** und dann auf der **Hierarchieauswahl** Registerkarte, wählen Sie **Konfigurierbare Hierarchie** aus.
>
> Weitere Informationen zum Erstellen von Workflows für Urlaubsanträge finden Sie unter [Erstellen eines Workflows für Urlaubsanträge](hr-leave-and-absence-workflow.md).

1. Wählen Sie im Arbeitsbereich **Mitarbeiter Selbstservice** die Registerkarte **Abwesenheitsmanager** aus.

2. Auf der Registerkarte **Abwesenheitsmanager** wählen Sie den gewünschten Mitarbeiter aus.

3. Wählen Sie **Einzelheiten** und dann **Freizeit**.

4. Suchen Sie den Urlaubsantrag und wählen Sie die Option **Genehmigung**. Sie können dann eine Option zum Genehmigen oder Stornieren des Urlaubsantrags auswählen.

Ein Status **Abbrechen** zeigt an, dass die Anfrage abgelehnt wurde. Ein Status **Abgeschlossen** zeigt an, dass die Anfrage genehmigt wurde.

## <a name="view-time-off-in-the-calendar"></a>Freizeit im Kalender anzeigen

Benutzer in der Rolle des Abwesenheitsmanagers können Urlaubsanträge in ihrem Kalender anzeigen. Wenn Sie auf den Kalender zugreifen wollen, führen sie die folgenden Schritte aus.

> [!IMPORTANT]
> Ein Systemadministrator muss die Ansichtsoptionen für den Kalender des Abwesenheitsmanagers konfigurieren. Auf der **Urlaubs- und Abwesenheitsparameter** Seite, auf der **Kalender** Registerkarte gibt es Optionen zum Ein- und Ausblenden von Geburtstagen, Abwesenheiten ohne Details, Beurlaubungen und ausstehenden Urlaubsanträgen. Es gibt auch eine Option zum Filtern der Kalenderansichtsoption nach Arbeitskrafttyp.

1. Im **Mitarbeiter Selbstservice** Arbeitsbereich **Abwesenheitsmanager** und dann **Kalender des Abwesenheitsmanagers** auswählen.

2. Geben Sie im Feld **Datum** die gewünschten Daten ein.

3. Aktualisieren Sie die Ansichtsoptionen nach Bedarf.

Der Kalender des Abwesenheitsmanagers zeigt alle Datensätze der Mitarbeiter, die dem Abwesenheitsmanager in der Abwesenheitshierarchie berichten.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Einen Urlaubsanforderungsworkflow erstellen](hr-leave-and-absence-workflow.md)
- [Team- und Unternehmenskalender anzeigen](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
