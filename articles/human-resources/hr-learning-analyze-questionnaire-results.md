---
title: Ergebnisse des Fragebogens analysieren
description: Die Fragebogenstatistiken können verwendet werden, um Durchschnitte, Summen und Prozentsätze basierend auf einer Gruppe von demografischen Daten zu berechnen.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b8e4fd5d9fabd35de067ab61c1e64156ce4f0ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418744"
---
# <a name="analyzing-questionnaire-results"></a>Ergebnisse des Fragebogens analysieren



Die Fragebogenstatistiken können verwendet werden, um Durchschnitte, Summen und Prozentsätze basierend auf einer Gruppe von demografischen Daten zu berechnen. Um diese Prozedur zu starten, gehen Sie zu "Fragebogen" > "Ergebnisse anzeigen und analysieren" > "Fragebogenstatistik". Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-questionnaire-statistics-record"></a>Fragebogenstatistik-Datensatz erstellen
1. Wechseln Sie zu "Fragebogenstatistik".
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Statistik" einen Wert ein.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Klicken Sie im Feld "Fragebogen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie auf die Registerkarte "Allgemein".
    * Wählen Sie, ob anonyme Ergebnisse oder Ergebnisse von Arbeitskräften, von Kontakten und Bewerbern einbezogen werden sollen.  
9. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Arbeitskraft".
    * Wenn Sie die Ergebnisse nach Dienstalter oder Alter anzeigen, geben Sie die Intervalle an, die Sie zum Gruppieren der Ergebnisse verwenden möchten.  
    * Der Wert 5 für das Altersintervall gruppiert die Ergebnisse auf Grundlage von Fünfjahresintervallen.  
10. Geben Sie im Feld "Alter" eine Zahl ein.
    * Aktivieren Sie diese Option, wenn die Berechnung gegen den gesamten Fragebogen, für jede Ergebnisgruppe, für jede Frage oder für jede Fragenzeile ausgeführt werden soll.  
    * Wählen Sie, wie die Ergebnisse gruppiert werden sollen.  
    * Wenn Sie beispielsweise die durchschnittlichen Punkte pro Frage berechnen, möchten Sie, dass die Fragen nach Ergebnisgruppe gruppiert werden.  
    * Wählen Sie die Daten aus, auf denen die Berechnung basieren soll.  
    * Wenn Sie beispielsweise den durchschnittlichen Prozentsatz anzeigen möchten, der auf dem Fragebogen zu den Arbeitskräften für die durchschnittliche Anzahl der Punkte empfangen wird, die über den Arbeitskräften erreicht werden.  
11. Klicken Sie auf die Registerkarte "Bereich".
    * Verwenden Sie Bereiche, um die Ergebnismenge auf die Bereichskriterien einzuschränken.  
12. Klicken Sie auf die Registerkarte "Gruppieren nach".
    * Verwenden Sie Gruppierungen, um zu bestimmen, wie die Ergebnisse angezeigt werden sollen.  
    * Gruppieren Sie z. B. die Ergebnisse zunächst nach Geschlecht und dann nach Alter.  
13. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Verschieben Sie die Gruppierungen auf die Seite "Ausgewählt" und platzieren Sie sie im gewünschten Auftrag.  

## <a name="execute-the-statistics-calculation"></a>Statistikberechnung ausführen
1. Klicken Sie auf "Ausführen".
    * Wählen Sie aus, welche Berechnungsfunktion Sie für die Ergebnisse ausführen möchten.  
    * Berechnen Sie z. B. die durchschnittlichen Prozentsätze zu dem Fragebogen für die ausgewählten Gruppierungen oder summieren Sie die Gesamtpunkte anhand der Ergebnisgruppen für die ausgewählten Gruppierungen.  
2. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Frühere Suchen löschen".
3. Klicken Sie auf "OK".

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Ergebnisse der Fragebogenstatistikausführung anzeigen
1. Klicken Sie auf "Ergebnis".
2. Klicken Sie auf "Ergebnis".
3. Schließen Sie die Seite.

