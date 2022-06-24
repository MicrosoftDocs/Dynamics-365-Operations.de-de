---
title: Konfigurieren Sie die Rolle des Abwesenheitsmanagers
description: In diesem Artikel wird erläutert, wie Sie die Rolle Abwesenheitsmanager für die Verwaltung von Mitarbeiterurlaub einrichten.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40f9607fb6fc16b96373141d8d2610538e3fdec7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886101"
---
# <a name="configure-the-absence-manager-role"></a>Konfigurieren Sie die Rolle des Abwesenheitsmanagers

>[!Important]
>Die in diesem Artikel beschriebene Funktionalität ist derzeit für Kunden der eigenständigen Version von Dynamics 365 Human Resources verfügbar. Einige oder die gesamten Funktionen werden in einem zukünftigen Release der Finance-Infrastruktur nach Finance-Version 10.0.26 verfügbar sein.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In einigen Organisationen verwalten Personalmanager den Urlaub für ihr Team möglicherweise nicht. Stattdessen könnte ein Abwesenheitsmanager diesen Prozess für Teammitglieder über mehrere Abteilungen und Teams hinweg abwickeln. Abwesenheitsmanager verfügen über die folgenden Funktionen für das Urlaubsmanagement:

- Überprüfen und genehmigen Sie Freizeit basierend auf einer alternativen Hierarchie.
- Zeigen Sie die Salden der Teammitglieder an.
- Sehen Sie sich den Abwesenheitskalender an.

## <a name="turn-on-the-feature"></a>Aktivieren Sie die Funktion

1. Wechseln Sie zu **Systemverwaltung** Arbeitsbereiche **Funktionsverwaltung**.

2. Aktivieren Sie auf der Registerkarte **Funktionsverwaltung** die Funktion **Abwesenheitsmanager zur Verwaltung des Urlaubs**.

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

## <a name="assign-the-absence-manager-role-to-a-user"></a>Weisen Sie einem Benutzer die Rolle des Benutzers zu

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

Im Arbeitsbereich **Mitarbeiter-Self-Service** der Registerkarte **Abwesenheitsverwaltung** werden die Abwesenheitsinformationen der Mitarbeiter angezeigt, die dem Abwesenheitsmanager in der Abwesenheitshierarchie zugeordnet sind. Dem Abwesenheitsmanager stehen einige Optionen zur Verfügung: 
 - Abwesenheitsanträgen überprüfen.</br>
 - Im Namen eines Mitarbeiters einen Abwesenheitsantrag einreichen.</br>
 - Alle ihnen als Teil der Abwesenheitshierarchie zugewiesenen Mitarbeiter anzeigen.</br>
 - Kalender für Abwesenheitsmanager anzeigen.</br>

Der Arbeitsbereich **Abwesenheitsverwaltung** hat zwei Registerkarten:
 - **Abwesenheitsanträge**: Auf dieser Registerkarte werden alle ausstehenden Abwesenheitsanträge aufgelistet, die der Abwesenheitsmanager genehmigen kann. Der Abwesenheitsmanager kann mehrere Datensätze gleichzeitig auswählen und darauf reagieren. Wenn die firmenübergreifende Abwesenheitsansicht aktiviert ist, werden in dieser Liste ausstehende Abwesenheitsanträge für alle juristischen Personen angezeigt, auf die er Zugriff hat. Andernfalls werden die ausstehenden Abwesenheitsanträge für die derzeit ausgewählte juristische Person angezeigt. </br>
 - **Alle Mitarbeiter**: Auf dieser Registerkarte werden alle Mitarbeiter aufgelistet, die dem Abwesenheitsmanager in der Abwesenheitshierarchie zugeordnet sind. Für jeden Mitarbeiter stehen mehrere Optionen zur Verfügung:
    - **Abwesenheit anfordern**: Senden Sie einen neuen Abwesenheitsantrag für den ausgewählten Mitarbeiter.</br>
    - **Freizeit** – Zeigen Sie Salden, genehmigte Freizeit und Urlaubsanträge für den ausgewählten Mitarbeiter an.</br>

## <a name="approve-time-off-requests"></a>Abwesenheitsanträge genehmigen

Abwesenheitsmanager können Urlaubsanträge für Mitarbeiter genehmigen oder ablehnen. 

> [!IMPORTANT]
> Bevor Abwesenheitsmanager Urlaubsanträge genehmigen oder ablehnen können, muss der Abwesenheitsantrag für Arbeitselemente so konfiguriert werden, dass ihnen Urlaubsantrags-Arbeitselemente zur Überprüfung zugewiesen werden.
>
> 1. Auf der **Personal-Workflows** Seite den Abwesenheitsantrag-Workflow auswählen oder erstellen.
> 2. Wählen Sie die **Assoziierte Hierarchie** Option aus und wählen Sie dann im Feld **Hierarchiename** **Urlaub** aus.
> 3. Aktualisieren Sie den Workflow im Workflow-Designer. Unter **Zuweisungstyp** wählen Sie die Option **Hierarchie** und dann auf der **Hierarchieauswahl** Registerkarte, wählen Sie **Konfigurierbare Hierarchie** aus.
>
> Weitere Informationen zum Erstellen von Workflows für Urlaubsanträge finden Sie unter [Erstellen eines Workflows für Urlaubsanträge](hr-leave-and-absence-workflow.md).

1. Wählen Sie im Arbeitsbereich **Mitarbeiter-Self-Service** die Registerkarte **Abwesenheitsverwaltung** aus.

2. Wählen Sie auf der Registerkarte **Abwesenheitsanträge** die Abwesenheitsanträge aus, für die Sie Maßnahmen ergreifen möchten. Sie können in dieser Listenansicht mehrere Datensätze auswählen.

3. Verwenden Sie die interaktiven Schaltflächen oben im Raster, um den Abwesenheitsantrag zu genehmigen, abzulehnen oder zu delegieren. 

Alternativ kann der Benutzer auch die Kachel **Abwesenheitsanträge** auf der linken Seite verwenden, um zur Liste aller Arbeitsaufgaben für Abwesenheitsanträge zu navigieren. 

## <a name="view-time-off-in-the-calendar"></a>Freizeit im Kalender anzeigen

Benutzer in der Rolle des Abwesenheitsmanagers können Urlaubsanträge in ihrem Kalender anzeigen. Wenn Sie auf den Kalender zugreifen wollen, führen sie die folgenden Schritte aus.

> [!IMPORTANT]
> Ein Systemadministrator muss die Ansichtsoptionen für den Kalender des Abwesenheitsmanagers konfigurieren. Auf der **Urlaubs- und Abwesenheitsparameter** Seite, auf der **Kalender** Registerkarte gibt es Optionen zum Ein- und Ausblenden von Geburtstagen, Abwesenheiten ohne Details, Beurlaubungen und ausstehenden Urlaubsanträgen. Es gibt auch eine Option zum Filtern der Kalenderansichtsoption nach Arbeitskrafttyp.

1. Wählen Sie im Arbeitsbereich **Mitarbeiter-Self-Service** **Abwesenheitsverwaltung** und dann **Kalender für Abwesenheitsmanager** aus.

2. Geben Sie im Feld **Datum** die gewünschten Daten ein.

3. Aktualisieren Sie die Ansichtsoptionen nach Bedarf.

Der Kalender des Abwesenheitsmanagers zeigt alle Datensätze der Mitarbeiter, die dem Abwesenheitsmanager in der Abwesenheitshierarchie berichten.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Einen Urlaubsanforderungsworkflow erstellen](hr-leave-and-absence-workflow.md)
- [Team- und Unternehmenskalender anzeigen](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
