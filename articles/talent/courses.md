---
title: Kursschulungen einrichten
description: "Personalverwaltungsadministratoren und ein Manager können die Kursfunktionen verwenden, um Informationen zur Schulung zu verwalten, welche für Arbeitskräfte angeboten wird."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0ab79e85872c19e30f24e182ea483687ecc0bc09
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-training-courses"></a>Kursschulungen einrichten

[!include[banner](includes/banner.md)]


Personalverwaltungsadministratoren und ein Manager können die Kursfunktionen verwenden, um Informationen zur Schulung zu verwalten, welche für Arbeitskräfte angeboten wird.

 <a name="set-up-prerequisites"></a>Einrichten von Voraussetzungen
---------------------

Die folgenden Informationen werden benötigt und müssen eingerichtet werden, bevor Sie Kurse erstellen.
-   **Kurstypen**

Die folgenden Informationen sind optionale Informationen, die Sie für Kurse angeben können. Wenn Sie wissen, dass Sie diese Informationen für Kurse eingeben werden, sollten Sie dies tun, bevor Sie Kursdatensätze erstellen.
-   **Kursraumgruppen**
-   **Kursgruppen**
-   **Kursorte**
-   **Kursräume**
-   **Kursleiter**

## <a name="course-types"></a>Kurstypen
Kurstypen können verwendet werden, um Kurse entsprechend ihrer Struktur oder ihrem Inhalt zu kategorisieren. Sie können Kurstypen auf der Seite **Kurstypen** erstellen. Sie müssen einen Kurstyp auswählen, wenn einen Kursdatensatz erstellen.

## <a name="course-setup-type"></a>Kurseinstellungstyp
In der folgenden Tabelle werden die drei Einstellungstypen für Kurse aufgeführt. Einstellungstypen bestimmen die Struktur des Kurses.

<table>
<thead>
<tr class="header">
<th>Einstellungstyp</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standard</strong></td>
<td>Wählen Sie diesen Typ für Kurse aus, die keinen täglichen Kursplan haben. Dies ist der Standardeinstellungstyp, wenn Sie einen neuen Kurs erstellen.</td>
</tr>
<tr class="even">
<td><strong>Agenda</strong></td>
<td>Wählen Sie diese Typ aus, um die Details für jeden Tag eines Kurses zu planen, der an mehreren Tagen stattfindet.</td>
</tr>
<tr class="odd">
<td><strong>Agenda und Sitzung</strong></td>
<td>Wählen Sie diesen Typ für komplexere Kurse aus. Sie können etwa den Kursplan in Verläufe und Sitzungen unterteilen.
<ul>
<li><strong>Verlauf</strong> - Verläufe sind bestimmte Fachgebiete für einen Kurs.</li>
<li><strong>Sitzungen</strong> – Sitzungen unterteilen Verläufe und können bestimmte Prozesse oder Techniken abdecken, die für jeden Verlauf relevant sind.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Kursaufgaben
Für jeden Kurs können die folgenden Aufgaben ausgeführt werden.
-   Registrieren von Teilnehmern
-   Angeben einer Registrierungsfrist
-   Festlegen der minimalen und maximalen Teilnehmerzahl.
-   Zuweisen eines Kursorts und Kursraums
-   Empfehlen von Hotels für Kursteilnehmer
-   Erstellen einer Kursbeschreibung, mit der Sie im Mitarbeiter-Self-Service-Portal werben können.

  >**Hinweis** Sie können einen Kurs nur löschen, wenn niemand für ihn registriert ist. 
    
## <a name="course-statuses"></a>Kursstatus
In der folgenden Tabelle werden die möglichen Kursstatus und Aktivitäten aufgelistet, die ausgeführt werden können, wenn der Kurs einen bestimmten Status hat.

<table>
<thead>
<tr class="header">
<th>Status</th>
<th>Aktionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Erstellt</strong></td>
<td><ul>
<li>Geben Sie Kursinformationen ein, und bearbeiten Sie sie.</li>
<li>Ändern Sie den Kursstatus in <strong>Offen</strong>, so dass Arbeitskräfte sich für den Kurs registrieren können.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Offen</strong></td>
<td><ul>
<li>Registrieren Sie Teilnehmer für den Kurs.</li>
<li>Entfernen Sie Teilnehmer aus dem Kurs.</li>
<li>Bestätigen Sie die Teilnehmer für den Kurs.</li>
<li>Ändern Sie den Kursstatus in <strong>Geschlossen</strong> oder <strong>Storniert</strong>.</li>
<li>Planen von Fragebögen für Teilnehmer mit dem Status <strong>Bestätigt</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Geschlossen</strong></td>
<td>Sie können den Kurs erneut öffnen.</td>
</tr>
<tr class="even">
<td><strong>Abgebrochen</strong></td>
<td>Sie können den Kurs erneut öffnen.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kursteilnehmer
Kursteilnehmer sind Arbeitskräfte, Bewerber oder Kontaktpersonen, die an einem Schulungskurs oder Ereignis teilnehmen. Sie können nur Teilnehmer für offene Kurse registrieren. Die Höchst- und Mindestzahl der Teilnehmer, die für einen Kurs registriert werden können, wird im Inforegister **Allgemein** auf der Seite **Kurse** definiert.

<a name="workflow"></a>Workflow
--------

Mitarbeiter, die sich über die Seite **Mitarbeiter-Self-Service** erfassen, können ihre Erfassung per Workflow zur Genehmigung weiterleiten.  Ein Workflow kann für einen Kurs im Inforegister **Allgemein** auf der Seite**Kurse** zugewiesen werden. 






