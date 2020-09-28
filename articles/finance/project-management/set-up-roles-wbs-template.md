---
title: Richten Sie Rollen in Projektstrukturplan-Vorlagen ein
description: Dieses Thema enthält Informationen zum Einrichten von Rolleninformationen in Projektstrukturplan-Vorlagen.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760556"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Richten Sie Rollen in Projektstrukturplan-Vorlagen ein

[!include [banner](../includes/banner.md)]

Projektmanager können Projektstrukturplan (PSP)-Vorlagen einrichten, die sie übernehmen können, wenn sie einen PSP für neue Projekte erstellen. Projektmanager können Rollen hinzufügen, wenn sie eine Vorlage erstellen. Gehen Sie folgendermaßen vor, um eine Rolle in einer PSP-Vorlage zuzuweisen. 

1. Wählen Sie **Projektverwaltung und -buchhaltung** > **Einstellungen** > **Projekte** > **Vorlagen für Projektstrukturpläne** aus.
2. Wählen Sie **Details** für eine ausgewählte PSP-Vorlage aus.
3. Wählen Sie eine Aufgabe in der Liste, und dann im **Rolle**-Feld eine Rolle aus, die der Aufgabe zugewiesen werden soll.

## <a name="work-with-a-wbs"></a>Arbeiten mit einem PSP

Sie können einen neuen PSP erstellen, oder Sie können einen PSP aus einer vorhandenen PSP-Vorlage kopieren. Ein Projektmanager kann die Ressourcen problemlos verwaltet werden, indem er Rollen in die neuen Aufgaben im PSP zuweist. Rollen können ersetzt werden, nachdem eine Ressource abgerufen ist oder nachdem eine bestätigte Ressource für die Arbeit an der Aufgabe identifiziert wurde. Diese Flexibilität bietet Projektmanager die Möglichkeit die folgenden Aufgaben ausführen:

- Ermitteln der Anzahl der Ressourcen, die für PSP-Arbeitsplanpakete erforderlich sind.
- Vorkalkulation von Projektkosten.
- Festlegen eines vorläufigen Budgets.
- Vorkalkulation der Aktivitätsdauer auf Grundlage von Rollen und Ressourcen.
- Entwickeln Sie mehrere Projektmanagementpläne auf Grundlage der verfügbaren Projektinformationen.

Es wurden zusätzliche Optionen im PSP zur besseren Verwendung der Ressourcenfunktionalität hinzugefügt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mit der folgenden Option...</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressourcenzuweisungen</td>
<td>Zeigen Sie die zugewiesenen Ressourcen, Datumsangaben, Anzahl Stunden und Buchungstypen für Aufgaben im PSP an.</td>
</tr>
<tr class="even">
<td>Team autom. generieren</td>
<td>Fügen Sie automatisch geplante Ressourcen hinzu, indem Sie Rollen verwenden, die einer Aufgabe zugeordnet sind. Finance schlägt automatisch geplante Ressourcen vor, indem es Multikriterienentscheidungsanalysen verwendet, die auf Rollen basieren. Nachdem Rollen und Aufwand (Stunden) für die Aufgaben eines PSP eingerichtet sind und die Struktur freigegeben wurde, wählen Sie <strong>Team autom. generieren</strong> aus. Die erforderliche Anzahl der geplanten Ressourcen wird dem PSP und zur Registerkarte <strong>Projekt und Teamplanung</strong> hinzugefügt.</td>
</tr>
<tr class="odd">
<td>Ressource (Dropdownliste)</td>
<td>Auf der <strong>Startressourcenzuweisung </strong>-Seite können Sie Ressourcen verbindlich oder nicht verbindlich buchen (je nach angegebener Dauer). Sie können die Ansichtseinstellungen anpassen anpassen, um die Dauer von Ressourcenaktivitäten anzuzeigen und festzulegen. Sie können Ressourcen am Arbeitspaket auswählen und zuweisen, indem Sie die folgenden Optionen des Stücklistenartikels nutzen:
<ul>
<li><strong>Übernehmen</strong> - Bestätigen von Änderungen an der Ressource, die einer Aufgabe zugewiesen ist.</li>
<li><strong>Stornieren</strong> - Stornieren von Änderungen an der Ressource, die einer Aufgabe zugewiesen ist.</li>
<li><strong>Automatisch zuweisen</strong> – Eine verfügbare Ressource mit Personal und einer übereinstimmenden Rolle wird automatisch ausgewählt und zur ausgewählten Aufgabe zugewiesen.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Wählen Sie auf der Seite **Alle Projekte** das Projekt **XYZ Upgrade-Phase 2** aus.
2. Wählen Sie **Plan** > **Aktivitäten** > **Projektstrukturplan** aus.
3. Wählen Sie **Neu** aus, um die folgenden Ebene-1-Aktivitäten dem PSP hinzuzufügen:

    - Initiieren
    - Planung
    - Ausführung
    - Überwachen und Steuern
    - Abschluss

4. Legt die Datumsangaben und den Aufwand (Stunden) wie in der folgenden Abbildung gezeigt fest.

    [![Einrichten der Datumsangaben und des Aufwands](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Wählen Sie die **Initiieren**-Aufgabenposition, und wählen Sie dann im **Rolle**-Feld **Senior-Projektmanager**.
6. Wählen Sie **Veröffentlichen** aus.
7. Wählen Sie in der gleichen Position im Feld **Ressource** **Daniel Goldschmidt** und dann die Option für **Akzeptieren**aus.
8. Wählen Sie die **Planung**-Aufgabenposition, und wählen Sie dann im **Rolle**-Feld **Business Analyst**.
9. Wählen Sie **Veröffentlichen** und **Team autom. generieren** aus.
10. Wählen Sie im Benachrichtigungsfeld **Ja** aus.
11. Prüfen Sie im **Ressource**-Feld, ob der Wert **Business Analyst 1** ist.
12. Für die **Business Analyst 1**-Ressource öffnen Sie die Suche und wählen **Ressourcenzuweisungsformular starten** aus. Wählen Sie dann eine Arbeitskraft für die Aufgabe aus.
13. Wählen Sie **Nicht verbindlich zuweisen** &gt; **Vollständige Kapazität** aus.

    > [!NOTE] 
    > Es wird keine Warnung angezeigt, dass die angegebene Ressource jetzt 2 ist, da die Anzahl der Ressourcen 1 bleibt.

14. Prüfen Sie auf der Seite **Projektstrukturplan** die Ressourcenzuweisung im PSP, und wählen Sie anschließend **Speichern** aus.
