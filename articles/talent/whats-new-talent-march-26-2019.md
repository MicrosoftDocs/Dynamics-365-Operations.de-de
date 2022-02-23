---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (26. März 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 17eae6c2aa2a1305b1d6f403c595c022f71da48f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529089"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (26. März 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="enhancements-to-interview-scheduling"></a>Verbesserungen für die Gesprächsplanung
Die folgenden Verbesserungen sind für die Gesprächsplanung verfügbar.

- Personalbeschaffer oder zukünftige Vorgesetzte können nun manuell eine Erinnerung für den Gesprächsleiter auslösen, damit er Feedack sendet. Die zugeordnete E-Mail-Vorlage für die Erinnerung ist auch konfigurierbar.
- Währen die Gesprächszusammenfassung mit dem Kandidaten geteilt wird, kann der Gesprächsplaner wählen, die Namen der Gesprächsleiter zu verberge. Er kann ebenfalls Zeilen aus der Gesprächszusammenfassungsansicht auszublenden.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

### <a name="embedded-images-in-activities"></a>Eingebettete Bilder in Aktionen
Sie können jetzt Bildern direkt in Aktivitäten einbetten. Zusätzlich zum in der Lage sein den zu kopieren und einfügen-Bildern über das Internet, können Sie Bilder von Ihrem lokalen Dateisystem hochladen. Die Größe der Aktivität ist auf 1 MB beschränkt. Wenn das Bild zu groß ist, ändern Sie Größe und versuchen Sie, es erneut hochzuladen.

[![Zuordnung](./media/embedimages.png)](./media/embedimages.png)

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
**Build 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Der benutzerdefinierte Feldsupport ist für ausgewählte Entitäten in Common Data Service verfügbar 

Die folgenden Entitäten Common Data Service unterstützen nun die Debitorenfelder, die in Talent erstellt werden:

- Arbeitskraft
- Nationalität
- Veteranenstatus
- Sprachcode
- Auftrag
- Stellentyp
- Stellenfunktion
- Position
- Positionstyp
 
### <a name="employment-history-not-displayed-chronologically"></a>Die Beschäftigungshistorie wird nicht chronologisch angezeigt
Mit dieser Änderung zeigt die Beschäftigungsverlaufsseite nun Beschäftigungszahlen chronologisch, unabhängig des Unternehmens. Sie können auch Sortieroptionen verwenden, um nach Unternehmen zu sortieren.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Feste Vergütungspläne werden nicht angezeigt, wenn Benutzer aus Sicherheitsgründen vom Unternehmen eingeschränkt sind.
In dieser Aktualisierung werden feste Vergütungspläne nun angezeigt, wenn Benutzer aus Sicherheitsgründen vom Unternehmen eingeschränkt sind. Alle Sicherheitseinstellungen werden beachtet und feste Pläne werden die Unternehmen angezeigt, für die der Benutzer die Zugriffsberechtigung hat. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Stellendatensätze können nicht mithilfe der Option Öffnen in Excel im Talent gelöscht werden
Mit dieser Version können Sie nun Stellendatensätze entfernen, indem Sie die Option **In Excel öffnen** in Talent verwenden.

### <a name="upgrade-to-common-data-service"></a>Upgrade auf Common Data Service
Die Fristen für das Upgrade auf Common Data Service kommen schnell näher. Melden Sie sich im Power Apps-Administratorcenter an, um zu bestimmen, ob die Datenbank aktualisiert werden muss. Weitere Informationen über die Termine und erforderlichen Schritte finden Sie unter [Upgrade auf Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Vorschau

Informationen zum Aktivieren von Vorschaufunktionen finden Sie unter [Zugriff auf Vorschaufunktionen in Microsoft Dynamics 365 Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Ermöglichen Sie, dass Ursachencodes für Sonderurlaubstypen angegeben werden können
Organisationen brauchen möglicherweise zusätzliche Informationen zu den betreffenden Freizeitanforderungen. Um diese Informationen zu erhalten, müssen die Mitarbeiter die Ursachencode für ihre Freizeitanforderungen einbeziehen. Mit dieser Aktualisierung können Sie nun die Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Konfigurieren der erforderlichen Ursachencodes, wenn Sie Freizeit für bestimmte Urlaubstypen eingeben
Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit einreichen. Dies ist möglicherweise auf Grundlage einer gesetzlichen Bestimmung in ihrem Land/ihrer Region oder einer Unternehmensrichtlinie erforderlich. Diese Version enthält die Möglichkeit bereit, für die Personalverwaltung anzugegeben, welche Freizeitanforderungen einen Ursachencode benötigen. Dies wird erzwungen, wenn Mitarbeiter Freizeitanforderungen senden, bei denen ein Ursachencode angegeben werden muss.

## <a name="coming-soon"></a>Bald verfügbar

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Erweiterte Vergütungssicherheit (feste oder variable)
In vielen Organisationen hat der Kompensations- und Vergütungsmanager nur Zugriff auf bestimmte Kompensationsdatensätze. Diese Datensätze sind möglicherweise für Führungskräfte oder regionale Mitarbeiter. Mit dieser Änderung kann HR Kompensationspläne für verschiedene Mitarbeitergruppen in der Organisation verwalten. Sie können Sicherheitsrollen festen und variablen Plänen zuordnen, die den Zugriff auf die Pläne und die Mitarbeiterdaten in Verbindung mit den Plänen bestimmen, wie Gehalts- oder Zulagedatensätze. Nur die Rollen mit Zugriff sind in der Lage, Kompensationen für solche Mitarbeiter zu verarbeiten.

###  <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen
Mit dem Plattformupdate 25 für Finance and Operations können Benutzer Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte ausgegeben werden, wenn dies von einem Ereignis ausgelöst wird. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Duplizierte Mitarbeiter suchen: Schnittstellenänderungen
Mit dieser Änderung werden Duplikate erkannt, während Sie Namenfelder eingeben, und ein Status zeigt, wie viele Duplikate gefunden wurden. Sie können die zur Verfügung gestellte Verknüpfung aktivieren, um eine neue Seite zu öffnen, um zu prüfen, ob die gefundene Übereinstimmung verwendet werden soll. Das Duplikatsformular wird nicht automatisch geöffnet, damit die Dateneingabe nicht unterbrochen wird.
