---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (27. Februar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
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
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d8e6a02b43ad60e3a0c4382f98cb808066587da7
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/12/2019
ms.locfileid: "949896"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-27-2019"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent (27. Februar 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Hinzufügen eines Menüs „Benutzerdefinierte Felder“ zur Systemverwaltung

Navigation zum Menü **Benutzerdefinierte Felder** wurde zum Arbeitsbereich **Systemverwaltung** hinzugefügt.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>Ausblenden der Import- und Erstellungsoptionen für neue mobile Anwendungen

So können derzeit keine neuen mobilen Apps in Talent erstellen. Die Option, neue mobile Umgebungen zu erstellen, wurde vom Menü **Mobile App** entfernt.

### <a name="variable-compensation-award-dmf-entity"></a>Prämien bei variabler Vergütung (DMF-Entität)

In dieser Version ist jetzt eine **Prämie bei variabler Vergütung**-Datenverwaltungs-Framework-Entität (DMF) für den Export verfügbar.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>Adressen aus dem Vereinigten Königreich werden in der Personalführungsanalyseseite als Adressen in der Schweiz aufgeführt

In dieser Version werden Adressen nach Ort angezeigt. Diese Version korrigiert Probleme, bei denen in Visualisierungen der Standort von Mitarbeitern verfälscht wurde.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Der Belegschafts-Power BI-Bericht zeigt einen Fehler, wenn ein Arbeitskraftdienstalterdatum ein Schalttag ist

Eine Korrektur wurde an Microsoft Power BI vorgenommen, um die Dienstalterdatumsangaben zu korrigieren, die auf den 29. Februar fallen.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Feste Mitarbeitervergütung, Prämien für variable Mitarbeitervergütung, variable Mitarbeiterpläne (Registrierungen) lassen benutzerdefinierte Felder zu

Benutzerdefinierte Felder können nun zu fester Mitarbeitervergütung, Prämien für variable Mitarbeitervergütung und variablen Mitarbeiterplänen (Registrierungen) hinzugefügt werden. Sie können jetzt weitere Informationen über feste und variable Mitarbeitervergütungspläne zusätzlich zu den Informationen erfassen, die standardmäßig verfügbar sind. Benutzerdefinierte Felder können über die Benutzeroberfläche oder über bereitgestellte Entitäten eingegeben und aktualisiert werden.

### <a name="other-miscellaneous-bug-fixes"></a>Verschiedene andere Fehlerkorrekturen

Es gibt weitere kleinere Fehlerkorrekturen in dieser Version.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="advanced-compensation-security-fixed-and-variable"></a>Erweiterte Vergütungssicherheit (feste oder variable)

In vielen Organisationen hat der Vergütungs- und Vorteilsmanager nur Zugriff auf bestimmte Kompensationsdatensätze. Diese Datensätze sind möglicherweise für Führungskräfte oder regionale Mitarbeiter. Mit dieser Änderung können Personalverwaltungsmitarbeiter Vergütungspläne für verschiedene Mitarbeitergruppen in der Organisation verwalten. Sicherheitsrollen, die festen und variablen Plänen zugewiesen werden können, legen den Zugriff auf die Pläne und die Mitarbeiterdaten in Verbindung mit den Plänen fest (wie z. B. Gehalts- oder Bonusdatensätze). Nur die Rollen mit festgelegtem Zugriff sind in der Lage, Vergütungen für solche Mitarbeiter zu verarbeiten.

### <a name="platform-update-24"></a>Plattformupdate 24

Weitere Informationen über Microsoft Dynamics 365 for Finance and Operations platform update 24 (März 2019) finden Sie unter [Vorschaufunktionen in Finance and Operations, platform update 24 (März 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Feste Mitarbeitervergütung für zukünftige Positionszuweisungen verfügbar machen

Mitarbeiter werden üblicherweise mit einen zukünftigen Startdatum zu einer Organisation hinzugefügt. Diese Änderung ermöglicht das Definieren der festen Mitarbeitervergütung für Mitarbeiter mit zukünftigen Positionszuweisungen.

## <a name="known-issues"></a>Bekannte Probleme

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance-and-operations"></a>Änderungen an der Core HR-Integrationsvorlage (Talent Common Data Service  zu Finance and Operations)
Die Vorlage für Core HR wurde in eine „erweiterte Abfragevorlage“ aktualisiert. Daher ist die erweiterte Abfrage standardmäßig für Projekte verfügbar, die mit dieser Vorlage erstellt werden. Darüber hinaus werden sämtliche Standardzuordnungsfunktionen nur im Editor für erweiterte Abfragen angezeigt. (Standardzuordnungsfunktionen werden als „FN“in den Zuordnungen angezeigt.)

Weitere Informationen über Zuordnungsfehler finden Sie unter [Neuigkeiten oder Änderungen in Dynamics 365 for Talent Core HR (14. Dezember 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

Um die neue Vorlage zu verwenden, erstellen Sie ein neues Projekt, und wählen Sie die neue Talent-Integrationsvorlage aus.

Um Ihre vorhandene Vorlage zu aktualisieren, führen Sie die folgenden Schritte aus.

1. Aktualisieren Sie die folgenden Zuordnungen:

    - **Stellenpositionen zu Positionen:** Entfernen Sie diese Zuordnung.
    - **Stellenpositionen zu übergeordneten Arbeitsaufgaben** Entfernen Sie diese Zuordnung.
    - **Stellenpositionen zur Basisposition:** Neue Zuordnung aus der **Stellenpositionen** Common Data Service für die Entität zur **Basisposition** Finance and Operations Entität hinzufügen. Verschieben zu Position 7 im Nummernkreis.

        [![Stellenpositionen zur Basispositionszuordnung](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Stellenpositionen zu Positionsdetails:** Neue Zuordnung aus der **Stellenpositionen** Common Data Service Entität zu den **Positionsdetails** Finance and Operations Entität hinzufügen. Verschieben zu Position 8 im Nummernkreis.

        [![Stellenpositionen zur Positionsdetailszuordnung](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Stellenpositionen zu Dauerangaben für Positionen:** Neue Zuordnung aus der **Stellenpositionen** Common Data Service  Entität zur **Dauerangaben für Positionen** Finance and Operations Entität hinzufügen.

        [![Stellenpositionen zur Positionsdauerzuordnung](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Stellenpositionen zu Positionshierarchien:** Neue Zuordnung aus der **Stellenpositionen** Common Data Service  Entität zur **Positionshierarchien** Finance and Operations Entität hinzufügen. Wählen Sie **Erweiterte Abfrage** aus, um eine erweiterte Abfrage für Ihr Projekt durchzuführen.

       [![Schaltfläche „Erweiterte Abfrage“](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Fügen Sie die folgenden Zuordnungen hinzu.
    
    [![Zuordnung](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. Wählen Sie den Link **Erweiterte Abfrage und Filterung** neben dem Feld **Suchen** aus.  

    3. Suchen Sie die Spalte **cdm_parentjobpositionid.cdm_jobpositionnumber**, und wählen Sie den Pfeil nach unten auf der rechten Seite aus.

    4. Im angezeigten Dialogfeld wählen Sie **Leere entfernen** aus.

    5. Wählen Sie **Spalte hinzufügen \> Hinzufügen von bedingten Spalten** aus, um einen Standardtransformationswert für HIERARCHYTYPENAME hinzuzufügen.

        [![Befehl „Bedingte Spalte hinzufügen“](./media/Add-column.png)](./media/Add-column.png)

    6. Geben Sie im Dialogfeld **Bedingte Spalte hinzufügen** als Namen der neuen Spalte **HIERARCHYTYPENAME** ein.
    7. Wählen Sie im **Falls**-Teil der Bedingung ein beliebiges Feld aus, verwenden Sie **Ist gleich** als Beziehung aus, und geben Sie einen beliebigen Wert ein. Geben Sie in den **Dann**- und **Andernfalls**-Teilen der Bedingung an, was der Standardwert sein soll. Geben Sie in diesem Fall **Position** für beide Teile ein.

        [![Dialogfeld „Bedingte Spalte hinzufügen“](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. Wählen Sie **OK** aus, um das Dialogfeld **Erweiterte Abfrage und Filterung** zu schließen.
    9. Wählen Sie auf der Seite **Zuordnungsaufgabe** die neue Spalte als Quelle aus, um eine neue Zuordnung für HIERARCHYTYPENAME zu erstellen.

        [![Zuordnung](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)
