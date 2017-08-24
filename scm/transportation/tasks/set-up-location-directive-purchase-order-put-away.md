--- 
title: "Lagerplatzdirektive für Bestellungseinlagerung einrichten"
description: Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird.
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4c2456fffd9a010728154749b35c58db13f142bb
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Lagerplatzdirektive für Bestellungseinlagerung einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen an, wie ein Satzmaster eingerichtet wird. Das Beispiel, das angezeigt wird, erstellt, um zu bestimmen, wo sich verwendet werden Lagerplatzdirektive, Artikel führt, die für eine Bestellung eingegangen sind. Sie können diese Prozedur mit dem Daten des Demodatenunternehmen USMF oder mit eigenen Daten verwenden. Vorbedingungen: Sie müssen einen Dispositionscode erstellen. In diesem Schritt verwenden Sie einen aufgerufenen Dispositionscode neu bezeichnen. Wenn Sie Lagerplatzdirektive in eigene Daten erstellen, müssen Sie einrichten erweiterte Lagerortverwaltung für den aktuellen Lagerort und Artikel verwenden.  Diese Prozedur ist für die Lagerverwaltung vorgesehen.

1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortparameter".
2. Wählen Sie im Feld "Standardauftragstyp" die Option "Bestellung" aus.

## <a name="create-a-location-directive-header"></a>Erstellen einer Lagerplatzrichtlinie
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
    * Geben Sie die Reihenfolge ein, in der der Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge, falls notwendig, auch ändern.  
3. Geben Sie im Feld "Name" einen Wert ein.
    * Dies ist eindeutige Bezeichner für die Vorlage.  
4. Wählen Sie im Feld "Arbeitstyp" die Option "Entnahme" aus.
    * Wählen Sie die Art der auszuführenden Arbeit aus. Für um mit Arbeitsauftragstyp Bestellung, ist Put einziger unterstützter Wert.  
5. Geben Sie im Feld "Standort" einen Wert ein.
6. Geben Sie im Feld "Lagerort" einen Wert ein.
    * Lassen Sie das richtungweisende Codeleerzeichen.  Richtungweisende Codes werden verwendet, um eine Arbeitsauftragsposition des Typs zu verknüpfen platziert zu bestimmten Direktiven. Für Bestellungen wird der Lagerplatz der letzten Arbeitsauftragsposition des Typs Put aufgelöst, bevor die Arbeitsvorlage bestimmt wird. Daher ist es nicht möglich, die letzte Zeile einer Arbeitsvorlage in bestimmten Es herzustellen.   
7. Geben Sie im Feld "Bereitstellungscode" einen Wert ein.
    * Der Dispositionscode schränkt die Verwendung von den Lagerplatzdirektiven ein, damit werden die Lagerplatzdirektive nur verwendet, wenn der Lagerarbeiter diesen bestimmten Wert bei der Erfassung des Artikels mithilfe eines mobilen Geräts eingibt.  
8. Klicken Sie auf "Speichern".

## <a name="edit-the-query-for-directive"></a>Abfrage für zu entfernende Ausreißer bearbeiten
1. (Zum Bearbeiten klicken)
    * Die Verwendung von diesen Direktiven ist bereits beschränkt, für die Artikel verwendet werden, die im Lagerort erfasst werden, den angegebenen und mit dem diesem Dispositionscode Sie angegeben haben. Sie können weitere Einschränkungen mithilfe der Abfrage hinzufügen.  
2. Klicken Sie auf "OK".

## <a name="add-directive-lines"></a>Lagerplatzrichtlinienpositionen hinzufügen
1. Klicken Sie auf "Neu".
    * Geben Sie die Reihenfolge ein, in der der Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge, falls notwendig, auch ändern.  
2. Geben Sie im Feld "Nach Menge" eine Zahl ein.
    * Dies ist das in geringer Menge, die für diese richtungweisende Position gültig ist.  
3. Geben Sie im Feld "Nach Menge" eine Zahl ein.
4. Geben Sie im Feld "Einheiten" einen Wert ein.
    * Die Einheit, die von der Menge sowie der Menge ist, wird die Quellensteuer ausgedrückt. Wenn Sie dieses Feld leer lassen, wird die Lagereinheit des Artikels verwendet.  
5. Wählen Sie im Feld Menge suchen eine Option aus.
    * Kein oder Lizenz-Kennzeichen-Menge: Die erfasste Menge auf jeder jeder Lizenzmenge. Unitized Menge: Die gesamte Menge, die erfasst wird. Die noch zu empfangende Menge, die in der Bestellposition angegeben ist. Die Gesamtmenge, die in der Bestellposition angegeben ist.  
6. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Menge initialisieren".
    * Wenn Sie diese Option auswählen und die Einheit im Eingeschränkte nach Einheitsseite angeben, nur Artikel mit dieser Maßeinheit in den Lagerplatz eingelagert werden können. Wenn beispielsweise die Maßeinheit Paletten ist, können Artikel auf Paletten an einem bestimmten Lagerplatz eingelagert werden.  
7. Aktivieren oder deaktivieren Sie das Kontrollkästchen ''.
    * Aktivieren Sie dieses Kontrollkästchen, um die Menge über mehrere Lagerplätze aufzuteilen.  
8. Klicken Sie auf "Speichern".

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Beschränken Sie die richtungweisende Position zu einer bestimmten Einheit ein
1. Nach Einheit einschränken.
    * Diese Schaltfläche ist nur verfügbar, wenn Sie Speichern drücken, nachdem Sie das Kontrollkästchen "Nach Einheit einschränken" aktiviert haben.  
2. Geben Sie im Feld "Einheiten" einen Wert ein.
3. Schließen Sie die Seite.

## <a name="add-a-location-directive-action-line"></a>Richtlinienpositionsaktivität für Lagerplätze an Lagerorten
1. Klicken Sie auf "Neu".
    * Geben Sie die Reihenfolge ein, in der der Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge, falls notwendig, auch ändern.  
2. Geben Sie im Feld "Name" einen Wert ein.
    * Dies ist eindeutige Bezeichner für die Vorlage.  
3. Wählen Sie im Feld fester Lagerplatz eine Option aus.
    * Feste und nicht-korrigierte Lagerplätze: Alle nicht-korrigierten Lagerplätze sind sowie der eigene feste Lagerplatz des Produkts, innerhalb des Bereichs gültig, der in der Abfrage angegeben ist.  Nur fester Ort für das Produkt: Feste Lagerplätze für das Produkt gültig sind, und alle Produktvarianten geben die gleiche Gruppe von festen Lagerplätzen frei. Nur fester Lagerplatz für die Produktvarianten: Nur die festen Lagerplätze, die für jede Produktvariante angegeben werden, gültig sind.  
4. Wählen Sie im Feld Strategie eine Option aus.
    * Arbeitsaufträge vom Typ Bestellung unterstützen die folgenden Strategien: Kein: der Artikel wird am ersten Lagerplatz platziert, der gefunden wird. Führen Sie: Der Artikel wird an einen Speicherort installiert, in dem ähnliche Artikel bereits verfügbar sind. Leerer Lagerplatz ohne eingehende Arbeit: der Artikel wird im ersten leeren Speicherort installiert, der gefunden wird. Der Lagerplatz wird als leer angesehen, wenn dieser keinen physischen Bestand und keine erwartete eingehende Arbeit hat.  
5. Klicken Sie auf "Speichern".

## <a name="edit-the-query-for-directive-action-line"></a>Abfrage für zu entfernende Ausreißer bearbeiten
1. (Zum Bearbeiten klicken)
2. Klicken Sie auf Hinzufügen.
3. Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.
    * In diesem Beispiel schränken wir die möglichen Lagerplätze mithilfe einer Lagerplatzprofil Kennung ein.  
4. Geben Sie im Feld "Kriterien" einen Wert ein.
5. Klicken Sie auf "OK".
    * Sie können fortfahren, um richtungweisende Positionen und richtungweisende Aktivitäten hinzuzufügen, bis Sie alle möglichen Szenarien am Lagerort abgedeckt haben.  


