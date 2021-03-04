---
title: Lagerplatzdirektive für Bestellungseinlagerung einrichten
description: In diesem Thema wird erläutert, wie Sie eine einfache Standortanweisung einrichten.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b07cd8af0fd619a71d3fe5188f41d0a0ed954f93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429074"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Lagerplatzdirektive für Bestellungseinlagerung einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie eine einfache Standortanweisung einrichten. Das Beispiel, das angezeigt wird, erstellt, um zu bestimmen, wo sich verwendet werden Lagerplatzdirektive, Artikel führt, die für eine Bestellung eingegangen sind. Sie können diese Prozedur mit dem Daten des Demodatenunternehmen USMF oder mit eigenen Daten verwenden. Vorbedingungen: Sie müssen einen Dispositionscode erstellen. In diesem Schritt verwenden Sie einen aufgerufenen Dispositionscode neu bezeichnen. Wenn Sie Lagerplatzdirektive in eigene Daten erstellen, müssen Sie einrichten erweiterte Lagerortverwaltung für den aktuellen Lagerort und Artikel verwenden. Diese Prozedur ist für die Lagerverwaltung vorgesehen.

1. Gehen Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einrichtung > Standortanweisungen**.
2. Wählen Sie im Feld **Arbeitsauftragsart** **Bestellungen**.

## <a name="create-a-location-directive-header"></a>Erstellen einer Lagerplatzrichtlinie
1. Wählen Sie **Neu** aus.
2. Geben Sie im Feld **Laufende Nummer** eine Zahl ein. Geben Sie die Reihenfolge ein, in der der Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge, falls notwendig, auch ändern.  
3. Geben Sie im Feld **Name** einen Wert ein. Dies ist eindeutige Bezeichner für die Vorlage.  
4. Wählen Sie im Feld **Arbeitsart** **Eingabe**. Wählen Sie die Art der auszuführenden Arbeit aus. Für die Richtposition mit der Auftragsart Bestellung ist **Einlagern** der einzige unterstützte Wert.  
5. Geben Sie in das Feld **Lagerort** einen Wert ein.
6. Geben Sie im Feld **Lagerort** einen Wert ein. Lassen Sie das richtungweisende Codeleerzeichen.  Richtungweisende Codes werden verwendet, um eine Arbeitsauftragsposition des Typs zu verknüpfen platziert zu bestimmten Direktiven. Für Bestellungen wird der Lagerplatz der letzten Arbeitsauftragsposition des Typs Put aufgelöst, bevor die Arbeitsvorlage bestimmt wird. Daher ist es nicht möglich, die letzte Zeile einer Arbeitsvorlage in bestimmten Es herzustellen.   
7. Geben Sie im Feld **Dispositionscode** einen Wert ein. Der Dispositionscode schränkt die Verwendung von den Lagerplatzdirektiven ein, damit werden die Lagerplatzdirektive nur verwendet, wenn der Lagerarbeiter diesen bestimmten Wert bei der Erfassung des Artikels mithilfe eines mobilen Geräts eingibt.  
8. Wählen Sie **Speichern**.

## <a name="edit-the-query-for-directive"></a>Abfrage für zu entfernende Ausreißer bearbeiten
1. Wählen Sie **Abfrage bearbeiten**. Die Verwendung von diesen Direktiven ist bereits beschränkt, für die Artikel verwendet werden, die im Lagerort erfasst werden, den angegebenen und mit dem diesem Dispositionscode Sie angegeben haben. Sie können weitere Einschränkungen mithilfe der Abfrage hinzufügen.  
2. Wählen Sie **OK**.

## <a name="add-directive-lines"></a>Lagerplatzrichtlinienpositionen hinzufügen
1. Wählen Sie **Neu** aus. Geben Sie die Reihenfolge ein, in der der Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge, falls notwendig, auch ändern.  
2. Geben Sie im Feld **Ab Menge** eine Zahl ein. Dies ist das in geringer Menge, die für diese richtungweisende Position gültig ist.  
3. Geben Sie im Feld **Bis Menge** eine Zahl ein.
4. Geben Sie im Feld **Einheit** einen Wert ein. Die Einheit, die von der Menge sowie der Menge ist, wird die Quellensteuer ausgedrückt. Wenn Sie dieses Feld leer lassen, wird die Lagereinheit des Artikels verwendet.  
5. Wählen Sie im Feld **Menge lokalisieren** eine Option aus.
    - Kein oder Kfz-Kennzeichen-Menge: Die Menge erfasste jedem Nachverfolgen.  
    - Vereinheitlichte Menge: Die gesamte Menge, die erfasst wird.  
    - Die noch zu empfangende Menge, die in der Bestellposition angegeben ist.  
    - Die Gesamtmenge, die in der Bestellposition angegeben ist.  
6. Aktivieren oder deaktivieren Sie das Kontrollkästchen **Einschränkung nach Einheit**. Wenn Sie diese Option wählen und die Einheit auf der Seite **Einschränkung nach Einheit** angeben, können nur Artikel mit dieser Maßeinheit an den Ort gebracht werden. Wenn beispielsweise die Maßeinheit Paletten ist, können Artikel auf Paletten an einem bestimmten Lagerplatz eingelagert werden.  
7. Aktivieren oder deaktivieren Sie das Kontrollkästchen **Aufteilung zulassen**. Aktivieren Sie dieses Kontrollkästchen, um die Menge über mehrere Lagerplätze aufzuteilen.  
8. Wählen Sie **Speichern**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Beschränken Sie die richtungweisende Position zu einer bestimmten Einheit ein
1. Wählen Sie **Einschränkung nach Einheit**. Diese Schaltfläche ist nur verfügbar, wenn Sie **Speichern** drücken, nachdem Sie das Kontrollkästchen **Einschränkung nach Einheit** aktiviert haben.  
2. Geben Sie im Feld **Einheit** einen Wert ein.
3. Schließen Sie die Seite.

## <a name="add-a-location-directive-action-line"></a>Richtlinienpositionsaktivität für Lagerplätze an Lagerorten
1. Wählen Sie **Neu** aus. Geben Sie die Reihenfolge ein, in der der Lagerplatzrichtlinie für den ausgewählten Arbeitstyp verarbeitet werden soll. Sie können die Reihenfolge, falls notwendig, auch ändern.  
2. Geben Sie im Feld **Name** einen Wert ein. Dies ist eindeutige Bezeichner für die Vorlage.  
3. Wählen Sie im Feld **Feste Standortnutzung** eine Option aus.
    - Feste und nicht-korrigierte Lagerplätze: Alle nicht-korrigierten Lagerplätze sind sowie der eigene feste Lagerplatz des Produkts, innerhalb des Bereichs gültig, der in der Abfrage angegeben ist.  
    - Nur fester Ort für das Produkt: Feste Lagerplätze für das Produkt gültig sind, und alle Produktvarianten geben die gleiche Gruppe von festen Lagerplätzen frei.  
    - Nur fester Lagerplatz für die Produktvarianten: Nur die festen Lagerplätze, die für jede Produktvariante angegeben werden, gültig sind.  
4. Wählen Sie im Feld **Strategie** eine Option aus. Arbeitsaufträge vom Typ Bestellung unterstützen die folgenden Strategien: 
    - Keine: Das Element wird an der ersten gefundenen Stelle platziert.  
    - Führen Sie: Der Artikel wird an einen Speicherort installiert, in dem ähnliche Artikel bereits verfügbar sind.  
    - Leerer Lagerplatz ohne eingehende Arbeit: der Artikel wird im ersten leeren Speicherort installiert, der gefunden wird. Der Lagerplatz wird als leer angesehen, wenn dieser keinen physischen Bestand und keine erwartete eingehende Arbeit hat.  
5. Wählen Sie **Speichern**.

## <a name="edit-the-query-for-directive-action-line"></a>Abfrage für zu entfernende Ausreißer bearbeiten
1. Wählen Sie **Abfrage bearbeiten**.
2. Wählen Sie **Hinzufügen** aus.
3. Geben Sie im Feld **Feld** `location profile ID` ein. In diesem Beispiel schränken wir die möglichen Lagerplätze mithilfe einer Lagerplatzprofil Kennung ein.  
4. Geben Sie im Feld **Kriterien** einen Wert ein.
5. Wählen Sie **OK**. Sie können fortfahren, um richtungweisende Positionen und richtungweisende Aktivitäten hinzuzufügen, bis Sie alle möglichen Szenarien am Lagerort abgedeckt haben.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]