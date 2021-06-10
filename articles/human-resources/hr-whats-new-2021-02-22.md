---
title: Was ist neu oder geändert in Dynamics 365 Human Resources 22. Februar 2021
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 22. Februar 2021 entweder neu sind oder geändert wurden.
author: marcelbf
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cac3c188e372521a1f63833cd0032f0e9ff7ebe3
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052384"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Was ist neu oder geändert in Dynamics 365 Human Resources 22. Februar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden oder demnächst verfügbar sind.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3988.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Dynamics 365 Human Resources App für Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](./hr-admin-teams-leave-app.md)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können dieses Thema aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Themas in den Build geschafft haben.

| Problemnummer | Abgang |  Beschreibung |
| --- | --- | --- |
| 529994 | Das Ändern des Feldes **Bekannt als** im Formular **Arbeitskraft** löst kein Dataverse-Update aus | Ein Problem wurde behoben, bei dem Dataverse nicht aktualisiert wird, wenn das Feld **Bekannt als** auf dem Formular **Arbeiter** aktualisiert wird. |
| 532651 | Der PBI-Bericht von Compensation analytics verwendet keine Währungsumrechnung bei der Berechnung von Metriken für alle Firmen | Ein Problem wurde behoben, bei dem der Compensation analytics PBI-Bericht die Währungsumrechnung nicht korrekt durchführte. |
| 552226 | Bei der Verarbeitung von Lebensereignissen werden Pläne für ein einzelnes Lebensereignis mehrfach geschlossen und wieder geöffnet  | Es wurde ein Problem behoben, bei dem ein Mitarbeiter in mehreren juristischen Entitäten ist und ein Lebensereignis eintritt, ein Lebensereignis-Datensatz für jede juristische Entität erzeugt wird, in der der Mitarbeiter ist. Bei der Verarbeitung von Lebensereignissen muss die zu verarbeitende juristische Entität ausgewählt werden. Die Verarbeitungslogik beschränkt sich jedoch nicht auf diese juristische Entität. Stattdessen verarbeitet sie für alle juristischen Entitäten und schließt und öffnet die Pläne in der ausgewählten juristischen Entität neu. Durch diese Aktion wird ein Ereignis in derselben juristischen Entität mehrfach verarbeitet, was zu einem mehrfachen Schließen/Wiedereröffnen jedes vom Ereignis betroffenen Plans führt. |
| 518064 | Nur ein Angehöriger auf berechtigten Plänen ausgewählt, wenn mehr als einer als Standard-Beauftragter markiert ist | Es wurde ein Problem behoben, bei dem mehrere Standardbevollmächtigte in berechtigten Plänen nicht automatisch ausgewählt wurden. Sie können jetzt auch einen Hauptbegünstigten für einen persönlichen Kontakt bestimmen. Der primäre Begünstigte wird in berechtigten Plänen als 100% aufgeführt, wenn es mehrere Begünstigte gibt. |
| 552365 | Bring your own database (BYOD)-Exportaufträge schlagen nach einem Upgrade auf Platform update 40 fehl | Es wurde ein Problem behoben, bei dem BYOD-Exporte fehlschlagen, nachdem Platform update 40 auf die Umgebung angewendet wurde. |
| 547123 | Begrenzung der Anzahl der abgefragten Aufgaben in der To-do-Liste auf dem Dashboard | Die Anzahl der Aufgaben, die in der Aufgabenliste angezeigt werden, ist jetzt auf 15 begrenzt, um ein Leistungsproblem zu beheben, das durch eine übermäßige Anzahl von Aufgaben verursacht wurde, die zu laden versuchten. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Unternehmensübergreifende Urlaubsansicht für Manager | [Unternehmensübergreifende Ansicht des Mitarbeiterurlaubs für Manager](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Urlaub- und Abwesenheitsparameter konfigurieren](./hr-leave-and-absence-parameters.md) |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich für Vorteilsverwaltung](hr-benefits-management-workspace.md) |
| Einschränkung der Mitarbeiter bei der Bearbeitung von Geschäftskontaktdetails | [Einschränkung der Mitarbeiter bei der Bearbeitung von geschäftlichen Kontaktdetails](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Bearbeitung von persönlichen Informationen einschränken](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Bald verfügbar

| Funktion | Detaildaten |
| --- | --- |
| Von einem Manager für seine Mitarbeiter eingegebene Qualifikationen können von einem Workflow automatisch genehmigt werden | Bald verfügbar. |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologie-Updates für Microsoft Dataverse

Gültig ab November 2020, Common Data Service wurde umbenannt in [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Siehe die [offizielle Ankündigung](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) im Power Apps-Blog, um mehr zu erfahren. Mit dieser Namensänderung wurden auch einige Begriffe in Dataverse aktualisiert. Beispielsweise ist *Entität* jetzt *Tabelle* und *Feld* *Säule*. Weitere Informationen finden Sie unter [Terminologie-Aktualisierungen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

In dieser Version wurde Terminologie, die sich auf die Dynamics 365 Human Resources-Integration mit Dataverse bezieht, in der gesamten Anwendung aktualisiert, um diese Änderungen widerzuspiegeln. Zum Beispiel ist das **Common Data Service-Integration**-Formular jetzt **Microsoft Dataverse-Integration**.

Weitere Informationen zur Dynamics 365 Human Resources-Integration in Microsoft Dataverse finden Sie unter [Konfigurieren der Microsoft Dataverse-Integration](./hr-admin-integration-common-data-service.md) und [Konfigurieren virtueller Microsoft Dataverse-Tabellen](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Aktualisierungen beim Bereitstellen von Diensten

Beginnend mit der Version vom 22. Februar 2021 passen wir die Bereitstellung von regionalen Service-Updates an. Die Anpassungen umfassen eine Rotation der Reihenfolge, in der die globalen Regionen Updates für den Human Resources-Dienst erhalten, sowie Änderungen bei der Wartezeit zwischen den Update-Stufen. Diese Änderungen bringen uns mehr in Einklang mit den Safe Deployment Practices (SDP), um die Stabilität, Qualität und Supportfähigkeit der Dienste zu verbessern.

Wir werden weiterhin den zweiwöchigen Bereitstellungsrhythmus beibehalten. Kunden werden jedoch möglicherweise feststellen, dass Updates für ihre Human Resources Umgebungen in der Regel an einem anderen Tag des zweiwöchigen Zyklus als in den vorherigen Versionen durchgeführt werden.

Weitere Informationen über den Service-Update-Prozess finden Sie unter [Update-Prozess](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]