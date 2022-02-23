---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (21. Januar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Talent neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528121"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (21. Januar 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Talent sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract. Wir haben Attract um Funktionen erweitert, um unsere jüngste Ankündigung [Aufbau einer erfolgreicheren Belegschaft mit Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/) zu unterstützen.

### <a name="download-environment-data"></a>Download von Umgebungsdaten

Administratoren können die Daten ihrer Umgebung herunterladen. Die Daten werden im Standard-JSON-Format exportiert, wobei alle Jobs, Kandidaten und Konfigurationen in einer ZIP-Datei exportiert werden. Weitere Informationen finden Sie unter [Exportieren von Daten aus Attract und Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Einschränkung des Zugriffs auf Umgebungen für Benutzer ohne Administratorrechte

Administratoren können nun den Zugriff auf die Umgebung für Benutzer ohne Administratorrechte einschränken. Diese Aktion kann nicht rückgängig gemacht werden. Weitere Informationen finden Sie unter [Einschränken des Zugriffs auf Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Onboarding-Guides exportieren

Benutzer können jetzt alle ihre Onboarding-Guides und Onboarding-Vorlagen im Word-Dokumentformat exportieren. Weitere Informationen finden Sie unter [Exportieren von Daten aus Attract und Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2726. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Das letzte Feld für die jährliche Vergütung im Formular zum Überprüfen der Beschäftigung ist nicht konsistent (392092)

Diese Version enthält eine Änderung, mit der die aktuelle Währung, basierend auf dem Unternehmensselektor auf dem Formular **Überprüfen der Beschäftigung**, konsistent abgebildet wird.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Bekannt als Feld, das der Suche nach Feedback-Empfängern hinzugefügt wurde (407789)

Bei der Bereitstellung von Leistungsfeedback hat die Suche nach Arbeitskräften nicht genügend Informationen geliefert, um festzustellen, ob das Feedback an die richtige Person geht. Wir haben eine Spalte **Bekannt als** hinzugefügt, um den eindeutigen Namen des Mitarbeiters zu identifizieren.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo-Datensatz wird ohne Zuordnung zu einer Arbeitskraft erstellt (394526)

Diese Version enthält die Änderung, HCMWorkerPayrollInfo-Datensätze nicht ohne Bezug zu einem Mitarbeiter zu schreiben.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Kann Abteilung beim Navigieren aus der Positionshierarchie heraus bearbeiten (341001)

Wenn die Sicherheit so eingerichtet wurde, dass der Zugriff auf Bearbeitungsabteilungen verweigert wird, ist die Bearbeitung beim Navigieren zum Formular **Abteilungen** in allen Szenarien deaktiviert.

## <a name="coming-soon"></a>Bald verfügbar

Eine neue Common Data Service Lösung wird in Kürze mit den folgenden Änderungen verfügbar sein:

| Beschreibung | Änderung |
| --- | --- |
| **Stelle/Position** Entitätsänderungen | <ul><li>**Kompensationsregion** hinzugefügt</li><li>**Finanzdimensionen** hinzugefügt</li></ul> |
| **Arbeitskraft** Entitätsänderungen | <ul><li>**Namensfolge** hinzugefügt</li><li>**Arbeitet von zu Hause** hinzugefügt</li><li>**Sprache** hinzugefügt</li><li>**Dienstalterdatum** hinzugefügt</li><li>**Jahrestag** hinzugefügt</li><li>**Ursprüngliches Einstellungsdatum** hinzugefügt</li></ul> |
| **Beschäftigung** Entitätsänderungen | <ul><li>**Finanzdimensionen** hinzugefügt</li><li>**Kündigungsgrund** hinzugefügt</li><li>**Kündigungsdatum** umbenannt von **Übergangsdatum**</li><li>**Probezeitdatum** hinzugefügt</li></ul> |
| **Arbeitskraftadresse** Entitätsänderungen | <ul><li>**Straße** hinzugefügt</li><li>**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert</li></ul> |
| Neue variable Vergütung-Einrichtungsentitäten | <ul><li>**Plantyp für variable Vergütung**</li><li>**Plan für variable Vergütung**</li><li>**Übertragungsregeln**</li><li>**Variable Planstufe zur Vergütung**</li></ul> |
| Neue **Arbeitskraftkalender-Beschäftigung** Entität | <ul><li>**Arbeitkraftkalender-Entität** hinzugefügt</li></ul> |
