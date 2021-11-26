---
title: Masseneinstellungsprojekte
description: Dieses Thema beschreibt Masseneinstellungsprojekte, die es dem Personalverwaltungsspezialisten erlauben, mehrere Positionen zu erstellen und effektiv mehrere Arbeitskräfte für diese Positionen einzustellen.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMMassHireProject, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e0a8bba2227136995542d08f4b3f1e9d6d48ad5
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728655"
---
# <a name="mass-hire-projects"></a>Masseneinstellungsprojekte

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Masseneinstellungsprojekte ermöglichen dem Personalverwaltungsspezialisten mehrere Positionen zu erstellen und effektiv mehrere Arbeitskräfte für diese Positionen einzustellen.

## <a name="overview"></a>Überblick

Verwenden Sie Masseneinstellungsprojekte, wenn Sie mehrere Arbeitskräfte gleichzeitig einstellen, beispielsweise bei Einstellungen zur Deckung eines saisonalen Bedarfs. Die Erstellung eines Masseneinstellungsprojekts ist sinnvoll, da Sie Positionsdatensätze, Arbeitskraftdatensätze und Arbeitskraftzuweisungen für Positionen gleichzeitig erstellen können. Wenn Sie Positionen für ein Masseneinstellungsprojekt erstellen, können Sie die folgenden Informationen angeben:

- die Anzahl der zu erstellenden Positionen
- den Arbeitskrafttyp der Personen, die Sie für die Positionen einstellen
- die Abteilung und den Einzelvorgang, die den Positionen zugeordnet sind
- das Vollzeitäquivalent der Position

## <a name="example"></a>Beispiel

Im Sommer stellen Sie normalerweise 15-20 Teilzeitstudenten ein, die verfügbare Praktikantenstellen in Ihrem Unternehmen ausfüllen. In diesem Jahr möchten Sie fünf Buchhalter, fünf Auftragsbearbeiter und fünf Kassierer einstellen. Anstatt jeden Positionsdatensatz und Arbeitskraftdatensatz separat zu erstellen, erstellen Sie ein Masseneinstellungsprojekt mit der Bezeichnung "SummerInterns". Anfangs- und Enddatum des Projekts entsprechen dem Anfangs- und Enddatum der Dauer der Positionen, die Sie für das Masseneinstellungsprojekt erstellen.

Wählen Sie auf der Seite **Masseneinstellungsprojekte** das Projekt **SummerInterns** aus und klicken Sie auf **Projekt öffnen**. Wählen Sie im geöffneten Masseneinstellungsprojekt auf **Positionen erstellen** aus und geben Sie Informationen zur Buchhalterposition ein. Sie können angeben, dass fünf Buchhalterpositionen erstellt und für jede dieselben Informationen verwendet werden sollen. Wählen Sie dann **OK** aus. Wiederholen Sie diesen Vorgang für die Auftragssachbearbeiter- und Kassiererpositionen.

Nachdem Sie Studenten für die Praktikumspositionen ausgewählt haben, geben Sie die Informationen jedes Studenten unter Positionsdetails für die Position ein, für die sie eingestellt werden. Wenn Sie alle Positionsdetails eingegeben haben, wählen Sie die Position auf der Seite **Masseneinstellungsprojekte** aus, und wählen Sie dann **Einstellen** aus. Für jede Position wird ein Positionsdatensatz erstellt und für jede Person, die Sie einstellen, wird ein Arbeitskraftdatensatz erstellt und der richtigen Position zugewiesen.

## <a name="mass-hire-project-statuses"></a>Status eines Masseneinstellungsprojekts

Ein Masseneinstellungsprojekt kann folgende Status besitzen.

- Erstellt am
- Öffnen
- Geschlossen

Wählen Sie auf der Seite **Masseneinstellungsprojekt** **Projekt öffnen** oder **Projekt schließen** aus, um den Status eines Masseneinstellungsprojekts zu ändern. In der folgenden Tabelle wird erläutert, welche Möglichkeiten Sie im Hinblick auf den Projektstatus haben:

<table>
<thead>
<tr>
<th>Status</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Erstellt</td>
<td>Sie können Informationen erstellen und ändern, können jedoch keine Positionen für das Projekt erstellen. Dies ist der standardmäßige Status von neuen Projekten.</td>
</tr>
<tr>
<td>Geöffnet</td>
<td>Sie können die Projektdetails ändern, Positionen für das Masseneinstellungsprojekt erstellen und Personen für die Positionen einstellen. Dies ist der Status für aktive Projekte.</td>
</tr>
<tr>
<td>Geschlossen</td>
<td><p>Sie können dem Projekt keine Positionen hinzufügen. Wenn Sie dem Masseneinstellungsprojekt Positionen hinzufügen möchten, öffnen Sie das Projekt erneut. Dies ist der Status für abgeschlossene Projekte.</p>
<p><strong>Hinweis:</strong> Ein Masseneinstellungsprojekt kann erst geschlossen werden, wenn alle Positionen im Projekt entweder den Status <b>Erstellt</b> oder den Status <b>Geschlossen</b> haben.</p>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
