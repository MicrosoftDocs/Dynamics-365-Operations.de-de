---
title: Zu hohe Entnahme für Aufträge und Umlagerungsaufträge verwenden
description: In diesem Artikel wird erläutert, wie Sie die zu hohe Entnahme für Aufträge und Umlagerungsaufträge aktivieren.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b8bbc7d532f910edfb442831d6c906f253dee06c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897283"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Zu hohe Entnahme für Aufträge und Umlagerungsaufträge verwenden

[!include [banner](../includes/banner.md)]

In diesem Artikel wird ein Szenario vorgestellt, in dem gezeigt wird, wie Sie entweder einer bestimmten Arbeitskraft oder allen Arbeitskräften die zu hohe Entnahme ermöglichen. Der Prozess der zu hohen Entnahme ermöglicht eine kontrollierte zu hohe Entnahme während der Entnahmearbeit.

Die zu hohe Lagerortentnahme ist ein einfaches Konzept. Das System ermöglicht es Arbeitskräften, mehr Artikel zu entnehmen, als für einen Auftrag angegeben sind. Es berücksichtigt jedoch weiterhin die auf Positionsebene für den Umlagerungsauftrag oder Auftrag festgelegte Überlieferungsgrenze. Wenn diese Grenze überschritten wird, benachrichtigt die Warehouse Management-App die Arbeitskräfte, dass sie die Überlieferungsgrenze überschreiten.

Die Überlieferungsfunktion hilft, den Wartungsaufwand zu minimieren und hilft auch Ihrem Setup, flexibel zu bleiben. Sie können ein oder mehrere Menüelemente für mobile Geräte definieren und nur für einige davon die zu hohe Entnahme aktivieren. Sie können auch verhindern, dass ausgewählte Arbeitskräfte für Aufträge und/oder Umlagerungsaufträge zu hohe Entnahmen vornehmen, ohne die Menüelemente ändern zu müssen. Stattdessen können Sie eine oder beide dieser Funktionen in den entsprechenden Arbeitskräfte-Setups deaktivieren.

Die Funktion zur zu hohen Entnahme kann Arbeitskräften helfen, sich Zeit und Mühe zu sparen, wenn sie Artikel entnehmen und versenden. Mit der Funktion können Arbeitskräfte beispielsweise die folgenden Aufgaben ausführen:

- Ausgleich von Rückgängen bei der Entnahme oder Lieferung.
- Das Auspacken von Verpackungsmaterial während des Entnahmeprozesses vermeiden.
- Artikelschäden während des Transports ausgleichen.
- Mengen- oder Maßeinheitsabweichung versenden.
- Das Aufteilen von Mengen auf Ladungsträgern vermeiden.
- Materialverschwendung und Knappheit von teuren Materialien vermeiden.
- Die entnommene Menge nach der Entnahme messen (z. B. durch Wiegen des LKW).

> [!IMPORTANT]
> Die Funktion zur zu hohen Entnahme gilt nur für die Entnahme und Verarbeitung von Aufträgen und Umlagerungsaufträgen. Die Wiederbeschaffung unterstützt die zu hohe Entnahme nicht. Wenn Wiederbeschaffungsarbeiten ausgeführt werden, erlaubt das System den Benutzern nicht, zu viel zu entnehmen.

Das Szenario in diesem Artikel zeigt, wie Sie die Funktion für die zu hohe Entnahme einrichten und verwenden.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Szenariovoraussetzung: Demodaten zur Verfügung stellen

Das Szenario in diesem Artikel verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf *USMF* festlegen, bevor Sie beginnen.

## <a name="scenario-setup"></a>Szenarioeinrichtung

Bevor Sie das Beispielszenario durcharbeiten, müssen Sie die zu hohe Entnahme sowohl für die entsprechende Arbeitskraft als auch für das entsprechende Menüelement aktivieren.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Die zu hohe Entnahme für eine Arbeitskraft zulassen

Hier ist das allgemeine Verfahren zum Konfigurieren einer Arbeitskraft, um die zu hohe Entnahme für Aufträge und Umlagerungsaufträge separat zu aktivieren. Diese Konfiguration steuert, welche entnehmende Arbeitskraft die zu hohe Entnahme durchführen kann und ob diese Arbeitskraft sowohl für Umlagerungsaufträge als auch für Aufträge eine zu hohe Entnahme durchführen kann.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeitskraft**.
1. Wählen Sie im Listenbereich **Julia Funderburk**.
1. Wählen Sie im Inforegister **Benutzer** die Zeile aus, die die folgenden Werte enthält. Wenn keine Zeile mit diesen Werten vorhanden ist, erstellen Sie sie.

    - **Benutzer-ID:** *24*
    - **Benutzername:** *WH 24*
    - **Standardlagerort:** *24*
    - **Menüname:** *Hauptseite*

1. Legen Sie auf dem Inforegister **Arbeit** die folgenden Werte für den Benutzer *24* fest, wenn sie nicht bereits festgelegt sind:

    - **Zu hohe Entnahme für Auftrag zulassen:** *Ja*
    - **Zu hohe Entnahme für Umlagerungsauftrag zulassen:** *Ja*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Auf einem mobilen Gerät ein Menüelement einrichten, um die zu hohe Entnahme zuzulassen

Hier ist das allgemeine Verfahren zum Konfigurieren eines Menüelements eines mobilen Geräts, um die zu hohe Entnahme zu ermöglichen. Abhängig von Ihren geschäftlichen Anforderungen an die Berechtigungsstufe der Arbeitskraft, die das Menü des mobilen Geräts verwenden wird, können einige Parameter aktiviert oder deaktiviert sein.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Wählen Sie im Listenbereich den Datensatz mit der Bezeichnung *Auftragskommissionierung*. Wenn kein Datensatz mit diesem Namen vorhanden ist, erstellen Sie ihn. Bestätigen Sie oder legen Sie die folgenden Werte für den Datensatz fest:

    - **Name des Menüelements:** *Auftragskommissionierung*
    - **Titel:** *Auftragskommissionierung*
    - **Modus:** *Arbeit*
    - **Vorhandene Arbeit verwenden:** *Ja*
    - **Geleitet von:** *Benutzergeleitet*
    - **Zielladungsträger überschreiben:** *Ja*
    - **Zielladungsträger während Einlagern überschreiben:** *Ja*
    - **Arbeit vom Benutzer gesperrt halten:** *Ja*
    - **Zu hohe Entnahme zulassen:** *Ja*

> [!IMPORTANT]
> Nachdem die relevanten Parameter sowohl für die Arbeitskraft als auch für das Menüelement des mobilen Geräts aktiviert wurden, kann die zu hohe Entnahme nur über das mobile Gerät verarbeitet werden.

## <a name="example-scenario"></a>Beispielszenario

Nachdem die Voraussetzungen, das Arbeitskraft-Setup und das Menüelement-Setup erfüllt sind, können Sie mit der Funktion arbeiten.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Einen Auftrag erstellen, der eine Überlieferung zulässt

1. Gehen Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus, um einen neuen Auftrag zu erstellen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *24*

1. Wählen Sie **OK** aus.
1. Der neue Auftrag wird geöffnet. Fügen Sie im Inforegister **Auftragspositionen** eine Position mit den folgenden Einstellungen hinzu:

    - **Artikelnummer** *A001*
    - **Menge** *10*

1. Im Inforegister **Zeilendetails** auf der Registerkarte **Lieferung** legen Sie das Feld **Mehrlieferung** auf *10* fest.
1. Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.
1. Schließen Sie die Seite **Reservierung**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

Wenn die Freigabe abgeschlossen ist, erhalten Sie Informationsnachrichten mit der Wellen- und Lade-ID, die erstellt wurden.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Holen Sie sich die Arbeitskennung und die Kennzeichennummer für den neuen Auftrag

Als Sie den Auftrag an den Lagerort freigegeben haben, sollte das System eine neue Arbeitskennung mit einer Entnahmeposition erstellt haben. Befolgen Sie diese Schritte, um die Arbeitskennung und die Ladungsträgerzuweisung zu finden.

1. Wechseln Sie zu **Lagerortverwaltung \> Arbeit \> Arbeitsdetails**.
1. Suchen Sie in dem **Übersicht**-Raster die **Bestellnummer**-Spalte für den Auftrag, den Sie gerade erstellt haben. Notieren Sie sich für den Auftrag die entsprechende Arbeitskennung.
1. Wählen Sie die Zeile für den neuen Auftrag aus, um relevante Informationen im **Positionen**-Raster anzuzeigen. Notieren Sie sich den Ort, an dem der Artikel ausgewählt wird.
1. Wechseln Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Bestandsliste**.
1. Wählen Sie im Aktionsbereich **Dimensionen** aus.
1. Stellen Sie im Dialogfeld **Dimensionsanzeige** sicher, dass die Kontrollkästchen **Ladungsträger**, **Lagerort** und **Artikelnummer** aktiviert sind und wählen Sie anschließend **OK** aus.
1. Legen Sie im **Filter**-Bereich folgende Filter fest:

    - **Artikelnummer**: **ist eine von** – *A0001*
    - **Warenhaus** – **beginnt mit** – *24*

1. Wählen Sie **Anwenden** aus.
1. Notieren Sie sich die angezeigten Werte für **Kennzeichen**.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Auftragsüberkommissionierung mithilfe der mobilen Warehouse Management-App

1. Melden Sie sich bei der Warehouse Management Mobile App als ein Benutzer im Lagerort *24* an.
1. Gehen Sie zu **Ausgehend \> Verkaufskommissionierung**.
1. Geben Sie im Feld **Arbeitskennung oder Ladungsträger scannen** die Arbeitskennung ein, die für den Auftrag erstellt wurde.
1. Wählen Sie **OK** (Häkchensymbol).
1. Wählen Sie **zu hohe Entnahme**.
1. Legen Sie das Feld **Entnahmemenge** auf *14* fest.
1. Wählen Sie **OK** (Häkchensymbol).

    Auf der Seite **Zu hohe Entnahme** wird die folgende Meldung angezeigt: „Überlieferung der Position beträgt 40,00 %, aber die zulässige Überlieferung beträgt nur 10,00 %.“ Diese Nachricht weist darauf hin, dass die von Ihnen eingegebene Entnahmemenge die Überlieferungsgrenze überschreitet. Die Überlieferungsgrenze für die Auftragsposition beträgt 10 %. Daher können Sie bei einer angegebenen Menge von 10 nur um 1 zu hoch entnehmen, insgesamt also 11.

1. Legen Sie das Feld **Entnahmemenge** auf *11* fest.
1. Wählen Sie **OK** (Häkchensymbol).
1. Geben Sie im Feld **Ladungsträger** den Ladungsträger ein, den Sie sich im vorherigen Abschnitt notiert haben.
1. Geben Sie in das Feld **Zielladungsträger** einen Zielladungsträger ein. Beachten Sie, dass Entnahmeort (*FLOOR-001*), Artikel (*A0001*) und Menge (*11 Stk*) gezeigt werden.
1. Wählen Sie **OK** (Häkchensymbol).
1. Prüfen Sie die Informationen auf der Seite **Aufträge – Einlagern**. Das Feld **Lagerplatz** sollte anzeigen, dass die ausgewählten Artikel an den Lagerplatz *BAYDOOR* gehen.
1. Wählen Sie **OK** (Häkchensymbol).

Auf der Seite **Arbeits-/Kennzeichen-ID scannen** erhalten Sie eine Meldung „Arbeit abgeschlossen“. Diese Nachricht zeigt an, dass die Arbeitskennung des Auftrags abgeschlossen wurde und die zu hohe Entnahmemenge die Überlieferungsgrenze von 10 % nicht überschreitet.
