---
title: Kopfzeilen-Steuerelement für Arbeitskraft
description: Dieser Artikel enthält Informationen zum personalisierbaren Header-Steuerelement im Mitarbeiter-Self-Service, im Hub „Personen“ und auf der Seite „Arbeiter“ in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445947"
---
# <a name="worker-header-control"></a>Kopfzeilen-Steuerelement für Arbeitskraft

Microsoft Dynamics 365 Human Resources bietet ein personalisierbares Kopfzeilen-Steuerelement in **Mitarbeiter-Self-Service**, im **Personal**-Hub und auf der optimierten **Arbeiter**-Seite. Die Kopfzeile enthält wichtige Informationen über den Mitarbeiter sowie Einzelklick-Aktionen wie E-Mail, Anruf oder Messaging. Die Kopfzeile kann geändert werden, indem Felder entfernt oder Felder hinzugefügt werden, einschließlich benutzerdefinierter Felder, um zusätzliche Informationen anzuzeigen. Um das neue Header-Steuerelement zu verwenden, gehen Sie zu **Funktionsverwaltung**, und aktivieren Sie die Funktion **Kopfzeilen-Steuerelement für Arbeitskraft**.

## <a name="personalization"></a>Personalisierung

Einer der Hauptvorteile des Kopfzeilen-Steuerelements für Arbeitskraft ist die Möglichkeit, Informationen zu personalisieren, die im Header angezeigt werden.

Oben rechts in der Kopfzeile befindet sich eine Gruppe von drei Feldern, die je nach Status des Mitarbeiters unterschiedliche Daten anzeigen. Diese Gruppe von Feldern wird als Spotlight-Teil der Kopfzeile bezeichnet. Sie können den Spotlight-Teil der Kopfzeile personalisieren, indem Sie die aktuellen Felder entfernen oder Felder hinzufügen. Die Felder, die dem Spotlight-Teil im Kopfzeilen-Steuerelement hinzugefügt werden können, sind für **Mitarbeiter-Self-Service**, **Personen**-Hub und die **Arbeitskraft**-Seite unterschiedlich.

## <a name="employee-self-service"></a>Mitarbeiter-Self-Service

Das Kopfzeilen-Steuerelement für Arbeeitskraft auf der **Mitarbeiter-Self-Service**-Seite enthält folgende Informationen:

- Name der Arbeitskraft
- Personalnummer
- Titel der Position
- Abteilungen
- Arbeitskrafttyp
- Juristische Person des Beschäftigungsverhältnisses
- Dienstjahre
- Vorgesetzter (Manager)
- Positionstyp

Die Kopfzeile enthält auch eine Ein-Klick-Aktion zum Bearbeiten der persönlichen Informationen der Person. Wählen Sie **Persönliche Daten bearbeiten**, um die **Persönliche Informationen**-Seite in **Mitarbeiter-Self-Service** zu öffnen.

## <a name="people-hub"></a>Kontakte-Hub

Der Kopfzeilen-Steuerelement für Arbeeitskraft im **Personen**-Hub (die Seite **Arbeitsbereich „Personen“**) enthält die folgenden Informationen:

- Name der Arbeitskraft
- Personalnummer
- Titel der Position
- Abteilungen
- Arbeitskrafttyp
- Juristische Person des Beschäftigungsverhältnisses
- Dienstjahre
- Vorgesetzter (Manager)
- Positionstyp

Die Kopfzeile enthält auch Einzelklick-Aktionen wie E-Mail, Anruf oder Messaging. Wenn ein Benutzer seine eigenen Informationen auf der **Arbeitsbereich „Personen“**-Seite anzeigt, enthält der Abschnitt mit Einzelklick-Aktionen die **Personendaten bearbeiten**-Schaltfläche. Der Benutzer kann diese Schaltfläche auswählen, um die **Persönliche Informationen**-Seite in **Mitarbeiter-Self-Service** zu öffnen.

## <a name="streamlined-worker-page"></a>Optimierte Arbeitskraft-Seite

Das Kopfzeilen-Steuerelement für Arbeeitskraft auf der optimierten **Arbeitskraft**-Seite enthält folgende Informationen:

- Name der Arbeitskraft
- Personalnummer
- Titel der Position
- Abteilungen
- Arbeitskrafttyp
- Juristische Person des Beschäftigungsverhältnisses

Je nach Status des Mitarbeiters können sich die Daten auf dem Kopf ändern. Wenn der Mitarbeiter beispielsweise das Unternehmen verlassen hat, enthält das Kopfsteuerelement ein **Beendet**-Badge, das Enddatum des Beschäftigungsverhältnisses und den Kündigungsgrund.

Die folgende Tabelle zeigt die Daten, die in der Kopfzeile für verschiedene Mitarbeiterstatus angezeigt werden.

| Mitarbeiterstatus | Daten, die angezeigt werden | Notiz |
|-----------------|--------------------|------|
| Ausstehend | <ul><li>Name</li><li>Personalnummer</li><li>Titel der Position</li><li>Abteilung</li><li>Arbeitskrafttyp</li><li>Juristische Person</li><li>Badge ausstehend</li><li>Startdatum</li><li>Berichtet an</li><li>Positionstyp</li></ul> | |
| Letzte Einstellung | <ul><li>Name</li><li>Personalnummer</li><li>Titel der Position</li><li>Abteilung</li><li>Arbeitskrafttyp</li><li>Juristische Person</li><li>Badge „Letzte Einstellung“</li><li>Dienstjahre</li><li>Berichtet an</li><li>Positionstyp</li></ul> | Standardmäßig wird die **Letzte Einstellung**-Badge für Mitarbeiter angezeigt, die in den letzten sieben Tagen eingestellt wurden. Um diese Einstellung zu ändern, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für den Abschnitt **Datumsbereich für letzte Einstellungen** fest. Um zum Beispiel die **Letzte Einstellung**-Badge der Mitarbeiter anzuzeigen, die in den letzten 14 Tagen eingestellt wurden, stellen Sie das Feld **Zeitraum** auf **14** und **Einheit** auf **Tage** ein. |
| Aktiver Mitarbeiter | <ul><li>Name</li><li>Personalnummer</li><li>Titel der Position</li><li>Abteilung</li><li>Arbeitskrafttyp</li><li>Juristische Person</li><li>Startdatum</li><li>Berichtet an</li><li>Positionstyp</li></ul> | |
| Ausscheidend | <ul><li>Name</li><li>Personalnummer</li><li>Titel der Position</li><li>Abteilung</li><li>Arbeitskrafttyp</li><li>Juristische Person</li><li>Badge „Ausscheidend“</li><li>Dienstjahre</li><li>Berichtet an</li><li>Positionstyp</li></ul> | Standardmäßig wird die **Ausscheidend**-Badge für Mitarbeiter angezeigt, die in den nächsten sieben Tagen ausscheiden. Um diese Einstellung zu ändern, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für den Abschnitt **Datumsbereich für ausscheidende Arbeitskräfte anzeigen** fest. Um zum Beispiel die **Ausscheidend**-Badge der Mitarbeiter anzuzeigen, die in den nächsten 14 Tagen ausscheiden, stellen Sie das Feld **Zeitraum** auf **14** und **Einheit** auf **Tage** ein. |
| Ausgetreten | <ul><li>Ausgetreten-Badge</li><li>Personalnummer</li><li>Datum des Beschäftigungsendes</li><li>Ursachencode</li></ul> | Standardmäßig wird die **Ausgetreten**-Badge für Mitarbeiter angezeigt, die in den letzten sieben Tagen ausgeschieden sind. Um diese Einstellung zu ändern, legen Sie auf der Seite **Personalverwaltungsparameter** auf der Registerkarte **Allgemein** einen Zeitrahmen für den Abschnitt **Datumsbereich der ausgetretenen Arbeitskräfte** fest. Um zum Beispiel die **Ausgetreten**-Badge der Mitarbeiter anzuzeigen, die in den letzten 14 Tagen ausgeschieden sind, stellen Sie das Feld **Zeitraum** auf **14** und **Einheit** auf **Tage** ein. |
