---
title: Vergütungsprozess definieren und Ergebnisse berechnen
description: Vergütungsprozesse werden verwendet, um neue Vergütungsbeträge und Prämien für die Mitarbeiter zu bestimmen, die in einem Plan für feste oder variable Vergütung registriert sind.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e5b0bb5558a8b71d02b5988c6f82f53f4f42646
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "325732"
---
# <a name="define-compensation-process-and-calculate-results"></a>Vergütungsprozess definieren und Ergebnisse berechnen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vergütungsprozesse werden verwendet, um neue Vergütungsbeträge und Prämien für die Mitarbeiter zu bestimmen, die in einem Plan für feste oder variable Vergütung registriert sind. Vergütungsprozesse können mehrmals ausgeführt werden, um "was wäre wenn"-Analysen auszuführen, um Änderungen und Einstellungen zu überprüfen. Diese Prozedur erstellt einen Vergütungsprozess, führt den Prozess aus und zeigt die Ergebnisse an. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-compensation-process"></a>Einen Vergütungsprozess erstellen
1. Wechseln Sie zu Personalverwaltung > Vergütung > Prozess > Vergütungsprozesse.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Prozess" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Prozesstyp" eine Option aus.
    * Ein Zyklus gibt die Zeitperiode an, die ausgewertet wird, um Vergütung zu bestimmen. Die Beurteilung berücksichtigt, welche Positionen die Mitarbeiter hatten, welche Leistungsbewertungen einbezogen werden, die Berechnung des Prozentsatzes der Beschäftigungszeit des Mitarbeiter während des Zyklus und mehr. Ein Beispiel für das Anfangsdatum des Zyklus könnte das erste Tag des letzten Geschäftsjahrs sein.  
6. Geben Sie im Feld "Anfang des Zyklus"ein Datum ein.
    * Das Enddatum des Zyklus ist wichtig, da es das Datum ist, das verwendet wird, um zu bestimmen, welche Mitarbeiter aktiv beschäftigt und in mindestens einem Vergütungsplan registriert sind.  
7. Geben Sie im Feld "Ende des Zyklus"ein Datum ein.
    * Das aktive Datum für die Buchung ist das Datum, ab dem die neuen Vergütungssätze wirksam werden sollen. Viele Unternehmen lassen mehrere Monate zwischen ihrem Ende eines Zyklus und der Gültig der neuen Vergütungssätze frei. Der Zeitraum wird zur Verarbeitung und zur Prüfung der neuen Vergütung verwendet.  
8. Geben Sie im Feld "Aktives Datum für Buchung" ein Datum ein.
    * Der Zeitpunkt (Datum) wird für die variablen Vergütungspläne verwendet, die den Prämienbetrag eines Mitarbeiters auf der Grundlage ihres jeweiligen Vergütungssatz zu diesem Datum bestimmen.  
    * Der Wert "Fester Lohn (anteilig) auf Basis des Einstellungsdatums" wird mit festen Vergütungsplänen mit einer Einstellungsregel nach Prozent verwendet.  Mitarbeiter, die zwischen dem Zyklusanfang und dem Datum in "Fester Lohn (anteilig) auf Basis des Einstellungsdatums" eingestellt werden, erhalten 100 % der berechneten Vergütung.  
9. Geben Sie im Feld "Fester Lohn (anteilig) auf Basis des Einstellungsdatums" ein Datum ein.
    * Der Überprüfungsstichtag ist das Datum, bis zu dem alle Prozessergebnisse geprüft werden sollten, damit sie vor dem aktiven Datum für die Buchung in einen Mitarbeitervergütungsdatensatz geladen werden können. Dieses Feld dient nur zur Information.  
10. Geben Sie im Feld "Stichtag überprüfen" ein Datum ein.
11. Klicken Sie auf "Speichern".

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a>Einrichten der Vergütungspläne und Aktivitäten für einen Vergütungsprozess
1. Klicken Sie auf Einstellungen.
    * Die Seite "Einrichtung" wird zur Auswahl der im Rahmen dieses Vergütungsprozess zu verarbeitenden Pläne sowie der Aktivitäten für jeden Plan verwendet.  
2. Geben Sie im Feld "Plan" einen Wert ein, oder wählen Sie einen Wert aus.
3. Klicken Sie auf "Speichern".
4. Klicken Sie auf Hinzufügen.
5. Wählen Sie im Feld "Aktivität" einen Entitätstyp für die Aktivität aus.
6. Klicken Sie auf Hinzufügen.
7. Wählen Sie im Feld "Aktivität" einen Verdiensttyp für die Aktivität aus.
    * Vergütungsaktivitäten können mithilfe des Feldes "Vorheriges Ergebnis verwenden" verkettet werden, um anzugeben, ob die ausgewählte Aktivität den Grundlohn der Mitarbeiter oder das Ergebnis der vorherigen Aktivität als Ausgangspunkt für die Berechnung dieser Aktivität verwenden.  
8. Wählen Sie "Ja" im Feld "Vorheriges Ergebnis verwenden".
9. Klicken Sie auf Hinzufügen.
10. Wählen Sie im Feld "Aktivität" einen allgemeinen Typ für die Aktivität aus.
    * Verschiedene Vergütungsaktivitätstypen aktivieren verschiedene Felder. Für einen Aktivitätstyp "Allgemeine Vergütung" kann ein Prozentwert oder ein Betrag zur Erhöhung festgelegt werden.  
11. Wählen Sie die Option "Betrag der Erhöhung auswählen" aus.
12. Geben Sie im Feld "Erhöhung (Betrag)" eine Zahl ein.
13. Klicken Sie auf Hinzufügen.
14. Wählen Sie im Feld "Aktivität" einen Aktionstyp für die Aktivität aus.
    * Die Aktivitätstypen "Beförderung" und "Änderung einer anderen Ebene" ermöglichen die manuelle Anpassung der Mitarbeitervergütung. Für diese Aktivitätstypen können Empfehlungen aktiviert werden. Andere Aktivitätstypen ermöglichen die Eingabe eines neuen empfohlenen Vergütungswertes für einen Mitarbeiter.  
15. Klicken Sie auf Hinzufügen.
16. Wählen Sie im Feld "Typ" eine Option aus.
    * Feste und variable Vergütungspläne können im gleichen Vergütungsprozess ausgeführt werden.  
17. Geben Sie im Feld "Plan" einen Wert ein, oder wählen Sie einen Wert aus.
    * Verwenden Sie das Kontrollkästchen "Leistungsbezogene Bezahlung aktivieren", um festzulegen, ob feste und variable Vergütungsbeträge auf Grundlage der Leistungsbewertung des Mitarbeiters angepasst werden sollen.  
    * Die Hebelwirkung kann für variable Vergütungspläne überschrieben werden.  
18. Klicken Sie auf "Speichern".
19. Klicken Sie auf Hinzufügen.
20. Schließen Sie die Seite.

## <a name="run-the-compensation-process"></a>Ausführen des Vergütungsprozesses
1. Klicken Sie auf "Prozess ausführen".
    * Mit dem Steuerelement "Ergebnisse der Verarbeitung anzeigen" können Sie Verarbeitungsmeldungen für den gesamten Vergütungsprozess nach der Verarbeitung anzeigen.  
2. Wählen Sie "Ja" im Feld "Ergebnisse der Verarbeitung anzeigen" aus.
3. Klicken Sie auf "OK".

## <a name="view-the-results"></a>Anzeigen der Ergebnisse
1. Klicken Sie auf "Prozessergebnisse".
2. Klicken Sie auf "Mitarbeiterergebnisse".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Erweitern Sie den Bereich "Feste Vergütung".
    * Erweitern Sie die Inforegister, um die Ergebnisse des Prozesses anzuzeigen. Wenn "Aktivieren von Empfehlungen" für eine Vergütungsaktivität markiert war, sind die Felder "Empfehlung" für diese Aktivität aktiviert.  
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Ergebnisse für einen einzelnen Mitarbeiter können angezeigt werden, indem auf die Schaltfläche "Ergebnisse anzeigen" klicken.  
    * Sie können den berechneten Vergütungsbetrag überschreiben, indem Sie den Prozentsatz oder den Betrag in den Feldern "Empfehlungsg" anpassen.  
6. Geben Sie im Feld "Empfohlener Prozentsatz" eine Zahl ein.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Geben Sie im Feld "Empfohlener Prozentsatz" eine Zahl ein.
    * "Neu berechnen" kann verwendet werden, um Änderungen am vorhandenen Datensatz zu ignorieren und ein neues Vergütungsergebnis für den ausgewählten Mitarbeiter zu generieren.  
    * Wenn alle Änderungen für einen Mitarbeiter abgeschlossen sind, ändern Sie den Status in "Genehmigt".  
9. Klicken Sie auf "Status ändern".
10. Klicken Sie auf "Genehmigt".
    * Nachdem der Datensatz genehmigt wurde, kann er in den offiziellen Vergütungsdatensatz des Mitarbeiters geladen werden. Die neue Vergütung ist ab dem Buchungsdatum wirksam, das im Vergütungsprozess festgelegt ist.  

