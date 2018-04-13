--- 
title: "Arbeitsvorlage für Bestellungen einrichten"
description: Ziel dieser Prozedur ist es, eine einfache Arbeitsvorlage einzurichten, die verwendet wird, wenn empfangene Artikel eingelagert werden sollen.
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Arbeitsvorlage für Bestellungen einrichten

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ziel dieser Prozedur ist es, eine einfache Arbeitsvorlage einzurichten, die verwendet wird, wenn empfangene Artikel eingelagert werden sollen. Arbeitsvorlagen bestimmen die Sammlung von Anweisungen, die dem Lagerarbeiter auf einem mobilen Gerät dargestellt wird, wenn Artikel aus dem Wareneingangsbereich umgelagert werden. Sie können diese Prozedur mit dem Daten des Demodatenunternehmen USMF oder mit eigenen Daten verwenden. Bevor Sie dieses Handbuch starten, erstellen Sie eine Arbeitspool-ID. In diesem Beispiel wird eine Arbeitspool-ID mit der Bezeichnung "Eingehend" verwendet. Diese Prozedur ist für die Lagerverwaltung vorgesehen.

1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsvorlagen".
2. Wählen Sie im Feld "Standardauftragstyp" die Option "Bestellung" aus.

## <a name="create-a-work-template-header"></a>Kopfzeile der Arbeitsvorlage erstellen
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
    * Dies ist die Sequenz, in der die Arbeitsvorlagen ausgewertet werden. Sie können die Reihenfolge bei Bedarf ändern.  
3. Geben Sie im Feld "Arbeitsvorlage" einen Wert ein.
    * Dies ist eindeutige Bezeichner für die Vorlage.  
4. Geben Sie im Feld "Arbeitsvorlagenbeschreibung" einen Wert ein.
    * Die Option "Gültig" wird nicht aktiviert, bis Sie alle Informationen, die für die Vorlage erforderlich sind, angegeben und gespeichert haben.  
    * Ein Arbeitsauftrag vom Typ "Bestellung" kann nicht automatisch verarbeitet werden, daher legen Sie die Option "Automatisch verarbeiten" auf "Nein" fest.  
5. Geben Sie im Feld "Arbeitspool-ID" einen Wert ein.
    * Mithilfe der Arbeitspool-IDs können Sie die Arbeit in Gruppen organisieren. Der Wert, der hier festgelegt ist, ist der Standardwert für jede Arbeit, die anhand dieser Vorlage erstellt wird.  
6. Geben Sie im Feld "Arbeitspriorität" 1 ein.
    * Dadurch wird die Wichtigkeit der Arbeit angegeben. Der hier festgelegte Wert wird als Standard für jede Arbeit festgelegt, die anhand dieser Vorlage erstellt wird.  
7. Klicken Sie auf "Speichern".
    * Sie müssen die Kopfzeile der Arbeitsvorlagen speichern, damit die Schaltfläche "Abfrage bearbeiten" verfügbar ist.  

## <a name="set-up-the-query-for-the-work-template"></a>Abfrage für Arbeitsvorlage erstellen
1. (Zum Bearbeiten klicken)
    * Wir legen eine Einschränkung fest, damit die Vorlage nur innerhalb eines bestimmten Lagerorts verwendet werden kann.  
2. Klicken Sie auf Hinzufügen.
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Lagerort" einen Wert ein.
5. Geben Sie im Feld "Kriterien" einen Wert ein.
6. Klicken Sie auf "OK".
7. Klicken Sie auf "Ja".

## <a name="set-work-template-details"></a>Arbeitsvorlagendetails einrichten
1. Klicken Sie auf "Neu".
2. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
3. Geben Sie im Feld "Arbeitsklassen-ID" einen Wert ein.
    * Die hier festgelegte Arbeitsklasse ist der Standard für alle Arbeitspositionen vom Typ "Entnahme", die anhand dieser Vorlage erstellt werden. Die Arbeitsklasse kann nicht von den Arbeitsauftragspositionen überschrieben werden. Arbeitsklassen werden verwendet, um den Typ der Arbeitsauftragspositionen zuzuweisen und/oder einzuschränken, die ein Lagerarbeiter auf einem mobilen Gerät verarbeiten kann.  
4. Klicken Sie auf "Neu".
5. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
6. Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein.
    * Die Entnahme- und Einlagerungsanweisungen sind ein Satz. Jede Entnahme/Einlagerung muss dieselbe Arbeitsklasse aufweisen. Verwenden Sie die gleiche Arbeitsklasse, die Sie für die Entnahmeanweisung angegeben haben.  
7. Klicken Sie auf "Speichern".
    * Beachten Sie, dass das Kontrollkästchen "Gültig" nun aktiviert ist.  


