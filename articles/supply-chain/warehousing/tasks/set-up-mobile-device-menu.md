--- 
title: "Eine Menüoption des mobilen Geräts für das Abschließen der Arbeit in einer Bestellung einrichten"
description: "Diese Prozedur zeigt an, wie ein Menüelement \"Mobiles Gerät\" eingerichtet wird."
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b80c258d6a779a8fc5bb6c846abd3af7e69d5e06
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a>Eine Menüoption des mobilen Geräts für das Abschließen der Arbeit in einer Bestellung einrichten

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt an, wie ein Menüelement "Mobiles Gerät" eingerichtet wird. In diesem Beispiel wird das Menüelement für die Ausführung der Arbeit von Typ "Bestellung" verwendet. Die Arbeitsklasse, die dem Menüelement zugeordnet wird, bestimmt, welche Arbeit gültig ist. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Normalerweise wird diese Prozedur von einem Lagerortleiter ausgeführt.


## <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts
1. Wechseln Sie zu "Menüelemente des mobilen Geräts".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Menüoptionsname" einen Wert ein.
    * Geben Sie einen eindeutigen Wert ein. So können beispielsweise "POMove" eingeben. Beachten Sie den Wert. Sie benötigen ihn später.  
4. Geben Sie im Feld "Titel" einen Wert ein.
    * Dies ist der Titel, der im mobilen Gerät angezeigt wird. So können beispielsweise "PO Move" eingeben.  
5. Wählen Sie im Feld "Modus" "Arbeit"aus.
6. Wählen Sie "Ja" im Feld "Vorhandene Arbeit verwenden".
    * Dieses Menüelement für das mobile Gerät wird zur Durchführung von vorhandenen Aufgaben verwendet. Daher müssen Sie diesen Wert auf "Ja" festlegen.  
    * Das Feld "Bestandsstatus anzeigen" bestimmt, ob der Lagerstatus des verfügbaren Lagerbestands für den Lagermitarbeiter auf dem mobilen Gerät angezeigt wird.  
7. Wählen Sie im Feld "Geleitet von" "Systemgruppierung" aus.
    * Wenn Sie etwas im Feld "Geleitet von" auswählen, werden zusätzliche Felder im Abschnitt "Allgemein" auf dieser Seite angezeigt. Die Felder, die angezeigt werden, sind davon abhängig, was Sie ausgewählt haben. Bei Auswahl von Systemgruppierung werden zwei neue Felder hinzugefügt. Diese werden unten erläutert.  
8. Wählen Sie im Feld "Systemgruppierung" die Option "WorkPoolId" aus.
    * Wenn Lagermitarbeiter dieses Menüelement öffnen, werden sie aufgefordert, eine Arbeitspoolkennung zu scannen. Alle Arbeitsaufträge mit dieser Arbeitspoolkennung und offene Arbeitsauftragspositionen der zu diesem Menüelement hinzugefügten Arbeitsklassen werden an den Benutzer übertragen.  
9. Geben Sie im Feld "Systemgruppierungsbezeichnung" einen Wert ein.
    * Dies ist der Text, der dem Benutzer des mobilen Geräts angezeigt wird. So können beispielsweise "Work pool" eingeben.  
10. Wählen Sie "Ja" im Feld "Kennzeichen bei Einlagerung überschreiben" aus.
    * Mit dieser Option können Lagermitarbeiter den Ziel-Ladungsträger überschreiben, wenn Artikel auf einem über Ladungsträger gesteuerten Lagerplatz abgelegt werden.  
11. Wählen Sie "Ja "im Feld "Gruppeneinlagerung" aus.
    * Wenn alle Einlagerungspositionen des Arbeitsauftrags den selben Lagerplatz haben, erhält der Benutzer eine kombinierte Einlagerungsanweisung für alle Positionen  
    * Überwachungsvorlagenkennung: Eine Arbeitsüberwachungsvorlage ermöglicht es ihnen anzugeben, dass der Arbeitsvorgang für ein Menüelement unterbrochen werden soll damit ein anderer Vorgang durchgeführt werden kann. Wenn beispielsweise dieses Menüelement für eingehende Arbeit ist, kann die Auditvorlage vorschreiben, dass die Arbeitskraft die Temperatur prüft. Der Zeitpunkt, zu dem der Prozess unterbrochen wird, wird auf der Auditvorlage angegeben und kann beispielsweise dann sein, wenn Arbeit gestartet oder abgeschlossen wird oder wenn sich der Status ändert.  
12. Erweitern Sie den Abschnitt "Arbeitsklassen".
13. Klicken Sie auf "Neu".
14. Geben Sie im Feld "Arbeitsklassen-ID" die Bezeichnung "Bestellung" ein.
    * Der Arbeitspool schränkt die Arbeit ein, für die das Menüelement verwendet werden kann. In diesem Fall wird es für offenen Arbeitsauftragspositionen verwendet, die die Arbeitsklassenkennung "Einkauf" haben.  
15. Klicken Sie auf "Speichern".

## <a name="set-up-work-confirmation"></a>Arbeitsbestätigung einrichten
1. Klicken Sie auf "Einrichtung Arbeitsbestätigung".
2. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
3. Aktivieren Sie das Kontrollkästchen "Automatisch bestätigen".
    * Die Arbeitsanweisung mit dem Arbeitstyp "Entnahme" wird automatisch bestätigt. Diese Anweisung wird dem Benutzer nicht angezeigt.  
4. Klicken Sie auf "Neu".
5. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
6. Aktivieren Sie das Kontrollkästchen "Lagerplatzbestätigung".
    * Der Lagermitarbeiter wird beim Ablegen des Artikels aufgefordert, einen Bestätigungsscan des Lagerortes durchzuführen.  
7. Klicken Sie auf "Speichern".
8. Schließen Sie die Seite.
9. Schließen Sie die Seite.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Hinzufügen der Menüoption zu einem mobilen Gerät
1. Wechseln Sie zu "Menü für mobiles Gerät".
2. Klicken Sie auf "Bearbeiten".
3. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Name" mit dem Wert "eingehend".
    * Sie suchen das Menü, dass Sie für eingehende Menüelemente verwendet haben. In USMF heißt es "Inbound".  
4. Wählen Sie in der Struktur "ein Wert".
5. Klicken Sie auf den Pfeil nach rechts.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.


