---
title: In LinkedIn Talent Hub integrieren
description: In diesem Thema wird erläutert, wie die Integration zwischen Microsoft Dynamics 365 Human Resources und LinkedIn Talent Hub eingerichtet werden.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efcac2bd82956015eb822c6a493b8625a35cd194
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805057"
---
# <a name="integrate-with-linkedin-talent-hub"></a>In LinkedIn Talent Hub integrieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) ist eine Bewerber-Nachverfolgungssystemplattform (ATS). Sie können damit Mitarbeiter an einem Ort suchen, verwalten und einstellen. Durch die Integration von Microsoft Dynamics 365 Human Resources mit LinkedIn Talent Hub können Sie auf einfache Weise Mitarbeiterdatensätze in der Personalabteilung für Bewerber erstellen, die für eine Position eingestellt wurden.

## <a name="setup"></a>Einrichtung

Ein Systemadministrator muss Einrichtungs-Aufgaben ausführen, um die Integration mit LinkedIn Talent Hub zu ermöglichen. Erstens in der Power Apps In dieser Umgebung müssen Sie eine Benutzer- und Sicherheitsrolle einrichten, um LinkedIn Talent Hub die entsprechenden Berechtigungen zum Schreiben von Daten in die Personalabteilung zu erteilen.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Verknüpfen Sie Ihre Umgebung mit LinkedIn Talent Hub

1. Öffnen Sie [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Wählen Sie im Dropdown-Menü Benutzer die Option **Produkteinstellungen**.

3. Im linken Navigationsbereich im Abschnitt **Erweitert** wählen Sie **Integrationen**.

4. Wählen Sie **Autorisieren** für die Microsoft Dynamics 365 Human Resources Integration.

5. Auf der Seite **Dynamics 365 Human Resources** wählen Sie die Umgebung aus, mit der LinkedIn Talent Hub verknüpft werden soll, und wählen Sie dann **Verknüpfung**.

    ![LinkedIn Talent Hub Onboarding](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Sie können nur Links zu Umgebungen erstellen, in denen Ihr Benutzerkonto Administratorzugriff sowohl auf die Personalumgebung als auch auf die zugehörige Power Apps Umgebung hat. Wenn auf der Linkseite Personal keine Umgebungen aufgeführt sind, stellen Sie sicher, dass Sie für den Mandanten Personalumgebungen lizenziert haben und dass der Benutzer, den Sie auf der Linkseite angemeldet haben, über Administratorrechte sowohl für die Personalumgebung als auch für die Power Apps Umgebung verfügt.

### <a name="create-a-power-apps-security-role"></a>Eine Power Apps Sicherheitsrolle erstellen

1. Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2. In der **Umgebungen**-Liste wählen Sie die Umgebung aus, die der Personalumgebung zugeordnet ist, mit der Sie Ihre Instanz von LinkedIn Talent Hub verknüpfen möchten.

3. Wählen Sie **Einstellungen**.

4. Erweitern Sie die **Benutzer + Berechtigungen** Knoten und wählen Sie **Sicherheitsrollen**.

5. Auf der **Sicherheitsrollen** Seite in der Symbolleiste wählen Sie **Neue Rolle**.

6. Auf der Registerkarte **Einzelheiten** geben Sie auf der Registerkarte einen Namen für die Rolle ein, z.B. **LinkedIn Talent Hub HRIS-Integration**.

7. Auf der Registerkarte **Anpassung** wählen Sie auf der Registerkarte Organisationsebene **Lesen**-Berechtigung für die folgenden Entitäten aus:

    - Entität
    - Feld
    - Beziehung

8. Speichern und schließen Sie die Sicherheitsrolle.

### <a name="create-a-power-apps-application-user"></a>Erstellen Sie einen Power Apps Anwendungsbenutzer

Für den LinkedIn Talent Hub-Adapter muss ein Anwendungsbenutzer erstellt werden, der dem Adapter die Berechtigung zum Schreiben von Kandidatendatensätzen in der Power Apps Umgebung erteilt.

1. Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2. In der **Umgebungen**-Liste wählen Sie die Umgebung aus, die der Personalumgebung zugeordnet ist, mit der Sie Ihre Instanz von LinkedIn Talent Hub verknüpfen möchten.

3. Wählen Sie **Einstellungen**.

4. Erweitern Sie die **Benutzer + Berechtigungen** Knoten und wählen Sie **Benutzer**.

5. Wählen Sie **Verwalten von Benutzern in Dynamics 365**.

6. Verwenden Sie das Dropdown-Menü über der Liste, um die Ansicht von der Standardansicht **Aktivierte Benutzer** auf **Anwendungsbenutzer** zu ändern.

    ![Anwendungsbenutzeransicht](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Wählen Sie auf der Symbolleiste auf **Neu**.

8. Gehen Sie auf der Seite **neuer Benutzer** folgendermaßen vor:

    1. Ändern Sie den Wert des **Benutzertyp**-Felds auf **Anwendungsbenutzer**.
    2. Stellen Sie das Feld **Benutzername** auf **Dynamics365 HR LinkedIn HRIS-Integration**.
    3. Legen Sie das Feld **Anwendungs-ID** auf **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** fest.
    4. Geben Sie einen beliebigen Wert in die Felder **Vorname**, **Nachname**, und **Erste E-Mail** ein.
    5. Wählen Sie auf der Symbolleiste **Speichern \& Schließen** aus.

### <a name="assign-a-security-role-to-the-new-user"></a>Zuweisen einer Sicherheitsrolle zu einem neuen Benutzer

Nachdem Sie den neuen Anwendungsbenutzer im vorherigen Abschnitt gespeichert und geschlossen haben, kehren Sie zur Seite **Benutzerliste** zurück.

1. Auf der Seite **Benutzerliste** ändern Sie die Ansicht in **Anwendungsbenutzer**.

2. Wählen Sie Anwendungsbenutzer aus, den Sie im vorherigen Abschnitt erstellt haben.

3. Wählen Sie in der Symbolleiste **Rollen verwalten** aus.

4. Wählen Sie die Sicherheitsrolle aus, die Sie zuvor für die Integration erstellt haben.

5. Wählen Sie **OK**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Eine Azure Active Directory App in Human Resources hinzufügen

1. In Dynamics 365 Human Resources öffnen Sie die **Azure Active Directory Anwendungen** Seite.
2. Fügen Sie einen neuen Datensatz der Liste hinzu und wählen Sie die folgenden Felder:

    - **Kundenkennung**: Geben Sie **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** ein.
    - **Name**: Geben Sie den Namen der Power Apps Sicherheitsrolle ein, die Sie zuvor erstellt haben, z.B. **LinkedIn Talent Hub HRIS-Integration**.
    - **Benutzer-ID**: Wählen Sie einen Benutzer aus, der zum Schreiben von Daten in der Personalverwaltung berechtigt ist.

### <a name="create-the-table-in-dataverse"></a>Erstellen Sie die Tabelle in Dataverse

> [!IMPORTANT]
> Die Integration mit LinkedIn Talent Hub hängt von virtuellen Tabellen ab in Dataverse für Human Resources. Als Voraussetzung für diesen Schritt bei der Einrichtung müssen Sie virtuelle Tabellen konfigurieren. Informationen zum Konfigurieren virtueller Tabellen finden Sie unter [Konfigurieren von Dataverse virtuellen Tabellen](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

1. Öffnen Sie in Human Resources die Seite **Dataverse-Integartion**.

2. Wählen Sie die Registerkarte **Virtuelle Tabellen**.

3. Filtern Sie die Entitätsliste nach der zu findenden Entitätsbezeichnung **LinkedIn exportierter Kandidat**.

4. Wählen Sie die juristische Person und dann **Erstellen/Aktualisieren**.

## <a name="exporting-candidate-records"></a>Kandidatendatensätze exportieren

Nach Abschluss der Einrichtung können Personalvermittler und Personalfachleute (HR) die Funktion **Export nach HRIS** in LinkedIn Talent Hub nutzen, um eingestellte Kandidatendatensätze von LinkedIn Talent Hub in die Personalabteilung zu exportieren.

### <a name="export-records-from-linkedin-talent-hub"></a>Exportieren Sie Datensätze von LinkedIn Talent Hub

Nachdem ein Kandidat den Rekrutierungsprozess durchlaufen hat und eingestellt wurde, können Sie den Kandidatendatensatz von LinkedIn Talent Hub in die Personalabteilung exportieren.

1. Öffnen Sie in LinkedIn Talent Hub das Projekt, für das Sie den neuen Mitarbeiter eingestellt haben.

2. Wählen Sie einen Kandidaten-Datensatz aus.

3. Wählen Sie **Status ändern** und dann **Eingestellt**.

4. Im Auslassungsmenü (**...**) für den Kandidaten wählen Sie **Export nach HRIS**.

5. In dem Bereich **Export nach HRIS** geben Sie die Informationen ein, die exportiert werden müssen:

    - In dem Feld **HRIS-Anbieter** wählen Sie **Microsoft Dynamics 365 Human Resources**.
    - Wählen Sie im Feld **Startdatum** ein Startdatum für den Mitarbeiter aus.
    - In dem Feld **Berufsbezeichnung** geben Sie eine Berufsbezeichnung für den Job des neuen Mitarbeiters ein.
    - In dem Feld **Standort** geben Sie im Feld den Standort ein, an dem sich der Mitarbeiter befindet.
    - Geben Sie die E-Mail-Adresse des Mitarbeiters ein oder überprüfen Sie sie.

![In den HRIS-Bereich in LinkedIn Talent Hub exportieren](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Komplettes Onboarding in der Personalabteilung

Kandidatendatensätze, die von LinkedIn Talent Hub in Human Resources exportiert werden, werden im Bereich **Kadidaten zum Einstellen** auf der Seite **Personalverwaltung** angezeigt.

1. Öffnen Sie in Human Resources die Siete **Personalverwaltung**.

2. In dem Abschnitt **Kandidaten zum Einstellen** wählen Sie **Einstellen** für den ausgewählten Kandidaten.

3. In dem Dialogfeld **Stellen Sie einen neuen Mitarbeiter ein** überprüfen Sie den Datensatz und fügen Sie alle erforderlichen Informationen hinzu. Sie können auch die Positionsnummer auswählen, für die der Kandidat eingestellt wurde.

Nachdem Sie die erforderlichen Informationen eingegeben haben, können Sie mit Ihren Standardprozessen zum Erstellen von Mitarbeiterdatensätzen und zum Einbinden von Mitarbeitern fortfahren.

Die folgenden Details werden importiert und in den neuen Mitarbeiterdatensatz aufgenommen:

- Vorname
- Nachname
- Datum des Beschäftigungsbeginns
- E-Mail-Adresse
- Telefonnummer

## <a name="see-also"></a>Siehe auch

[Virtuelle Dataverse-Tabellen konfigurieren](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Was ist Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]