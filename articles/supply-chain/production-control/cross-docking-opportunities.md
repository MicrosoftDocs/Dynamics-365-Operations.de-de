---
title: Crossdocking von Produktionsaufträgen zu Ausgangsrampen
description: In diesem Thema wird beschrieben, wie Sie den Prozess des Crossdockings von Materials verwalten, das als fertig gestellt gemeldet wurde, spricht von eine Produktionsauftragsposition an einen ausgehenden Transportdock beendet.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockOpportunityPolicy, WHSReservationHierarchy, WHSInventTableReservationHierarchy, WHSItemGroupLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c408c0b0c32292c074bcabf3822a50a24bbdd301
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007290"
---
# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Crossdocking von Produktionsaufträgen zu Ausgangsrampen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie den Prozess des Crossdockings von Materials verwalten, das als fertig gestellt gemeldet wurde, spricht von eine Produktionsauftragsposition an einen ausgehenden Transportdock beendet.

<a name="introduction"></a>Einführung
------------

Crossdocking aus der Produktion an einen ausgehenden Lagerplatz ist für Hersteller von Bedeutung, die große Mengen produzieren und die fertigen Produkte idealerweise versenden möchten, sobald sie von den Produktionsauftragspositionen als fertiggestellt gemeldet werden. Die Produkte sollen zu den Verteilzentren, die physisch nahe bei der Kundennachfrage liegen, gesendet werden, anstatt Bestand am Produktionsstandort anzuhäufen.

Falls kein unmittelbarer Bedarf für ein Produkt besteht, muss es bei Lagerortlagerplätzen am Produktionsstandort eingelagert werden. Dieser Vorgang ist auch als *opportunistisches Crossdocking* bekannt. Dies gibt an, dass die Verkaufschance bei Bedarf zum Versand des Produkts genutzt werden soll, anstatt das Produkt für interne Lagerung zu halten.

Im folgenden Beispiel werden drei Variationen eines Flows dargestellt, der am Ende der Produktionsposition (2) beginnt.

Ein Produkt wird dem Warenausgangslagerplatz (3) als fertig gemeldet und ein Gabelstaplerfahrer holt die Palette an diesem Lagerplatz (3) ab.

-   Wenn es eine geplante Aktivität (6) für die Umlagerung des Produkts von der Fertigung (1) zu Verteilzentrum (7) gibt, wird der LKW-Fahrer vom System aufgefordert, die Palette an einen Frachttürlagerplatz (4) zu bringen.
-   Wenn der Frachttür bereits ein Anhänger zugewiesen ist, wird der LKW-Fahrer aufgefordert, das Produkt direkt auf den Anhänger zu laden.
-   Wenn keine Aktivität für die Umlagerung des Produkts geplant ist, wird der Staplerfahrer angewiesen, das Produkt zu einem Lagerplatz am internen Lagerort (5) zu bringen.

[![Opportunistisches Crossdocking](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Konfigurieren von Crossdocking
Sie konfigurieren den Crossdocking-Prozess in **Arbeitsrichtlinien** Eine Arbeitsrichtlinie enthält einen Arbeitsauftragstyp, einen Lagerplatz und ein Produkt. Im folgenden Beispiel wird Crossdocking für Produkt X und Lagerplatz Y konfiguriert.

#### <a name="work-order-types"></a>Arbeitsauftragstypen

-   Arbeitsauftragstyp: Fertigerzeugnislagerung
-   Arbeitserstellungsmethode: Crossdocking
-   Crossdocking-Richtlinienname: Umlagerungsaufträge

#### <a name="inventory-locations"></a>Lagerplätze für Lagerbestand

-   Lagerort: 51
-   Lagerplatz: Y

#### <a name="products"></a>Produkte

-   Artikelnummer: X

Derzeit kann Crossdocking für nur zwei Arbeitsauftragstypen konfiguriert werden:

-   Einlagerung von Fertigerzeugnissen
-   Einlagerung von Kuppel- und Nebenprodukten

In der **Crossdockingrichtlinie** definieren Sie, welche Dokumenttypen für das Crossdocking anwendbar sind. Derzeit wird nur das Dokumenttyp **Umlagerungsaufträge** unterstützt. Das folgende Beispiel zeigt die Konfiguration einer Crossdocking-Richtlinie.

### <a name="cross-docking-policy-name-transfer-order"></a>Crossdocking-Richtlinienname: Umlagerungsauftrag

- Laufende Nummer: 10
  -   Arbeitsauftragstyp: Übergangsabgang
- Crossdockingbedarf erfordert Lagerplatz: Falsch
- Crossdockingstrategie: Datum und Uhrzeit

### <a name="sequence-number"></a>Laufende Nummer

Der **Nummernkreis** gibt die Priorität des Dokumenttyps an. Derzeit wird nur der Typ **Umlagerungsabgang** unterstützt. Daher wird der Nummernkreis nur relevant, wenn mehr Arbeitsauftragstypen unterstützt werden.

### <a name="cross-docking-policy"></a>Crossdockingrichtlinie

Die Crossdocking-Richtlinie legt auch die Richtlinie für die Vergabe des Umlagerungsauftragsbedarfs fest. Wenn beispielsweise mehrere Umlagerungsaufträge für das gleiche Produkt, das geplante Datum und die Uhrzeit vorliegen, die für die Auslastung festgelegt werden, und dem Umlagerungsauftrag zugeordnet sind, bestimmen Sie die Vergabe zwischen den Aufträgen. Das geplante Datum und die Uhrzeit kann direkt bei der Auslastung festgelegt werden, oder die Angaben können bei einer **Terminplanung** festgelegt werden, die der Auslastung zugeordnet ist. Die Vergabe wird durch die Crossdocking-Strategie bestimmt. Momentan gibt es nur eine Strategie: **Datum und Uhrzeit**.

### <a name="cross-docking-demand-requires-location"></a>Crossdockingbedarf erfordert Lagerplatz

In der Crossdocking-Richtlinie können Sie ein Kriterium einrichten, um anzufordern, dass Umlagerungsaufträgen ein Lagerplatz zugewiesen ist, um Crossdocking zu ermöglichen. Dieses Kriterium wird im Feld **Crossdockingbedarf erfordert Lagerplatz** festgelegt. Der Lagerplatz bei der Terminplanung, der der Auslastung zugeordnet wird, wird als abschließender Lagerplatz für die Waren verwendet, für die das Crossdocking durchgeführt wird. Der endgültige Lagerplatz für die Waren, für die Crossdocking durchgeführt wird, wird von der Lagerplatzdirektive für **Umlagerungsabgang** den Arbeitsauftragstyp **Einlagern** bestimmt. Es ist möglicherweise nützlich, das Feld **Crossdockingbedarf erfordert Lagerplatz** in einem Szenario festzulegen, in dem für die Fertigprodukte nur dann ein Crossdocking durchgeführt werden soll, wenn der Frachttür ein Anhänger zugewiesen ist. In diesem Szenario werden die Waren direkt aus der Fertigungsstraße in den Anhänger verschoben. Wenn der Frachttür ein Anhänger zugewiesen wird, weist ein Benutzer der Terminplanung den Lagerplatz zu und macht diesen somit für das Crossdocking verfügbar. In den folgenden Abschnitten werden Sie durch zwei Beispiele geführt.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Szenario 1 – Crossdocking von Produktion zu Umlagerungsaufträgen

Nachdem ein Produkt an der Fertigungsstraße als fertig gemeldet wird, wird es zum Frachttürlagerplatz umgelagert. Dort wird es auf einen LKW geladen und an ein Verteilzentrum umgelagert. Verwenden Sie Unternehmens-USMF.

1.  Aktivieren Sie einen neuen Nummernkreis für das Crossdocking. Wechseln Sie zur Seite **Nummernkreise**, und wählen Sie die Schaltfläche **Generieren** aus. Der Assistent führt Sie durch den Prozess.
2.  Erstellen Sie eine Crossdockingrichtlinie. Wechseln Sie zur Seite **Crossdocking-Richtlinie** und erstellen Sie eine neue Richtlinie namens **Crossdocking zum Umlagerungsauftrag**. Beachten Sie, dass Sie nur den Arbeitsauftragstyp **Umlagerungsabgang** auswählen können und dass die einzige verfügbare Crossdockingstrategie **Datum und Uhrzeit** ist.
3.  Erstellen Sie eine Arbeitsrichtlinie. Wechseln Sie zur Seite **Arbeitsrichtlinien** und erstellen Sie eine neue Arbeitsrichtlinie namens **Cross Dock L0101**.
4.  Richten Sie Auslastungen ein, sodass diese für Umlagerungsaufträge automatisch erstellt werden. Legen Sie in den Lagerortparametern Auslastungen fest, damit diese automatisch erstellt werden, wenn Umlagerungsaufträge erstellt werden. Eine Auslastung ist eine Voraussetzung, damit ein Umlagerungsauftrag für das Crossdocking freigegeben wird.
5.  Richten Sie Artikelladungszuordnung ein. Wechseln Sie zur Seite **Artikelauslastungszuordnung**, und richten Sie eine Standardauslastungsvorlage für die Artikelgruppe **CarAudio** ein. Diese Zuordnung wird die Auslastungsvorlage für die Auslastung automatisch einfügen, wenn der Umlagerungsauftrag erstellt wird.
6.  Erstellen Sie einen Umlagerungsauftrag. Erstellen Sie den Umlagerungsauftrag für Artikelnummer L0101. Menge = 20.
7.  Geben Sie den Umlagerungsauftrag aus der Ladungsplanungsworkbench frei. Auf der Registerkarte **Versenden** wählen Sie die Menüoption für die Ladungsplanungsworkbench und im Menü **Freigabe** der Ladungsposition wählen Sie **Für Lagerort freigeben** aus. Eine offene Serienposition des Typs **Umlagerungsabgang** ist jetzt für den Umlagerungsauftrag vorhanden.
8.  Erstellen Sie einen Produktionsauftrag. Wechseln Sie zur Listenseite **Produktionsauftrag** und erstellen Sie einen Produktionsauftrag für Produkt L0101. Menge = 20. Schätzen und starten Sie den Produktionsauftrag. Beachten Sie, dass das Felde **Kommissionierliste jetzt buchen** auf **Nein** festgelegt bleibt.
9.  Vom mobilen Gerät als beendet melden. Wechseln Sie zum Portal für das mobile Gerät wählen Sie die Menüoption **Fertig melden und einlagern** aus. Melden Sie L0101 jetzt vom Handgerät als fertig. Menge = 10. Beachten Sie, dass der Einlieferungslagerplatz **BAYDOOR** ist. Dieser Lagerplatz stammt aus der Lagerplatzdirektive **Umlagerungsabgang** für den Arbeitsauftragstyp **Einlagern**. Beachten Sie auch, dass Arbeit des Typs **Übergangsabgang** erstellt und ausgeführt wurde. Wechseln Sie zu den Arbeitsdetails des Umlagerungsauftrags, um die Arbeit zu überprüfen.
10. Melden Sie jetzt zusätzliche 10 Artikel aus den mobilen Geräten. Beachten Sie, dass der Einlieferungslagerplatz wieder **BAYDOOR** ist. Beachten Sie auch, dass ein neuer Arbeitstyps **Übergangsabgang** für 10 Stück erstellt wurde.
11. Versuchen Sie nun, weitere 20 Stück für den Produktionsauftrag zu starten und dann 20 St. als fertig zu melden, indem Sie das tragbare Gerät verwenden. Diesmal wird Lagerplatz **LP-001** als Einlieferungslagerplatz vorgeschlagen. Dieser Lagerplatz stammt aus der Lagerplatzdirektive für **Einlagerung von Fertigerzeugnissen**. Diese Lagerplatzdirektive wird verwendet, da keine Möglichkeit für Crossdocking vorhanden ist. Der Umlagerungsauftrag für LP-001 wurde vollständig von den zwei Crossdockingaktivitäten in Schritt 9 und 10 erfüllt. Beachten Sie, dass Arbeit vom Typ **Einlagerung von Fertigerzeugnissen** erstellt und verarbeitet wurde.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Szenario 2 - Crossdocking aus der Produktion zu Umlagerungsaufträgen mit einer Terminplanung

Nachdem ein Produkt an der Fertigungsstraße als fertig gemeldet wird, wird es an einen Frachttürlagerplatz umgelagert, der von einer Terminplanung für die Frachttürlagerplätze identifiziert wird. Verwenden Sie Unternehmens-USMF.

1.  Ändern Sie die Crossdockingrichtlinie. Ändern Sie die Crossdockingrichtlinie, die Sie in Szenario 1 erstellt haben, indem Sie das Kontrollkästchen **Crossdockingbedarf erfordert Lagerplatz** aktivieren.
2.  Erstellen Sie einen neuen Umlagerungsauftrag.
3.  Öffnen Sie die **Ladungsplanungsworkbench**.
4.  Wechseln Sie aus der Ladungsplanungsworkbench zum Abschnitt **Auslastung**, und wählen Sie **Terminplanung** im Menü **Transport** aus, um eine neue Terminplanung zu erstellen. Beachten Sie, dass die Terminplanung eine Referenz zu dem Umlagerungsauftrag im Feld **Auftragsnummer** hat. Im Feld **Geplantes Startdatum/-uhrzeit am Lagerplatz** können Sie das Datum und die Uhrzeit für den Termin festlegen. Dieses Datum und die Uhrzeit werden verwendet, wenn Crossdockingbedarf während des Crossdockingprozesses priorisiert wird. Die Angaben zu Datum und Uhrzeit, die Sie in diesem Feld festlegen, aktualisieren das Feld **Geplantes Datum und Uhrzeit des Versands der Ladung** bei der entsprechende Auslastung. Der Lagerplatz auf dem Inforegister **Versanddetails** bestimmt den Lagerplatz, an den der Umlagerungsauftrag versendet wurde.
5.  Geben Sie im **Ladungsplanungsworkbench** an den Lagerort frei.
6.  Erstellen Sie einen Produktionsauftrag für Artikelnummer **L0101**, und legen Sie den Status mit einer Menge von 20 auf **Gestartet** fest.
7.  Vom mobilen Gerät als beendet melden.
8.  Wechseln Sie zum Portal für das mobile Gerät und wählen Sie die Menüoption **Fertig melden und einlagern** aus.
9.  Melden Sie Artikelnummer **L0101** Handgerät als fertig. Beachten Sie, dass der Einlieferungslagerplatz jetzt **BAYDOOR 2** ist. Diese Option ist vom Terminplanung anstelle von **Umlagerungseingang** Lagerplatzdirektive gefunden.

### <a name="additional-information"></a>Weitere Informationen

-   Das Crossdockingszenario wird für Chargen- und seriengesteuerte Artikel unterstützt. Die Chargen- und Seriennummerdimensionen über und unter dem Lagerplatz in der Reservierungshierarchie sind definiert. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]