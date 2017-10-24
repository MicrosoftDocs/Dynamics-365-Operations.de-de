--- 
title: "Einen Min-Max-Auffüllungsprozess einrichten"
description: "Diese Prozedur zeigt Ihnen an, wie ein neuer Auffüllungsprozess eingerichtet wird, der die Min./Max.-Auffüllungsstrategie verwendet."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a>Einen Min-Max-Auffüllungsprozess einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen an, wie ein neuer Auffüllungsprozess eingerichtet wird, der die Min./Max.-Auffüllungsstrategie verwendet. Wenn Lagerbestand unter der Untergrenze liegt, wird Arbeit erstellt, um den Lagerplatz aufzufüllen. Die Prozedur zeigt auch, wie feste Entnahmeorte verwendet werden, um die Lagerauffüllung zuzulassen, selbst wenn der Lagerbestand unter die Untergrenze sinkt und wie der Auffüllungsprozess aktiviert wird, um mithilfe eines Batchauftrags regelmäßig ausgeführt zu werden. Diese Aufgaben werden normalerweise von einem Lagerortleiter ausgeführt. Sie können diese Prozedur im USMF-Demodatunternehmen ausführen, unter Verwendung der Beispielswerte in den Hinweisen, oder Sie können sie mit Ihren eigenen Daten ausführen. Wenn Sie Ihre eigenen Daten verwenden, stellen Sie sicher, dass Sie einen Lagerort haben, der für Lagerortverwaltungsprozesse aktiviert ist.


## <a name="create-a-fixed-picking-location"></a>Erstellen Sie einen festen Entnahmeort
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerort" > "Feste Lagerplätze".
    * Dies ist eine optionale Aufgabe für Min./Max.-Auffüllung, aber wenn Sie feste Entnahmeorte verwenden, ermöglicht dies das Auffüllen des Bestands, selbst wenn es unterhalb des minimalen Niveaus fällt, da das System bestimmen kann, welche Artikel aufgefüllt werden müssen, selbst wenn keine mehr übrig sind.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie Artikel A0001 auswählen.  
4. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "Standort 2" auswählen.  
5. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie Lagerort 24 auswählen.  
6. Geben Sie im Feld "Lagerplatz" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "CP-003" auswählen.  
7. Schließen Sie die Seite.

## <a name="create-a-replenishment-location-directive"></a>Erstellen Sie eine Auffüllungslagerplatz-Anweisung
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortparameter".
    * Lagerplatzanweisungen werden verwendet, um zu bestimmen, von wo Artikel im Auffüllungsprozess entnommen werden sollen.  
2. Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Auffüllung" aus.
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Name" einen Wert ein.
5. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
6. Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie "Standort 2" auswählen.  
7. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie Lagerort 24 auswählen.  
8. Klicken Sie auf "Speichern".
9. Klicken Sie auf "Neu".
10. Markieren Sie in der Liste die ausgewählte Zeile.
11. Geben Sie im Feld "Nach Menge" eine Zahl ein.
    * Beispielweise können Sie es auf 9999 festlegen.  
12. Aktivieren Sie das Kontrollkästchen "Teilung zulassen".
    * Wenn Sie diese Option auswählen, ermöglicht es der Arbeitserstellungsprozess, dass die Arbeitspositionsmengen über mehrere Lagerplätze verteilt werden.  
13. Klicken Sie auf "Speichern".
14. Klicken Sie auf "Neu".
15. Markieren Sie in der Liste die ausgewählte Zeile.
16. Geben Sie im Feld "Name" einen Wert ein.
17. Klicken Sie auf "Speichern".
18. (Zum Bearbeiten klicken)
    * Sie können diese Abfrage bearbeiten, um Einschränkungen hinzuzufügen, bei denen der Bestand innerhalb des Auffüllungsprozesses ausgewählt werden kann. Beispielsweise kann es sein, dass Bestand nur aus dem Sammelbereich des Lagerorts verwendet werden soll.  
19. Klicken Sie auf "OK".
20. Schließen Sie die Seite.

## <a name="create-a-replenishment-work-template"></a>Erstellen Sie eine Auffüllungs-Arbeitsvorlage
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsvorlagen".
    * Diese Arbeitsvorlage wird verwendet, um das System darin zu führen, wie die Min./Max.-Auffüllungsarbeit erstellt werden muss. Als Minimum muss es eine Arbeitsvorlagenposition für eine Entnahme und eine Einlagerung geben. Die Arbeitsvorlage weist darauf hin, dass sie "Ungültig" ist, bis die gesamten erforderlichen Informationen ausgefüllt wurden.  
2. Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Auffüllung" aus.
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Arbeitsvorlage" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie auf "Neu".
7. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
8. Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein, oder wählen Sie einen Wert aus.
    * Diese sollte eine Arbeitsklasse sein, die der Auffüllung zugeordnet ist. Wenn Sie USMF erwenden, wählen Sie "Auffüllen" aus.  
9. Klicken Sie auf "Neu".
10. Markieren Sie in der Liste die ausgewählte Zeile.
11. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
12. Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein, oder wählen Sie einen Wert aus.
13. Klicken Sie auf "Speichern".
14. Schließen Sie die Seite.

## <a name="create-a-new-replenishment-template"></a>Erstellen Sie eine neue Auffüllungsvorlage
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Wiederbeschaffung" > "Wiederbeschaffungsvorlagen".
    * Die Auffüllungsvorlage wird verwendet, um die Artikel und Mengen sowie den aufzufüllenden Lagerplatz zu definieren.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Auffüllungsvorlage" einen Wert ein.
    * Geben Sie der Vorlage einen Namen, um anzugeben, dass sie für die Min./Max.-Auffüllung ist.  
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Aktivieren Sie das Kontrollkästchen "Zulassen, dass Wellenanforderung nicht reservierte Mengen verwendet".
    * Wenn Sie diese Option auswählen, wird die Wellenbedarfsauffüllung aktiviert, um Mengen zu verbrauchen, die der Min./Max.-Auffüllung zugeordnet sind. Beispielsweise kann dies hilfreich, wenn die Min./Max.-Auffüllungsarbeit nicht sofort verarbeitet wird, um zu verhindern, dass unnötige Bedarfsauffüllungsarbeit erstellt wird.  
6. Klicken Sie auf "Neu".
7. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Markieren Sie in der Liste die ausgewählte Zeile.
10. Geben Sie im Feld "Auffüllungseinheit" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie beispielsweise Stck. aus. Diese Einstellung ist obligatorisch. Sie ermöglicht es Ihnen, eine andere Maßeinheit für die Auffüllungsarbeit anzugeben im Vergleich zur Einheit, die für die minimalen und maximalen Lagerbestände in dieser Vorlage angegeben ist.  
11. Geben Sie im Feld "Arbeitsvorlage" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die Arbeitsvorlage aus, die Sie zuvor erstellt haben.  
12. Geben Sie im Feld "Mindestmenge" eine Zahl ein.
    * Wählen Sie die Mindestmenge aus, die die Auffüllung auslösen soll. Legen Sie diese beispielsweise auf 50 fest. Es ist möglich, diese auf null zu belassen, wenn Sie einen festen Lagerplatz auffüllen und die Option "Leere feste Lagerplätze auffüllen" auf "Ja" festgelegt ist. Außerdem wird empfohlen, dass Sie die Option "Nur feste Lagerplätze auffüllen" aus Leistungsgründen auswählen.  
13. Geben Sie im Feld "Höchstmenge" eine Zahl ein.
    * Legen Sie diese beispielsweise auf 100 fest.  
14. Geben Sie im Feld 'Einheit' einen Wert ein, oder wählen Sie einen Wert aus.
    * Weisen Sie die Einheit für die Mindest- und Höchstmengen zu. Legen Sie diese beispielsweise auf Stck. fest.  
15. Aktivieren Sie das Kontrollkästchen "Leere feste Lagerplätze auffüllen".
    * Aktivieren Sie dieses Kontrollkästchen, um feste Lagerplätze aufzufüllen, wenn sie leer sind. Andernfalls wird nur die Lagerplätze, in denen es eine verfügbare Menge gibt, aufgefüllt.  
16. Aktivieren Sie das Kontrollkästchen "Nur leere feste Lagerplätze auffüllen".
17. Klicken Sie auf "Produkte auswählen".
    * Dies ist die Stelle, an der definiert wird, welche Produkte aufgefüllt werden sollten. Wenn die Option "Feste Entnahmeorte" aktiviert ist, müssen Sie auch die Lagerplätze in dieser Abfrage definieren. Variantenspezifische Abfragen sind verfügbar, sowie auch produktspezifische Abfragen.  
18. Wählen Sie die Zeile "Artikel" aus.
19. Geben Sie im Feld "Kriterien" einen Wert ein.
    * Wählen Sie die Artikel aus, die an den festen Lagerplätzen aufgefüllt werden sollen. Geben Sie beispielsweise A* ein, um alle Artikelnummern auszuwählen, die mit A beginnen.  
20. Klicken Sie auf Hinzufügen.
    * Fügen Sie die Entität "Lagerplatz" (es sei denn, dass sie bereits vorhanden ist) hinzu, um die Auffüllungsarbeit auf die festen Entnahmeorte innerhalb eines bestimmten Bereichs des Lagerorts einzuschränken.  
21. Markieren Sie in der Liste die ausgewählte Zeile.
22. Legen Sie das Feld "Tabelle" auf "Lagerplätze" fest.
23. Wählen Sie im Feld "Feld" die Option "Lagerortprofilkennung" aus.
24. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
25. Klicken Sie auf "OK".
26. Schließen Sie die Seite.

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a>Legen Sie fest, dass der Auffüllungsprozess als Batchauftrag ausgeführt wird
1. Wechseln Sie zu "Lagerortverwaltung" > "Wiederbeschaffung" > "Wiederbeschaffen".
    * Die Seite "Auffüllungen" ermöglicht es Ihnen festzulegen, dass Auffüllung als Batchauftrag ausgeführt wird oder festzulegen, dass sie manuell gestartet wird.  
2. Klicken Sie auf "Filter".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
5. Klicken Sie auf "OK".
6. Erweitern Sie den Abschnitt "Ausführen im Hintergrund".
7. Legen Sie Option "Stapelverarbeitung" auf "Ja" fest.
8. Klicken Sie auf "Wiederholung".
9. Wählen Sie die Option "Kein Enddatum" aus.
10. Legen Sie das Wiederholungsmuster fest.
    * Wählen Sie beispielsweise "Tage" aus.  
11. Klicken Sie auf "OK".
12. Klicken Sie auf "OK".


