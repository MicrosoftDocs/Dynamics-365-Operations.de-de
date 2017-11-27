---
title: Masseneinstellungsprojekte
description: "Masseneinstellungsprojekte ermöglichen dem Personalverwaltungsspezialisten mehrere Positionen zu erstellen und effektiv mehrere Arbeitskräfte für diese Positionen einzustellen."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e98e6b3baf57302804d9171833f2b48b60355b22
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="mass-hire-projects"></a>Masseneinstellungsprojekte

[!include[banner](../includes/banner.md)]


Masseneinstellungsprojekte ermöglichen dem Personalverwaltungsspezialisten mehrere Positionen zu erstellen und effektiv mehrere Arbeitskräfte für diese Positionen einzustellen.

<a name="overview"></a>Überblick
--------

Verwenden Sie Masseneinstellungsprojekte, wenn Sie mehrere Arbeitskräfte gleichzeitig einstellen, beispielsweise bei Einstellungen zur Deckung eines saisonalen Bedarfs. Die Erstellung eines Masseneinstellungsprojekts ist sinnvoll, da Sie Positionsdatensätze, Arbeitskraftdatensätze und Arbeitskraftzuweisungen für Positionen gleichzeitig erstellen können. Wenn Sie Positionen für ein Masseneinstellungsprojekt erstellen, können Sie die folgenden Informationen angeben:
-   die Anzahl der zu erstellenden Positionen
-   den Arbeitskrafttyp der Personen, die Sie für die Positionen einstellen
-   die Abteilung und den Einzelvorgang, die den Positionen zugeordnet sind
-   das Vollzeitäquivalent der Position

## <a name="example"></a>Beispiel
Im Sommer stellen Sie normalerweise 15-20 Teilzeitstudenten ein, die verfügbare Praktikantenstellen in Ihrem Unternehmen ausfüllen. In diesem Jahr möchten Sie fünf Buchhalter, fünf Auftragsbearbeiter und fünf Kassierer einstellen. Anstatt jeden Positionsdatensatz und Arbeitskraftdatensatz separat zu erstellen, erstellen Sie ein Masseneinstellungsprojekt mit der Bezeichnung "SummerInterns". Anfangs- und Enddatum des Projekts entsprechen dem Anfangs- und Enddatum der Dauer der Positionen, die Sie für das Masseneinstellungsprojekt erstellen. 

Wählen Sie auf der Seite **Masseneinstellungsprojekte** das Projekt “SummerInterns” aus und klicken Sie auf **Projekt öffnen**. Klicken Sie im geöffneten Masseneinstellungsprojekt auf **Positionen erstellen**, und geben Sie Informationen zur Buchhalterposition ein. Sie können angeben, dass fünf Buchhalterpositionen mithilfe derselben Informationen erstellt werden sollten. Klicken Sie anschließend auf "OK". Wiederholen Sie diesen Vorgang für die Auftragssachbearbeiter- und Kassiererpositionen. 

Nachdem Sie Studenten für die Praktikumspositionen ausgewählt haben, geben Sie die Informationen jedes Studenten unter **Positionsdetails** für die Position ein, für die sie eingestellt werden. Wenn Sie alle Positionsdetails eingegeben haben, wählen Sie die Position auf der Seite "Masseneinstellungsprojekte" aus, und dann klicken Sie auf **Einstellen**. Für jede Position wird ein Positionsdatensatz erstellt, und für jede Person, die Sie einstellen, wird ein Arbeitskraftdatensatz erstellt und der richtigen Position zugewiesen.

## <a name="mass-hire-project-statuses"></a>Status eines Masseneinstellungsprojekts
Ein Masseneinstellungsprojekt kann folgende Status besitzen.
-   Erstellt
-   Geöffnet
-   Geschlossen

Klicken Sie auf der Seite **Masseneinstellungsprojekt** auf **Projekt öffnen** oder **Projekt schließen**, um den Status eines Masseneinstellungsprojekts zu ändern. In der folgenden Tabelle wird erläutert, welche Möglichkeiten Sie im Hinblick auf den Projektstatus haben:

<table>
<thead>
<tr class="header">
<th>Status</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Erstellt</td>
<td>Sie können Informationen erstellen und ändern, können jedoch keine Positionen für das Projekt erstellen. Dies ist der standardmäßige Status von neuen Projekten.</td>
</tr>
<tr class="even">
<td>Geöffnet</td>
<td>Sie können die Projektdetails ändern, Positionen für das Masseneinstellungsprojekt erstellen und Personen für die Positionen einstellen. Dies ist der Status für aktive Projekte.</td>
</tr>
<tr class="odd">
<td>Geschlossen</td>
<td>Sie können dem Projekt keine Positionen hinzufügen. Wenn Sie dem Masseneinstellungsprojekt Positionen hinzufügen möchten, öffnen Sie das Projekt erneut. Dies ist der Status für abgeschlossene Projekte.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Hinweis </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ein Masseneinstellungsprojekt kann erst geschlossen werden, wenn alle Positionen im Projekt entweder den Status "Erstellt" oder den Status "Geschlossen" haben.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 






