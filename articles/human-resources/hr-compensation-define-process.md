---
title: Vergütungsprozess definieren und Ergebnisse berechnen
description: Vergütungsprozesse werden verwendet, um neue Vergütungsbeträge und Prämien für die Mitarbeiter zu bestimmen, die in einem Plan für feste oder variable Vergütung registriert sind.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 196c907521bba5440f12149abcb2fc446c2aa523
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687050"
---
# <a name="define-compensation-process-and-calculate-results"></a>Vergütungsprozess definieren und Ergebnisse berechnen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vergütungsprozesse werden verwendet, um neue Vergütungsbeträge und Prämien für die Mitarbeiter zu bestimmen, die in einem Plan für feste oder variable Vergütung registriert sind. Vergütungsprozesse können mehrmals ausgeführt werden, um "was wäre wenn"-Analysen auszuführen, um Änderungen und Einstellungen zu überprüfen. Diese Prozedur erstellt einen Vergütungsprozess, führt den Prozess aus und zeigt die Ergebnisse an. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-compensation-process"></a>Einen Vergütungsprozess erstellen
1. Gehen Sie zu **Vergütungsmanagement** > **Prozess** > **Vergütungsprozesse**.
2. Klicken Sie auf **Neuer Vergütungsprozess**.
3. Geben Sie im Feld **Prozess** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie im Feld **Prozesstyp** eine Option aus.
    * Ein Zyklus gibt die Zeitperiode an, die ausgewertet wird, um Vergütung zu bestimmen. Die Beurteilung berücksichtigt, welche Positionen die Mitarbeiter hatten, welche Leistungsbewertungen einbezogen werden, die Berechnung des Prozentsatzes der Beschäftigungszeit des Mitarbeiter während des Zyklus und mehr. Ein Beispiel für das Anfangsdatum des Zyklus könnte das erste Tag des letzten Geschäftsjahrs sein.  
6. Geben Sie im Feld **Anfang des Zyklus** ein Datum ein.
    * Das Enddatum des Zyklus ist wichtig, da es das Datum ist, das verwendet wird, um zu bestimmen, welche Mitarbeiter aktiv beschäftigt und in mindestens einem Vergütungsplan registriert sind.  
7. Geben Sie im Feld **Ende des Zyklus** ein Datum ein.
    * Das aktive Datum für die Buchung ist das Datum, ab dem die neuen Vergütungssätze wirksam werden sollen. Viele Unternehmen lassen mehrere Monate zwischen ihrem Ende eines Zyklus und der Gültig der neuen Vergütungssätze frei. Der Zeitraum wird zur Verarbeitung und zur Prüfung der neuen Vergütung verwendet.  
8. Geben Sie im Feld **Aktives Datum für Buchung** ein Datum ein.
    * Der Zeitpunkt (Datum) wird für die variablen Vergütungspläne verwendet, die den Prämienbetrag eines Mitarbeiters auf der Grundlage ihres jeweiligen Vergütungssatz zu diesem Datum bestimmen.  
    * Die feste Bewertung des Einstellungsdatums wird bei festen Vergütungsplänen mit einer Einstellungsregel von **Prozent** verwendet. Mitarbeiter, die zwischen dem Zyklusanfang und dem Datum in "Fester Lohn (anteilig) auf Basis des Einstellungsdatums" eingestellt werden, erhalten 100 % der berechneten Vergütung.  
9. Geben Sie im Feld **Fester Lohn (anteilig) auf Basis des Einstellungsdatums** ein Datum ein.
    * Der Überprüfungsstichtag ist das Datum, bis zu dem alle Prozessergebnisse geprüft werden sollten, damit sie vor dem aktiven Datum für die Buchung in einen Mitarbeitervergütungsdatensatz geladen werden können. Dieses Feld dient nur zur Information.  
10. Geben Sie im Feld **Stichtag überprüfen** ein Datum ein.
11. Klicken Sie auf **Speichern**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>Legen Sie die Vergütungspläne und Aktionen für einen Vergütungsprozess fest
1. Klicken Sie auf **Einstellungen**.
    * Die Seite **Einrichtung** wird zur Auswahl der im Rahmen dieses Vergütungsprozess zu verarbeitenden Pläne sowie der Aktivitäten für jeden Plan verwendet.  
2. Geben Sie im Feld **Plan** einen Wert ein oder wählen Sie ihn aus.
3. Klicken Sie auf **Speichern**.
4. Klicken Sie auf **Hinzufügen**.
5. Wählen Sie im Feld **Aktivität** einen **Entitätstyp** für die Aktivität aus.
6. Klicken Sie auf **Hinzufügen**.
7. Wählen Sie im Feld **Aktivität** einen **Verdiensttyp** für die Aktivität aus.
    * Vergütungsaktivitäten können mithilfe des Feldes **Vorheriges Ergebnis verwenden** verkettet werden, um anzugeben, ob die ausgewählte Aktivität den Grundlohn der Mitarbeiter oder das Ergebnis der vorherigen Aktivität als Ausgangspunkt für die Berechnung dieser Aktivität verwenden.  
8. Wählen Sie **Ja** im Feld **Vorheriges Ergebnis verwenden**.
9. Klicken Sie auf **Hinzufügen**.
10. Wählen Sie im Feld **Aktivität** einen **allgemeinen Typ** für die Aktivität aus.
    * Verschiedene Vergütungsaktivitätstypen aktivieren verschiedene Felder. Für einen Aktivitätstyp "Allgemeine Vergütung" kann ein Prozentwert oder ein Betrag zur Erhöhung festgelegt werden.  
11. Wählen Sie die Option **Betrag der Erhöhung auswählen** aus.
12. Geben Sie im Feld **Erhöhung (Betrag)** eine Zahl ein.
13. Klicken Sie auf **Hinzufügen**.
14. Wählen Sie im Feld **Aktivität** einen **Aktionstyp** für die Aktivität aus.
    * Die Aktivitätstypen "Beförderung" und "Änderung einer anderen Ebene" ermöglichen die manuelle Anpassung der Mitarbeitervergütung. Für diese Aktivitätstypen können Empfehlungen aktiviert werden. Andere Aktivitätstypen ermöglichen die Eingabe eines neuen empfohlenen Vergütungswertes für einen Mitarbeiter.  
15. Klicken Sie auf **Hinzufügen**.
16. Wählen Sie im Feld **Typ** eine Option aus.
    * Feste und variable Vergütungspläne können im gleichen Vergütungsprozess ausgeführt werden.  
17. Geben Sie im Feld **Plan** einen Wert ein oder wählen Sie ihn aus.
    * Verwenden Sie das Kontrollkästchen **Leistungsbezogene Bezahlung aktivieren**, um festzulegen, ob feste und variable Vergütungsbeträge auf Grundlage der Leistungsbewertung des Mitarbeiters angepasst werden sollen.  
    * Die Hebelwirkung kann für variable Vergütungspläne überschrieben werden.  
18. Klicken Sie auf **Speichern**.
19. Klicken Sie auf **Hinzufügen**.
20. Schließen Sie die Seite.

## <a name="run-the-compensation-process"></a>Ausführen des Vergütungsprozesses
1. Klicken Sie auf **Prozess ausführen**.
    * Mit dem Steuerelement **Ergebnisse der Verarbeitung anzeigen** können Sie Verarbeitungsmeldungen für den gesamten Vergütungsprozess nach der Verarbeitung anzeigen.  
2. Wählen Sie **Ja** aus im Feld **Ergebnisse der Verarbeitung anzeigen**.
3. Klicken Sie auf **OK**.

## <a name="view-the-results"></a>Anzeigen der Ergebnisse
1. Klicken Sie auf **Prozessergebnisse**.
2. Klicken Sie auf **Mitarbeiterergebnisse**.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Erweitern Sie den Abschnitt **Feste Vergütung**.
    * Erweitern Sie die Inforegister, um die Ergebnisse des Prozesses anzuzeigen. Wenn **Aktivieren von Empfehlungen** für eine Vergütungsaktivität markiert war, sind die Felder **Empfehlung** für diese Aktivität aktiviert.  
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Die Ergebnisse für einen einzelnen Mitarbeiter können angezeigt werden, indem auf die Schaltfläche **Ergebnisse anzeigen** klicken.  
    * Sie können den berechneten Vergütungsbetrag überschreiben, indem Sie den Prozentsatz oder den Betrag in den Feldern **Empfehlung** anpassen.  
6. Geben Sie im Feld **Empfohlener Prozentsatz** eine Zahl ein.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Geben Sie im Feld **Empfohlener Prozentsatz** eine Zahl ein.
    * "Neu berechnen" kann verwendet werden, um Änderungen am vorhandenen Datensatz zu ignorieren und ein neues Vergütungsergebnis für den ausgewählten Mitarbeiter zu generieren.  
    * Wenn alle Änderungen für einen Mitarbeiter abgeschlossen sind, ändern Sie den Status in **Genehmigt**.  
9. Klicken Sie auf **Status ändern**.
10. Klicken Sie auf **Genehmigt**.
    * Nachdem der Datensatz genehmigt wurde, kann er in den offiziellen Vergütungsdatensatz des Mitarbeiters geladen werden. Die neue Vergütung ist ab dem Buchungsdatum wirksam, das im Vergütungsprozess festgelegt ist.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
