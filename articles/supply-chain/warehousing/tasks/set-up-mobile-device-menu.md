---
title: Richten Sie eine Menüoption des mobilen Geräts für das Abschließen der Arbeit von Typ Bestellung
description: In diesem Thema wird gezeigt, wie Sie einen Menüpunkt für mobile Endgeräte einrichten.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10843f9ae9c657df5deae6a1ec11423cc426ba34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976912"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Richten Sie eine Menüoption des mobilen Geräts für das Abschließen der Arbeit von Typ Bestellung

[!include [banner](../../includes/banner.md)]

In diesem Thema wird gezeigt, wie Sie einen Menüpunkt für mobile Endgeräte einrichten. In diesem Beispiel wird das Menüelement für die Ausführung der Arbeit von Typ "Bestellung" verwendet. Die Arbeitsklasse, die dem Menüelement zugeordnet wird, bestimmt, welche Arbeit gültig ist. Sie können diese Anleitung im Demodatenunternehmen USMF ausführen. Normalerweise wird diese Prozedur von einem Lagerortleiter ausgeführt.


## <a name="create-a-mobile-device-menu-item"></a>Erstellen eines Menüelements für ein mobiles Geräts
1. Gehen Sie zu **Menüeinträge für mobile Geräte**, indem Sie sie in der Suchleiste eingeben.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Menüoptionsname** einen Wert ein. Geben Sie einen eindeutigen Wert ein. Sie können z.B. `POMove` eingeben. Beachten Sie den Wert. Sie benötigen ihn später.  
4. Geben Sie im Feld **Titel** einen Wert ein. Dies ist der Titel, der im mobilen Gerät angezeigt wird. Sie können z.B. `PO Move` eingeben.  
5. Wählen Sie im Feld **Modus** **Arbeit**.
6. Wählen Sie **Ja** im Feld **Vorhandene Arbeit verwenden**.
    - Dieses Menüelement für das mobile Gerät wird zur Durchführung von vorhandenen Aufgaben verwendet. Daher müssen Sie diesen Wert auf **Ja** setzen.  
    - Das Feld **Bestandsstatus anzeigen** legt fest, ob der Bestandsstatus des verfügbaren Bestands dem Lagerarbeiter auf dem mobilen Gerät angezeigt wird.  
7. Wählen Sie im Feld **Gerichtet von** **Systemgruppierung**. Wenn Sie im Feld **Gerichtet von** etwas auswählen, erscheinen zusätzliche Felder im Abschnitt **Allgemein** auf dieser Seite. Die Felder, die angezeigt werden, sind davon abhängig, was Sie ausgewählt haben. Wenn Sie **Systemgruppierung** wählen, werden zwei neue Felder hinzugefügt. Diese werden unten erläutert.  
8. Wählen Sie im Feld **Systemgruppierung** **WorkPoolId**. Wenn Lagermitarbeiter dieses Menüelement öffnen, werden sie aufgefordert, eine Arbeitspoolkennung zu scannen. Alle Arbeitsaufträge mit dieser Arbeitspoolkennung und offene Arbeitsauftragspositionen der zu diesem Menüelement hinzugefügten Arbeitsklassen werden an den Benutzer übertragen.  
9. Geben Sie im Feld **Systemgruppierungsbeschriftung** einen Wert ein. Dies ist der Text, der dem Benutzer des mobilen Geräts angezeigt wird. Sie können beispielsweise **Arbeitsplatz** eingeben.  
10. Wählen Sie **Ja** im Feld **Override Kennzeichen während der Eingabe**. Mit dieser Option können Lagermitarbeiter den Ziel-Ladungsträger überschreiben, wenn Artikel auf einem über Ladungsträger gesteuerten Lagerplatz abgelegt werden.  
11. Wählen Sie **Ja** im Feld **Gruppe einlagern**.
    - Wenn alle Einlagerungspositionen des Arbeitsauftrags den selben Lagerplatz haben, erhält der Benutzer eine kombinierte Einlagerungsanweisung für alle Positionen 
    - Überwachungsvorlagenkennung: Eine Arbeitsüberwachungsvorlage ermöglicht es ihnen anzugeben, dass der Arbeitsvorgang für ein Menüelement unterbrochen werden soll damit ein anderer Vorgang durchgeführt werden kann. Wenn beispielsweise dieses Menüelement für eingehende Arbeit ist, kann die Auditvorlage vorschreiben, dass die Arbeitskraft die Temperatur prüft. Der Zeitpunkt, zu dem der Prozess unterbrochen wird, wird auf der Auditvorlage angegeben und kann beispielsweise dann sein, wenn Arbeit gestartet oder abgeschlossen wird oder wenn sich der Status ändert.  
12. Erweitern Sie den Abschnitt **Arbeitsklassen**.
13. Wählen Sie **Neu** aus.
14. Geben Sie im Feld **Arbeitsklassen-ID** `Purchase` ein. Der Arbeitspool schränkt die Arbeit ein, für die das Menüelement verwendet werden kann. In diesem Fall wird es für offenen Arbeitsauftragspositionen verwendet, die die Arbeitsklassenkennung "Einkauf" haben.  
15. Wählen Sie **Speichern**.

## <a name="set-up-work-confirmation"></a>Arbeitsbestätigung einrichten
1. Wählen Sie **Einstellung der Arbeitsbestätigung**.
2. Wählen Sie im Feld **Arbeitsart** **Auswahl**.
3. Aktivieren Sie das Kontrollkästchen **Automatische Bestätigung**. Die Arbeitsanweisung mit dem Arbeitstyp "Entnahme" wird automatisch bestätigt. Diese Anweisung wird dem Benutzer nicht angezeigt.  
4. Wählen Sie **Neu** aus.
5. Wählen Sie im Feld **Arbeitstyp** die Option 'Einlagern'.
6. Aktivieren Sie das Kontrollkästchen **Standortbestätigung**. Der Lagermitarbeiter wird beim Ablegen des Artikels aufgefordert, einen Bestätigungsscan des Lagerortes durchzuführen.  
7. Wählen Sie **Speichern**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Hinzufügen der Menüoption zu einem mobilen Gerät
1. Gehen Sie zum Menü **Mobiles Gerät**, indem Sie es in der Suchleiste eingeben.
2. Wählen Sie **Bearbeiten** aus.
3. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise nach dem Feld **Name** mit dem Wert **Eingang**. Sie suchen das Menü, dass Sie für eingehende Menüelemente verwendet haben. In USMF heißt dies **Eingang**.  
4. Wählen Sie im Baum **einen Wert**.
5. Wählen Sie den Pfeil, der nach rechts zeigt.
6. Wählen Sie **Speichern**.
7. Schließen Sie die Seite.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]