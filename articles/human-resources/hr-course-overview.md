---
title: Überblick über Kurse
description: Dieser Artikel erklärt, wie Human Resources Administratoren und Manager die Funktionen für Kurse nutzen können, um Informationen über die für Arbeitskräfte verfügbaren Kurse zu erhalten.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716336"
---
# <a name="courses-overview"></a>Überblick über Kurse

Microsoft Dynamics 365 Human Resources bietet eine Lösung für die Lernbedürfnisse Ihres Unternehmens. Diese Lösung bietet zwei Lernkurspfade: *virtuelles Lernen* und *von einem Kursleiter geleitet*.

*Virtuelles Lernen* ist eine Lernerfahrung, die durch Online-Ressourcen erweitert wird. Beim *von einem Kursleiter durchgeführten Training* leitet ein Kursleiter eine Trainingseinheit für eine Gruppe von Arbeitskräften oder Lernenden.

In unserem Lernmodul können Fachleute aus dem Bereich Human Resources, Administratoren, Schulungsleiter und Manager beide Lernpfade erstellen und den Arbeitskräften zuweisen.

> [!NOTE]
> Um virtuelle Kurse zu verwenden, müssen Sie die Funktion **Kurserweiterungen** in der Funktionsverwaltung aktivieren.

## <a name="set-up-virtual-courses"></a>Virtuelle Kurse festlegen

Um virtuelle Kurse zu konfigurieren, müssen Sie die Funktion **Kurserweiterungen** in der Funktionsverwaltung aktivieren. Gehen Sie zu **Kurse \> Neu**, und legen Sie die Option **Virtuell** auf **Ja** fest. Nachdem die Funktion aktiviert wurde, ist eine Kursverknüpfung erforderlich. Das Feld **Kursstatus** wird auf **Offen** festgelegt. Die Option **Mitarbeiter zur Selbstregistrierung zulassen** wird auf **Ja** festgelegt, kann aber auch auf **Nein** festgelegt werden.

Nachdem die Funktion **Kurserweiterungen** in der Funktionsverwaltung aktiviert wurde, ergeben sich die folgenden Änderungen:

- Es muss ein Fälligkeitsdatum für die Kurszuweisung festgelegt werden.
- Eine Kursverknüpfung ist erforderlich.
- **Mitarbeiter-Self-Service** zeigt eine Mitarbeiterübersicht in **Kurse** an. Benutzer können Kurse einsehen, die überfällig, bald fällig und zugewiesen sind.
- Arbeitskräfte können virtuelle Kurse absolvieren und sich diese selbst nachweisen.

## <a name="set-up-instructor-led-courses"></a>Lehrergeleitete Kurse festlegen

Von Dozenten geleitete Kurse müssen nicht konfiguriert werden, bevor sie verwendet werden.

Die folgenden Informationen sind optional und können für Kurse angegeben werden. Wenn diese Informationen für Kurse eingegeben werden sollen, sollten sie festgelegt werden, bevor die Datensätze für die Kurse erstellt werden:

- Kurstyp
- Kursraumgruppen
- Kursgruppen
- Kursorte
- Kursräume
- Kursleiter
- Kurstypen

Sie können *Kurstypen* verwenden, um Kurse nach ihrer Struktur oder ihrem Inhalt zu kategorisieren. Sie können Kurstypen auf der Seite  **Kurstypen** erstellen.

Die minimale und maximale Anzahl der Teilnehmer, die Sie für einen Kurs anmelden können, wird auf der Seite **Allgemein** Inforegister der Seite **Kurse** festgelegt.

### <a name="course-setup-type"></a>Kurseinstellungstyp 

*Einrichtungstypen* bestimmen die Struktur des Kurses. Es gibt drei Einrichtungstypen für Kurse.

| Einrichtungstyp | Description |
|------|--------|
| Standard | Kurse dieses Einrichtungstyps haben keine tägliche Agenda. Es ist die Standardeinrichtung, wenn Sie einen neuen Kurs erstellen. |
| Agenda | Wählen Sie diesen Einrichtungstyp, wenn Sie die Details für jeden Tag eines Kurses planen möchten, der über mehrere Tage hinweg stattfindet. |
| Agenda und Sitzung | <p>Wählen Sie diesen Einrichtungstyp für komplexere Kurse. Sie können zum Beispiel die Agenda des Kurses in *Tracks* und *Sitzungen* unterteilen:</p><ul><li>*Tracks* sind spezifische Themenbereiche für einen Kurs.</li><li>*Sessions* unterteilen die Tracks und helfen dabei, bestimmte Prozesse oder Techniken zu identifizieren, die für einen Track relevant sind.</li></ul> |

### <a name="course-tasks"></a>Kursaufgaben

Erledigen Sie für jeden Kurs die folgenden Aufgaben:

- Registrieren Sie die Teilnehmer.
- Legen Sie einen Anmeldeschluss fest.
- Legen Sie die Mindest- und Höchstzahl der Teilnehmer fest.
- Weisen Sie einen Kursort und ein Klassenzimmer zu.
- Empfehlen Sie den Kursteilnehmern Hotels.
- Erstellen Sie eine Kursbeschreibung, die im  **Mitarbeiter-Self-Service** veröffentlicht werden kann.

> [!NOTE]
> Sie können einen Kurs nur löschen, wenn sich niemand für ihn angemeldet hat.

### <a name="course-statuses"></a>Kursstatus

In der folgenden Tabelle finden Sie die Kursstatus und die Aktionen, die für jeden Status ausgeführt werden.

| Status | Aktionen |
|------|--------|
| Erstellt am | <ul><li>Geben Sie Kursinformationen ein, und bearbeiten Sie sie.</li><li>Ändern Sie den Kursstatus auf **Offen**, sodass sich Arbeitskräfte für den Kurs anmelden können.</li></ul> | 
| Geöffnet | <ul><li>Registrieren Sie Teilnehmer für den Kurs.</li><li>Entfernen Sie Teilnehmer aus dem Kurs.</li><li>Bestätigen Sie die Teilnehmer für den Kurs.</li><li>Ändern Sie den Kursstatus auf **Geschlossen** oder **Abgebrochen** für Teilnehmer, deren Status **Bestätigt** ist.</li></ul>|
| Abgeschlossen | Sie können den Kurs erneut öffnen. |
| Abgebrochen | Sie können den Kurs erneut öffnen. |

### <a name="course-participants"></a>Kursteilnehmer

*Kursteilnehmer* sind Arbeitskräfte, die an einem Trainingskurs oder Ereignis teilnehmen. Sie können Teilnehmer nur für offene Kurse registrieren.

### <a name="workflow"></a>Workflow

Mitarbeiter, die sich über die Seite **Mitarbeiter-Self-Service** für einen Kurs anmelden, können ihre Anmeldung zur Genehmigung durch einen Workflow leiten lassen. Sie können einem Kurs auf der Seite **Allgemein** Inforegister der Seite **Kurse** einen Workflow zuweisen.
