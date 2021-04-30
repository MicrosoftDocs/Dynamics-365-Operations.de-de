---
title: Flexible Reservierungsrichtlinie für Dimensionen auf Lagerortebene
description: In diesem Thema wird die Bestandsreservierungsrichtlinie beschrieben, mit der Unternehmen, die Produkte mit Chargenverfolgung verkaufen und für die Logistik WMS-fähige Vorgänge ausführen, bestimmte Chargen für Debitorenaufträge reservieren können, obwohl die mit den Produkten verknüpfte Reservierungshierarchie die Reservierung bestimmter Chargen nicht zulässt.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 13b81459fe3449a90839dac7637118f09afe2e55
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910232"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Flexible Reservierungsrichtlinie für Dimensionen auf Lagerortebene

[!include [banner](../includes/banner.md)]

Wenn eine Bestandsreservierungshierarchie vom Typ *Charge unterhalb\[Lagerplatz\]* mit Produkten verknüpft ist, können Unternehmen, die Produkte mit Chargenverfolgung verkaufen und ihre Logistik als Operationen ausführen, die für das Microsoft Dynamics 365 Warehouse Management System (WMS) aktiviert sind, bestimmte Chargen dieser Produkte nicht für Debitorenaufträge reservieren.

Ähnlich können bestimmte Ladungsträger nicht für Produkte in Aufträgen reserviert werden, wenn diese Produkte mit der Standardreservierungshierarchie verknüpft sind.

In diesem Thema wird die Bestandsreservierungsrichtlinie beschrieben, mit der diese Unternehmen bestimmte Chargen oder Ladungsträger reservieren können, auch wenn die Produkte mit einer Reservierungshierarchie *Charge unterhalb\[Lagerplatz\]* verknüpft sind.

## <a name="inventory-reservation-hierarchy"></a>Bestandreservierungshierarchie

In diesem Abschnitt wird die vorhandene Bestandsreservierungshierarchie zusammengefasst.

Die Bestandsreservierungshierarchie schreibt vor, dass der Bedarfsauftrag in Bezug auf die Lagerdimension die obligatorischen Dimensionen für Standort, Lagerort und Bestandsstatus enthält. Mit anderen Worten, die obligatorischen Dimensionen sind alle Dimensionen über der Lagerplatzdimension in der Reservierungshierarchie, während die Lagerlogik dafür verantwortlich ist, den angeforderten Mengen einen Lagerplatz zuzuweisen und ihn zu reservieren. Bei den Interaktionen zwischen dem Bedarfsauftrag und den Lagerortvorgängen wird erwartet, dass der Bedarfsauftrag angibt, von wo der Auftrag versendet werden muss (d. h., von welchem Lagerplatz und von welchem Lagerort). Das Lager verlässt sich dann auf seine Logik, um die erforderliche Menge in den Lagerstätten zu finden.

Um jedoch das Betriebsmodell des Unternehmens widerzuspiegeln, unterliegen die Rückverfolgungsangaben (Chargen- und Seriennummern) einer größeren Flexibilität. Eine Bestandsreservierungshierarchie kann Szenarien berücksichtigen, bei denen die folgenden Bedingungen zutreffen:

- Das Unternehmen verlässt sich auf seine Lagerortvorgänge für die Verwaltung der Entnahme von Mengen mit Chargen- oder Seriennummern, *nachdem* die Mengen an einem Lagerort gefunden wurden. Dieses Modell wird häufig als *Charge unterhalb\[Lagerplatz\]* oder *Serie unterhalb\[Lagerplatz\]* bezeichnet. Es wird normalerweise verwendet, wenn die Chargen- oder Seriennummer eines Produkts für die Debitoren nicht wichtig ist, die eine Nachfrage beim verkaufenden Unternehmen stellen.
- Das Unternehmen verlässt sich auf seine Lagerortvorgänge für die Verwaltung der Entnahme von Mengen mit Chargen- oder Seriennummern, *bevor* die Mengen an einem Lagerort gefunden wurden. Wenn Chargen- oder Seriennummern als Teil der Auftragsspezifikation eines Debitors erforderlich sind, werden sie im Bedarfsauftrag aufgeführt. Die Lagerortvorgänge, welche die Mengen im Lagerort finden, dürfen diese nicht ändern. Dieses Modell wird häufig als *Charge oberhalb\[Lagerplatz\]* oder *Serie oberhalb\[Lagerplatz\]* bezeichnet. Da die Dimensionen über dem Lagerplatz die spezifischen Anforderungen für den Bedarf sind, die erfüllt werden müssen, werden sie von der Lagerlogik nicht zugeteilt. Diese Dimensionen **müssen** immer auf dem Bedarfsauftrag oder in den entsprechenden Reservierungen angegeben werden.

In diesen Szenarien besteht die Herausforderung darin, dass jedem freigegebenen Produkt nur eine Bestandsreservierungshierarchie zugeordnet werden kann. Damit das WMS nachverfolgte Artikel verarbeiten kann, können, nachdem die Hierarchiezuweisung bestimmt, wann die Chargen- oder Seriennummer reserviert werden sollte (entweder wenn der Bedarfsauftrag entgegengenommen wird oder während der Lagerentnahme), diese Zeiten nicht ad-hoc geändert werden.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Flexible Reservierung für chargenverfolgte Artikel

### <a name="business-scenario"></a>Geschäftsszenario

In diesem Szenario verwendet ein Unternehmen eine Bestandsstrategie, bei der Fertigwaren anhand von Chargennummern verfolgt werden. Diese Firma verwendet auch die WMS-Arbeitsauslastung. Da diese Arbeitsauslastung eine gut gerüstete Logik für die Planung und Durchführung von Kommissionierungs- und Versandvorgängen für Artikel hat, für die Chargen aktiviert sind, werden die meisten Fertigprodukte mit der Bestandsreservierungshistorie *Charge unterhalb\[Lagerplatz\]* verknüpft. Der Vorteil dieser Art des operativen Einrichtung besteht darin, dass Entscheidungen (die im Grunde genommen Reservierungsentscheidungen sind) darüber, welche Chargen kommissioniert werden sollen und wo sie im Lager abgelegt werden sollen, verschoben werden, bis mit der Kommissionierung begonnen wird. Sie werden nicht schon gemacht, wenn der Kunde bestellt.

Obwohl die Reservierungshistorie *Charge unterhalb\[Lagerort\]* den Geschäftszielen des Unternehmens dient, fordern viele der etablierten Unternehmenskunden bei der Nachbestellung die gleiche Charge an, wie beim vorherigen Kauf. Aus diesem Grund ist das Unternehmen bestrebt, die Regeln für die Chargenreservierung flexibel zu gestalten, sodass, je nachdem, ob der Kunde den gleichen Artikel wünscht, die folgenden Verhaltensweisen auftreten:

- Eine Chargennummer kann aufgezeichnet und reserviert werden, wenn der Auftrag vom Verkäufer entgegengenommen wird. Sie kann während des Lagerortbetriebs nicht geändert werden und/oder aufgrund anderer Bedarfe verwendet werden. Dieses Verhalten hilft zu gewährleisten, dass die bestellte Chargennummer an den Kunden gesendet wird.
- Wenn die Chargennummer für den Kunden nicht wichtig ist, kann der Lagerbetrieb während der Kommissionierungsarbeiten eine Chargennummer bestimmen, nachdem die Kundenauftragsregistrierung und -reservierung durchgeführt wurden.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Reservierung einer bestimmten Charge im Auftrag zulassen

Um der gewünschten Flexibilität bei der Chargenreservierung für Artikel, die mit einer *Charge unterhalb\[Lagerplatz\]*-Bestandsreservierungshistorie verknüpft sind, gerecht zu werden, müssen Bestandsverwalter das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** für die **Chargennummer**-Ebene auf der Seite **Bestandsreservierungshierarchien** aktivieren.

![Bestandreservierungshierarchie flexibler machen](media/Flexible-inventory-reservation-hierarchy.png)

Wenn die **Chargennummer**-Ebene in der Hierarchie ausgewählt wird, werden alle Dimensionen über dieser Ebene und bis zur **Lagerort**-Ebene wird automatisch ausgewählt. (Standardmäßig sind alle Dimensionen über der **Lagerort**-Ebene ausgewählt.) Dieses Verhalten spiegelt eine Logik wider, bei der alle Dimensionen im Bereich zwischen Chargennummer und Lagerort automatisch reserviert werden, nachdem Sie eine bestimmte Chargennummer aus der Auftragsposition reserviert haben.

> [!NOTE]
> Das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** gilt nur für die Reservierungshierarchieebenen, die unterhalb der Lagerortdimension liegen.
>
> **Chargennummer** und **Ladungsträger** sind die einzigen Ebenen in der Hierarchie, die für die flexible Reservierungsrichtlinie offen sind. Mit anderen Worten, Sie können das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** nicht für die Ebenen **Lagerplatz** oder **Seriennummer** aktivieren.
>
> Wenn Ihre Reservierungshierarchie die Seriennummerdimension enthält (die immer unterhalb der **Chargennummer**-Ebene liegen muss), und wenn Sie die chargenspezifische Reservierung für die Chargennummer aktiviert haben, wird das System weiterhin die Seriennummernreservierung und die Kommissionierungsvorgänge basierend auf den Regeln durchführen, die für die Reservierungsrichtlinie *Serie unterhalb\[Lagerplatz\]* gelten.

Sie können jederzeit eine chargenspezifische Reservierung für eine vorhandene *Charge unterhalb\[Lagerplatz\]*-Reservierungsrichtlinie in Ihrer Bereitstellung zulassen. Diese Änderung wirkt sich nicht auf Reservierungen und offene Lagerarbeiten aus, die vor der Änderung erstellt wurden. Das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** kann aber nicht deaktiviert werden, wenn Lagerbuchungen vom Abgangstyp **Bestellt reserviert**, **Physisch reserviert** oder **Bestellt** für mindestens einen Artikel vorhanden sind, der mit der Reservierungshistorie verknüpft ist.

> [!NOTE]
> Wenn die vorhandene Reservierungshierarchie eines Artikels keine Chargenspezifikation für den Auftrag zulässt, können Sie ihn einer Reservierungshierarchie zuordnen, die eine Chargenspezifikation zulässt, vorausgesetzt, die Struktur der Hierarchieebene ist in beiden Hierarchien gleich. Verwenden Sie die **Reservierungshierarchie für Artikel ändern**-Funktion, um die Neuzuweisung durchzuführen. Diese Änderung ist möglicherweise relevant, wenn Sie die flexible Chargenreservierung für eine Teilmenge von Artikeln mit Chargenverfolgung verhindern möchten, aber für den Rest des Produktportfolios zulassen möchten.

Unabhängig davon, ob Sie das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** aktiviert haben, wird dennoch die standardmäßige Lagerort-Operationslogik angewendet, die für eine *Charge unterhalb\[Lagerplatz\]*-Reservierungshierarchie gilt, wenn Sie keine bestimmte Chargennummer für den Artikel in einer Auftragsposition reservieren möchten.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Reservieren einer bestimmten Chargennummer für eine Kundenbestellung

Nachdem die *Charge unterhalb\[Lagerplatz\]*-Bestandsreservierungshierarchie eines Artikels mit Chargenverfolgung so eingerichtet ist, dass bestimmte Chargennummern für Aufträge reserviert werden können, können Verarbeiter von Aufträgen, je nach Kundenwunsch, die Debitorenaufträge für den gleichen Artikel auf eine der folgenden Arten aufnehmen:

- **Auftragsdetails ohne Angabe einer Chargennummer eingeben** – Dieser Ansatz sollte verwendet werden, wenn die Chargenspezifikation des Produkts für den Kunden nicht wichtig ist. Alle bestehenden Prozesse, die mit der Abwicklung eines Auftrags dieser Art verbunden sind, bleiben im System unverändert. Es sind keine zusätzlichen Überlegungen seitens der Benutzer erforderlich.
- **Bestelldetails eingeben und eine bestimmte Chargennummer reservieren** – Dieser Ansatz sollte verwendet werden, wenn der Kunde eine bestimmte Charge anfordert. In der Regel fordern Kunden eine bestimmte Charge an, wenn sie ein zuvor erworbenes Produkt erneut bestellen. Diese Art der chargenspezifischen Reservierung wird als *auftragsgebundene Reservierung* bezeichnet.

Die folgenden Regeln gelten, wenn Mengen verarbeitet werden und eine Chargennummer für eine bestimmte Bestellung vorgegeben ist:

- Um die Reservierung einer bestimmten Chargennummer für einen Artikel zuzulassen, für den die Reservierungsrichtlinie *Charge unterhalb\[Lagerplatz\]* gilt, muss das System alle Dimensionen bis zum Lagerort reservieren. Dieser Bereich umfasst normalerweise die Ladungsträgerdimension.
- Lagerplatzrichtlinien werden nicht verwendet, wenn Kommissionierungsarbeiten für eine Verkaufsposition angelegt werden, die die auftragsgebundene Chargenreservierung verwendet.
- Während der Verarbeitung von Lagerarbeit für auftragsgebundene Chargen dürfen weder der Benutzer noch das System die Chargennummer ändern. (Diese Verarbeitung umfasst auch die Ausnahmebehandlung.)

Das folgende Beispiel zeigt den vollständigen Ablauf.

## <a name="example-scenario-batch-number-allocation"></a>Beispielszenario: Chargennummernzuteilung

Für dieses Beispielmüssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Einrichten einer Bestandsreservierungshierarchie, um eine chargenspezifische Reservierung zu ermöglichen

1. Gehen Sie zu **Lagerortverwaltung** \> **Einrichten** \> **Bestand \> Reservierungshierarchie**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** einen Namen ein (beispielsweise **BatchFlex**).
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein (beispielsweise **Charge unterhalb flexibel**).
5. Wählen Sie im Feld **Ausgewählt** **Seriennummer** und **Besitzer** aus und wählen Sie dann die linke Pfeiltaste, um sie zum Feld **Verfügbar** zu verschieben.
6. Wählen Sie **OK**.
7. In der Zeile mit der **Chargennummer**-Dimensionsebene aktivieren Sie das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen**. Die Ebenen **Ladungsträger** und **Lagerort** werden automatisch ausgewählt und Sie können die Kontrollkästchen für diese nicht deaktivieren.
8. Wählen Sie **Speichern**.

### <a name="create-a-new-released-product"></a>Neues freigegebenes Produkt erstellen

1. Stellen Sie die drei Stammdatenparameter des Produkts mit diesen Werten ein:

    - Wählen Sie im Feld **Lagerdimensionsgruppe** **Ware** aus.
    - Wählen Sie im Feld **Rückverfolgungsgruppe** **Batch-Phy** aus.
    - Wählen Sie im Feld **Reservierungshierarchie** **BatchFlex** aus.

2. Erstellen Sie zwei Chargennummern, beispielsweise **B11** und **B22**.
3. Fügen Sie unter Verwendung der folgenden Werte Artikelmengen zum verfügbaren Bestand hinzu.

    | Lagerort | Chargennummer | Elektronische Adresse | Ladungsträger | Leistung |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Nichts          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Auftragsdetails eingeben

1. Wechseln Sie zu **Vertrieb und Marketing** \> **Aufträge** \> **Alle Aufträge**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Auftragskopf im Feld **Debitorenkonto** **US-003** ein.
4. Fügen Sie eine Position für den neuen Artikel hinzu und geben Sie als Menge **10** ein. Stellen Sie sicher, dass das Feld **Lagerort** auf **24** gesetzt ist.
5. Wählen Sie im Inforegister **Auftragspositionen** **Bestand** und dann in der Gruppe **Verwalten** **Chargenreservierung** aus. Die Seite **Chargenreservierung** zeigt eine Liste der Chargen, die für die Reservierung für die Bestellposition verfügbar sind. In diesem Beispiel wird eine Menge von **20** für die Chargennummer **B11** und eine Menge von **10** für die Chargennummer **B22** angezeigt. Beachten Sie, dass auf die Seite **Chargenreservierung** nicht von einer Position aus zugegriffen werden kann, wenn der Artikel in dieser Position mit einer *Charge unterhalb\[Lagerplatz\]*-Reservierungshierarchie verknüpft ist, es sei denn, diese ist so eingerichtet, dass chargenspezifische Reservierungen möglich sind.

    > [!NOTE]
    > Um eine bestimmte Charge für einen Auftrag zu reservieren, müssen Sie die Seite **Chargenreservierung** verwenden.
    >
    > Wenn Sie die Chargennummer direkt in die Auftragsposition eingeben, verhält sich das System so, als hätten Sie einen bestimmten Chargenwert für einen Artikel eingegeben, für den die *Charge unterhalb\[Lagerplatz\]*-Reservierungsrichtlinie gilt. Wenn Sie die Position speichern, erhalten Sie eine Warnmeldung. Wenn Sie bestätigen, dass die Chargennummer direkt in der Bestellposition angegeben werden soll, wird die Position nicht von der normalen Lagerortverwaltungslogik verarbeitet.
    >
    > Wenn Sie die Menge über die Seite **Reservierung** reservieren, wird keine bestimmte Charge reserviert und die Ausführung der Lagerortoperationen für die Position folgt den Regeln, die im Rahmen der Reservierungsrichtlinie *Charge unterhalb\[Lagerplatz\]* gelten.

    Im Allgemeinen funktioniert und interagiert diese Seite genauso wie sie bei Artikeln funktioniert und interagiert, die mit einer Reservierungshierarchie vom Typ *Charge oberhalb\[Lagerplatz\]* verknüpft sind. Es gelten jedoch folgende Ausnahmen:

    - Das Inforegister **Chargennummern für Quellposition zugesagt** zeigt die Chargennummern an, die für die Bestellposition reserviert sind. Die Chargenwerte im Raster werden während des gesamten Erfüllungszyklus der Auftragsposition angezeigt, einschließlich der Phasen der Lagerortverarbeitung. Im Gegensatz dazu werden auf dem Inforegister **Übersicht** regelmäßige Auftragspositionsreservierungen (also Reservierungen für die Dimensionen oberhalb der **Lagerort**-Ebene) im Raster bis zu dem Punkt angezeigt, wenn Lagerarbeiten generiert werden. Die Arbeitsentität übernimmt dann die Positionsreservierung und die Positionsreservierung erscheint nicht mehr auf der Seite. Das Inforegister **Chargennummern für Quellposition zugesagt** sorgt mit dafür, dass der Auftragsverarbeiter die Chargennummern, die für den Kundenauftrag zugesagt wurden, während des gesamten Lebenszyklus bis hin zur Rechnungsstellung anzeigen kann.
    - Zusätzlich zur Reservierung einer bestimmten Charge kann ein Benutzer den spezifischen Lagerort und Ladungsträger manuell auswählen und auf die automatische Auswahl durch das System verzichten. Diese Funktion hängt mit dem Design des auftragsgebunden Chargenreservierungsmechanismus zusammen. Wie bereits erwähnt: Wenn eine Chargenummer für einen Artikel reserviert ist, für den die Reservierungsrichtlinie *Charge unterhalb\[Lagerplatz\]* gilt, muss das System alle Dimensionen bis zum Lagerort reservieren. Aus diesem Grund gelten für die Lagerarbeit die gleichen Lagerdimensionen, die von den Benutzern reserviert wurden, die diese Aufträge bearbeitet haben. Sie zeigt möglicherweise nicht immer die Artikellagerplatzierung, die für Kommissionierungsarbeiten zweckmäßig oder möglich ist. Wenn Auftragsbearbeiter die Einschränkungen des Lagerorts kennen, möchten sie möglicherweise die spezifischen Lagerorte und Ladungsträger manuell auswählen, wenn sie eine Charge reservieren. In diesem Fall muss der Benutzer die **Dimensionen anzeigen**-Funktionalität auf dem Seitenkopf nutzen und den Lagerort und den Ladungsträger zum Raster im Inforegister **Übersicht** hinzufügen.

6. Auf der Seite **Chargenreservierung** wählen Sie die Position für Charge **B11** sowie **Position reservieren** aus. Es gibt keine festgelegte Logik zum Zuweisen von Lagerorten und Ladungsträgern während der automatischen Reservierung. Sie können die Menge manuell in das Feld **Reservierung** eingeben. Beachten Sie, dass auf dem Inforegister **Chargennummern für Quellposition zugesagt** die Charge **B11** als **Zugesagt** angezeigt wird.

    ![Festlegen einer bestimmten Chargennummer für eine Auftragsposition auf der Seite „Chargenreservierung“](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Die Reservierung der Menge auf einer Auftragsposition kann über mehrere Chargen hinweg erfolgen. Ebenso kann die Reservierung der gleichen Charge für mehrere Lagerorte und Ladungsträger erfolgen (sofern Ladungsträger für die Lagerorte aktiviert sind).
    >
    > Die Reservierung einer bestimmten Charge in der Menge auf einer Auftragsposition kann auch teilweise erfolgen. Beispielsweise kann eine Gesamtmenge von 100 Einheiten reserviert werden, sodass eine bestimmte Charge 20 Einheiten enthalten muss. Für die restlichen 80 Einheiten werden verfügbare Chargen auf Standort- und Lagerortebene reserviert. In diesem Fall übernimmt das WMS die Kommissionierung mittels zweier separater Arbeitspositionen.

7. Wechseln Sie zu **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**. Wählen Sie Ihren Artikel und dann **Lagerbestand verwalten** \> **Ansicht** \> **Transaktionen** aus.

    ![Auftragsgebundene Reservierung als Lagerbuchungstyp](media/Inventory-transactions-for-order-committed-reservation.png)

8. Überprüfen Sie die Lagerbuchungen, die mit der Reservierung der Auftragsposition verknüpft sind.

    - Eine Transaktion, bei der das Feld **Referenz** auf **Auftrag** gesetzt ist und das Feld **Abgang** auf **Physisch reserviert**, stellt die Auftragspositionsreservierung für Bestandsdimensionen oberhalb der Ebene **Lagerort** dar. Entsprechend der Bestandsreservierungshierarchie des Artikels sind diese Dimensionen Standort, Lagerort und Bestandsstatus.
    - Eine Transaktion, bei der das Feld **Referenz** auf **Auftragsgebundene Reservierung** und das Feld **Abgang** auf **Physisch reserviert** gesetzt ist, stellt die Auftragspositionsreservierung für die spezifische Charge und alle Bestandsdimensionen darüber dar. Entsprechend der Bestandsreservierungshierarchie des Artikels sind diese Dimensionen Chargenummer und Lagerort. In diesem Beispiel ist der Lagerort **Bulk-001**.

9. Wählen Sie im Auftragskopf **Lagerort** \> **Aktionen** \> **Für Lagerort freigeben** aus. Die Bestellposition ist jetzt gewellt und eine Ladung sowie Arbeit werden erstellt.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Überprüfen und Verarbeiten von Lagerarbeit mit auftragsgebundenen Chargennummern

1. Wählen Sie auf dem Inforegister **Auftragspositionen** **Lagerort** \> **Arbeitsdetails** aus.

    Die Arbeit, die den Kommissionierungsvorgang für Chargenmengen erledigt, die für die Kundenauftragsposition zugesagt sind, weist folgende Merkmale auf:

    - Das System verwendet Arbeitsvorlagen, jedoch keine Lagerplatzrichtlinien, um Arbeit zu generieren. Alle Standardeinstellungen, die für Arbeitsvorlagen definiert sind, z. B. eine maximale Anzahl von Entnahmepositionen oder eine bestimmte Maßeinheit, werden angewendet, um festzulegen, wann neue Arbeit angelegt werden sollte. Die Regeln, die mit Lagerplatzrichtlinien zum Identifizieren von Entnahmepositionen verknüpft sind, werden nicht berücksichtigt, da die auftragsgebundene Reservierung bereits alle Bestandsdimensionen angibt. Diese Bestandsdimensionen enthalten Dimensionen auf Lagerortebene. Daher erbt die Arbeit diese Dimensionen, ohne dass Lagerplatzrichtlinien berücksichtigt werden müssen.
    - Die Chargennummer wird nicht an der Entnahmeposition angezeigt (im Gegensatz zur Arbeitsposition, die für einen Artikel mit verknüpfter *Charge oberhalb\[Lagerplatz\]*-Reservierungshierarchie erstellt wird.) Stattdessen werden die von-Chargennummer und alle anderen Lagerdimensionen in der Lagerbuchung der Arbeitsposition angezeigt, auf die von den verknüpften Lagerbuchungen verwiesen wird.

        ![Lagerort-Lagerbuchungen für Arbeit, die aus einer auftragsgebundenen Reservierung stammt](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Nachdem die Arbeit erstellt wurde, wird die Lagerbuchung, bei der das Feld **Referenz** auf **Auftragsgebundene Reservierung** gesetzt ist, entfernt. Die Lagerbuchung, bei das Feld **Referenz** auf **Arbeit** gesetzt ist, enthält nun die physische Reservierung für alle Lagerdimensionen der Menge.

        Arbeitsgänge am Arbeitsort können auf die übliche Art und Weise abgewickelt werden. Die Anweisungen auf dem Mobilgerät weisen die Arbeitskraft jedoch an, eine bestimmte Chargennummer auszuwählen. In Lagerortumgebungen, bei denen Lagerorte durch Ladungsträger gesteuert werden, kann eine Arbeitskraft, nachdem sie den Lagerort erreicht hat, der die gleiche Charge auf mehreren Ladungsträgern lagert, von einem beliebigen Ladungsträger entnehmen, der nicht bereits reserviert ist (beispielsweise von einer anderen auftragsgebundenen Reservierung oder einer Arbeit, die von einer Reservierung diesen Typs stammt).

        Wenn es sich als unpraktisch herausstellt, von dem Lagerort zu entnehmen, der in der Arbeitsposition angegeben ist, kann der Lagerortoperator eine der folgenden Aktionen verwenden, um die Kommissionierung der bestimmten Charge zu einem passenderen Lagerort umleiten.

        - Der Standardaktion **Lagerplatzüberschreibung** auf einem mobilen Gerät (vorausgesetzt, die Lagerort-Arbeitskräfte-Einstellung **Außerkraftsetzen des Entnahmeorts zulassen** ist aktiviert)
        - Die Aktion **Lagerplatz ändern** auf der Seite **Arbeitslistendetails**. 

2. Beenden Sie auf dem mobilen Gerät die Kommissionierung und Platzierung der Arbeit.

    Die Menge von **10** für Chargennummer **B11** wird nun für die Auftragsposition und im Lagerort **Baydoor** platziert. Zu diesem Zeitpunkt kann es auf den LKW verladen und an die Adresse des Kunden versendet werden.

## <a name="flexible-license-plate-reservation"></a>Flexible Ladungsträgerreservierung

### <a name="business-scenario"></a>Geschäftsszenario

In diesem Szenario verwendet ein Unternehmen die Lagerortverwaltung und die Arbeitsverarbeitung und erledigt die Ladungsplanung auf der Ebene einzelner Paletten/Container außerhalb des Supply Chain Management, bevor die Arbeit erstellt wird. Diese Behälter werden durch Ladungsträger in den Bestandsdimensionen dargestellt. Daher müssen für diesen Ansatz den Auftragspositionen bestimmte Ladungsträger vorab zugewiesen werden, bevor die Kommissionierarbeit abgeschlossen wird. Das Unternehmen sucht nach Flexibilität bei der Handhabung der Ladungsträgerreservierungsregeln, damit folgende Verhaltensweisen auftreten:

- Ein Ladungsträger kann aufgezeichnet und reserviert werden, wenn der Auftrag vom Verkäufer entgegengenommen wird. Er kann nicht aufgrund anderer Bedarfe verwendet werden. Mit diesem Verhalten wird gewährleistet, dass der vorgesehene Ladungsträger an den Kunden gesendet wird.
- Wenn der Ladungsträger noch keiner Auftragsposition zugeordnet ist, kann das Lagerpersonal während der Kommissionierarbeiten nach Abschluss der Registrierung und Reservierung des Auftrags einen Ladungsträger auswählen.

### <a name="turn-on-flexible-license-plate-reservation"></a>Flexible Ladungsträgerreservierung aktivieren

Bevor Sie die flexible Ladungsträgerreservierung verwenden können, müssen zwei Funktionen in Ihrem System aktiviert sein. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktionen überprüfen und sie gegebenenfalls aktivieren. Sie müssen die Funktionen in der folgenden Reihenfolge aktivieren:

1. **Funktionsname:** *Flexible Dimensionsreservierung auf Lagerebene*
1. **Funktionsname:** *Flexible auftragsgebundene Ladungsträgerreservierung*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Einen bestimmten Ladungsträger für den Auftrag reservieren

Um die Ladungsträgerresevierung für eine Bestellung zu aktivieren, müssen Sie das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** für die Ebene **Ladungsträger** auf der Seite **Bestandsreservierungshierarchien** für die Hierarchie auswählen, die dem entsprechenden Artikel zugeordnet ist.

![Seite „Bestandsreservierungshierachien“ für eine flexible Ladungsträgerreservierungshierarchie](media/Flexible-LP-reservation-hierarchy.png)

Sie können die Ladungsträgerreservierungshierarchie für den Auftrag zu jedem Zeitpunkt Ihrer Bereitstellung aktivieren. Diese Änderung wirkt sich nicht auf Reservierungen oder offene Lagerarbeiten aus, die vor der Änderung erstellt wurden. Sie können jedoch das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** nicht deaktivieren, wenn offene ausgehende Lagerbuchungen den Abgangsstatus *Bestellt*, *Bestellt reserviert* oder *Physisch reserviert* für mindestens einen Artikel haben, der mit der Reservierungshierarchie verknüpft ist.

Selbst wenn das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** für die Ebene **Ladungsträger** aktiviert ist, ist es *nicht* möglich, in dem Auftrag einen bestimmten Ladungsträger zu reservieren. In diesem Fall gilt die Standardlagerort-Operationslogik, die auf die Reservierungshierarchie zutrifft.

Um einen bestimmten Ladungsträger zu reservieren, müssen Sie einen Prozess mit [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) verwenden. In der Anwendung können Sie diese Reservierung direkt aus einem Auftrag über die Option **Auftragsgebundene Reservierungen nach Ladungsträger** des Befehls **In Excel öffnen**. In den Entitätsdaten, die im Excel-Add-In geöffnet werden, müssen Sie die folgenden reservierungsbezogenen Daten eingeben und dann **Veröffentlichen** auswählen, um die Daten an das Supply Chain Management zurückzusenden:

- Referenz (nur der Wert *Auftrag* wird unterstützt)
- Auftragsnummer (der Wert kann aus dem Los abgeleitet werden)
- Loskennung
- Kennzeichen
- Leistung

Wenn Sie einen bestimmten Ladungsträger für einen Artikel mit Chargenverfolgung reservieren müssen, verwenden Sie die Seite **Chargenreservierung** wie im Abschnitt [Auftragsdetails](#sales-order-details) beschrieben.

Wenn die Auftragsposition, die eine auftragsgebundene Ladungsträgerreservierung verwendet, durch Lageroperationen verarbeitet wird, werden keine Lagerplatzrichtlinien verwendet.

Wenn eine Lagerarbeitsaufgabe aus Positionen besteht, die einer vollständigen Palette entsprechen und ladungsträgergebundene Mengen haben, können Sie den Kommissionierprozess mithilfe eines Menüelements für mobile Geräte optimieren, bei denen die Option **Mit Ladungsträger handhaben** auf *Ja* gesetzt ist. Ein Lagerarbeiter kann dann einen Ladungsträger scannen, um eine Kommissionierung abzuschließen, anstatt die Artikel aus der Arbeit einzeln scannen zu müssen.

![Menüpunkt für mobiles Gerät, bei dem die Option „Mit Ladungsträger handhaben“ auf „Ja“ gesetzt ist](media/Handle-by-LP-menu-item.png)

Da die Funktionalität **Mit Ladungsträger handhaben** keine Arbeit unterstützt, die mehrere Paletten abdeckt, ist es besser, für verschiedene Ladungsträger separate Arbeitsaufgaben zu nutzen. Um diesen Ansatz zu verwenden, fügen Sie das Feld **Auftragsgebundene Ladungsträger-ID** als Arbeitskopfzeilenumbruch auf der Seite **Arbeitsvorlage** hinzu.

> [!NOTE]
> Für den Prozess der auftragsgebundenen Arbeitserstellung wird den Kommissionierarbeitspositionen ein Wert für die Dimension „auftragsgebundener Bestand“ zugewiesen, und es wird nicht möglich sein, den Kennzeichenwert direkt einzusehen. Nur der *Benutzergeleitet*-Prozess wird beim Einrichten eines Menüelements für mobile Geräte unterstützt.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Beispielszenario: auftragsgebundenen Ladungsträgerreservierung einrichten und verarbeiten

Dieses Szenario zeigt, wie man eine auftragsgebundene Ladungsträgerreservierung einrichtet und verarbeitet.

### <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Dieses Szenario verweist auf Werte und Datensätze, die in den für das Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie das Szenario mithilfe der in diesem Thema dargestellten Werte bearbeiten möchten, müssen Sie in einer Umgebung arbeiten, in der die Standarddemodaten installiert sind. Außerdem müssen Sie die juristische Person **USMF** auswählen, bevor Sie beginnen.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Erstellen Sie eine Bestandsreservierungshierarchie, die eine Ladungsträgerreservierung erlaubt

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> Reservierungshierachie**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Name** einen Wert ein (beispielsweise *Flexibler LP*).
1. Geben Sie im Feld **Beschreibung** einen Wert ein (beispielsweise *Flexible LP-Reservierung*).
1. Wählen Sie in der Liste **Ausgewählt** die **Chargennummer**, **Seriennummer** und den **Besitzer**.
1. Wählen Sie die Schaltfläche **Entfernen** aus ![Rückwärtspfeil](media/backward-button.png), um die Auswahl in die Liste **Verfügbar** zu verschieben.
1. Wählen Sie **OK**.
1. In der Zeile mit der **Ladungsträger**-Dimensionsebene aktivieren Sie das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen**. Die Ebene **Lagerplatz** wird automatisch ausgewählt und Sie können das Kontrollkästchen für diese nicht deaktivieren.
1. Wählen Sie **Speichern** aus.

### <a name="create-two-released-products"></a>Zwei freigegebene Produkte erstellen

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Neues freigegebenes Produkt** die folgenden Werte fest:

    - **Produktnummer:** *Artikel 1*
    - **Artikelnummer:** *Artikel 1*
    - **Lagersteuerungsgruppe:** *FIFO*
    - **Artikelgruppe:** *Audio*
    - **Lagerdimensionsgruppe:** *Lagerort*
    - **Rückverfolgungsangabengruppe:** *Keine*
    - **Reservierungshierarchie:** *Flexibler LP*

1. Wählen Sie **OK** aus, um das Produkt zu erstellen und das Dialogfeld zu schließen.
1. Das neue Produkt wird geöffnet. Geben Sie im Inforegister **Lagerort** im Feld **Einheitennummernkreisgruppen-ID** *ea* ein.
1. Wiederholen Sie die vorherigen Schritte, um ein zweites Produkt mit denselben Einstellungen zu erstellen, geben Sie aber bei **Produktnummer** und **Artikelnummer** *Artikel 2* ein.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Ansicht** **Verfügbarer Lagerbestand** aus. Dann wählen Sie **Mengenanpassung**.
1. Passen Sie den verfügbaren Lagerbestand der neuen Artikel wie in der folgenden Tabelle angegeben an.

    | Artikel  | Lagerort | Ziel | Kennzeichen | Leistung |
    |-------|-----------|----------|---------------|----------|
    | Artikel 1 | 24        | FL-010   | LP01          | 10       |
    | Artikel 1 | 24        | FL-011   | LP02          | 10       |
    | Artikel 2 | 24        | FL-010   | LP01          | 5        |
    | Artikel 2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > Sie müssen die beiden Ladungsträger erstellen und Lagerplätze verwenden, die gemischte Artikel zulassen, z. B. *FL-010* und *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Legen Sie einen Auftrag an und reservieren Sie einen bestimmten Ladungsträger

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *24*

1. Wählen Sie **OK** aus, um das Dialogfeld **Auftrag erstellen** zu schließen und den neuen Auftrag zu öffnen.
1. Fügen Sie im Inforegister **Auftragspositionen** eine Position mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *Artikel 1*
    - **Menge** *10*

1. Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *Artikel 2*
    - **Menge** *5*

1. Wählen Sie **Speichern** aus.
1. Im Inforegister **Positionsdetails** in der Registerkarte **Einrichtungen** notieren Sie die **Los-ID** für jede Position. Diese Werte werden bei der Reservierung bestimmter Ladungsträger benötigt.

    > [!NOTE]
    > Um einen bestimmten Ladungsträger zu reservieren, müssen Sie die Datenentität **Auftragsgebundene Reservierungen nach Ladungsträger** verwenden. Um einen Artikel mit Chargenverfolgung auf einem bestimmten Ladungsträger zu reservieren, verwenden Sie die Seite **Chargenreservierung** wie im Abschnitt [Auftragsdetails](#sales-order-details) beschrieben.
    >
    > Wenn Sie den Ladungsträger direkt in die Auftragsposition eingeben und bestätigen, wird die Lagerverwaltungsverarbeitung für die Position nicht verwendet.

1. Wählen Sie **In Microsoft Office** öffnen, **Auftragsgebundene Reservierungen nach Ladungsträger** und laden Sie die Datei herunter.
1. Öffnen Sie die heruntergeladene Datei in Excel und wählen Sie **Bearbeiten aktiveren**, damit das Excel Add-In ausgeführt werden kann.
1. Wenn Sie das Excel-Add-In zum ersten Mal ausführen, klicken Sie auf **Diesem Add-In vertrauen**.
1. Klicken Sie nach Aufforderung auf **Anmelden**, und melden Sie sich mit den Anmeldeinformationen an, mit denen Sie sich beim Supply Chain Management angemeldet haben.
1. Um einen Artikel auf einem bestimmten Ladungsträger zu reservieren, wählen Sie im Excel-Add-In die Option **Neu**, um eine Reservierungszeile hinzuzufügen, und legen Sie dann die folgenden Werte fest:

    - **Los-ID:** Geben Sie die **Los-ID** ein, die Sie für die Auftragsposition für *Artikel 1* gefunden haben.
    - **Ladungsträger:** *LP02*
    - **Reservieren von Lagermenge:** *10*

1. Wählen Sie **Neu** aus, um eine weitere Reservierungszeile hinzuzufügen, und legen Sie die folgenden Werte fest:

    - **Los-ID:** Geben Sie die **Los-ID**, die Sie für die Auftragsposition für *Artikel 2* gefunden haben.
    - **Ladungsträger:** *LP02*
    - **Reservieren von Lagermenge:** *5*

1. Wählen Sie im Excel-Add-In die Option **Veröffentlichen** aus, um die Daten an das Supply Chain Management zurückzusenden.

    > [!NOTE]
    > Die Reservierungszeile wird im System nur angezeigt, wenn die Veröffentlichung fehlerfrei abgeschlossen wurde.

1. Gehen Sie zurück zum Supply Chain Management. 
1. Um die Reservierung des Artikels zu überprüfen, klicken Sie im Inforegister **Auftragspositionen** im Menü **Bestand** auf **Verwalten \> Reservierung**. Beachten Sie, dass für die Auftragsposition für *Artikel 1* ein Bestand von *10* reserviert ist und für die Auftragsposition für *Artikel 2* ein Bestand von *5*.
1. Um Lagerbuchungen zu überprüfen, die sich auf die Reservierung der Auftragsposition beziehen, klicken Sie im Inforegister **Auftragspositionen** im Menü **Bestand** auf **Ansicht \> Buchungen**. Beachten Sie, dass es zwei Buchungen gibt, die sich auf die Reservierung beziehen: eine, bei der das Feld **Referenz** auf *Auftrag* steht und eine, bei der das Feld **Referenz** auf *Auftragsgebundene Reservierung* steht.

    > [!NOTE]
    > Eine Buchung, bei der das Feld **Referenz** auf *Auftrag* gesetzt ist, steht für die Auftragspositionsreservierung für Bestandsdimensionen, die über der Ebene **Lagerplatz** liegen (Standort, Lagerort und Bestandsstatus). Eine Buchung, bei der die das Feld **Referenz** auf *Auftragsgebundene Reservierung* steht, steht für die Auftragspositionsreservierung für den bestimmten Ladungsträger und den Lagerplatz.

1. Um den Auftrag freizugeben, gehen Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Aktivitäten** auf **Für Lagerort freigeben**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Lagerarbeiten mit zugewiesenen auftragsgebundenen Ladungsträgern überprüfen und verarbeiten

1. Wählen Sie im Inforegister **Auftragspositionen** im Menü **Lagerort** die Option **Arbeitsdetails** aus.

    Wie bei der Reservierung für eine bestimmte Charge verwendet das System keine Lagerplatzrichtlinien, wenn es die Arbeit für den Auftrag erstellt, der die Ladungsträgerreservierung verwendet. Da die auftragsgebundene Reservierung alle Bestandsdimensionen einschließlich des Lagerplatzes spezifiziert, müssen Lagerplatzrichtlinien nicht verwendet werden, da diese Bestandsdimensionen nur in die Arbeit eingegeben werden. Sie werden im Abschnitt **Aus Bestandsdimensionen** auf der Seite **Arbeitslagerbuchungen** angezeigt.

    > [!NOTE]
    > Nachdem die Arbeit erstellt wurde, wird die Lagerbuchung, bei der das Feld **Referenz** auf *Auftragsgebundene Reservierung* gesetzt ist, entfernt. Die Lagerbuchung, bei der das Feld **Referenz** auf *Arbeit* gesetzt ist, enthält nun die physische Reservierung für alle Lagerdimensionen der Menge.

1. Beenden Sie die Kommissionierung und Platzierung der Arbeit auf dem mobilen Gerät mithilfe eines Menüelements, in dem das Kontrollkästchen **Mit Ladungsträger handhaben** aktiviert ist.

    > [!NOTE]
    > Die Funktionalität **Mit Ladungsträger handhaben** hilft Ihnen bei der Verarbeitung des kompletten Ladungsträgers. Wenn Sie einen Teil des Ladungsträgers verarbeiten müssen, können Sie diese Funktionalität nicht verwenden.
    >
    > Wir empfehlen, dass Sie für jeden Ladungsträger separate Arbeiten erstellen lassen. Verwenden Sie dafür die Funktion **Arbeitskopfzeilenumbrüche** auf der Seite **Arbeitsvorlage**.

    Der Bestandsträger *LP02* wird nun für die Auftragspositionen kommissioniert und an den Lagerplatz *Ladebereichstor* gebracht. Zu diesem Zeitpunkt kann er verladen und an den Kunden versendet werden.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Ausnahmenbehandlung von Lagerortarbeit mit auftragsgebundenen Chargennummern

Die Lagerarbeit für die Kommissionierung von auftragsgebundenen Chargennummern unterliegt denselben standardmäßigen Lagerortausnahmebehandlungen und -Aktionen wie die reguläre Arbeit. Im Allgemeinen kann die offene Arbeit oder Arbeitsposition storniert werden. Sie kann unterbrochen werden, weil ein Lagerort voll ist, sie kann kurz entnommen werden und sie kann aufgrund einer Bewegung aktualisiert werden. Ebenso kann die kommissionierte Arbeit, die bereits erledigt wurde, reduziert oder rückgängig gemacht werden.

Für alle diese Ausnahmebehandlungsaktionen gilt die folgende Grundregel: Die für den Kunden reservierte Chargennummer kann niemals durch eine andere Chargennummer ersetzt werden, ihre Lagerdimensionen (Lagerort und Ladungsträger) können jedoch durch eine manuelle Aktualisierung seitens des Benutzers geändert werden oder durch eine automatische Aktualisierung seitens des Systems. Die automatische Aktualisierung basiert auf der gleichen zufälligen Zuweisung von Lagerdimensionen, die galten, als eine bestimmte Charge automatisch reserviert wurde, aber keine Lagerdimensionen angegeben waren.

### <a name="example-scenario"></a>Beispielszenario

Ein Beispiel für dieses Szenario ist eine Situation, in der zuvor abgeschlossene Arbeiten teilweise rückgängig gemacht wird, indem die Funktion **Entnommene Menge reduzieren** verwendet wird. In diesem Beispiel wird davon ausgegangen, dass Sie die im [Beispielszenario: Chargennummernzuteilung](#Example-batch-allocation) beschriebenen Schritte bereits ausgeführt haben. Es knüpft an dieses Beispiel an.

1. Gehen Sie zu **Lagerortverwaltung** \> **Ladungen** \> **Aktive**.
2. Wählen Sie die Ladung aus, die im Zusammenhang mit dem Versand Ihres Auftrags erstellt wurde.
3. Wählen Sie auf dem Inforegister für **Auftragspositionen laden** die Option **Entnommene Menge reduzieren** aus.
4. Wählen Sie auf der Seite **Entnommene Menge reduzieren** im Feld **An Lagerplatz verschieben** **FL-001** aus.
5. Wählen Sie im Feld **Auf Ladungsträger verschieben** **LP33** aus.
6. Geben Sie im Raster des Felds **Bestandsmenge, deren Entnahme rückgängig gemacht werden soll** **10** ein.
7. Wählen Sie **OK**.

Hier sind die Ergebnisse der Entnahme-Aktion:

- Der Status der zuvor abgeschlossenen Arbeit wird auf **Storniert** gesetzt.
- Neue Arbeit vom Typ **Lagerumlagerung** wird für die nicht entnommene Menge von **10** für die Chargennummer **B11** erstellt. Diese Arbeit repräsentiert die Verschiebung vom Lagerort **Baydoor** zum Ladungsträger **LP33** im Lagerort **FL-001**. Der Status wird auf **Abgeschlossen** gesetzt.
- Das System reserviert die ursprünglich bestellte Chargennummer erneut und weist die IDs des Lagerorts und des Ladungsträgers zu. (Dieser Vorgang entspricht dem Ausführen der Funktion **Position reservieren** für die Bestellposition einer bestimmten Chargennummer). Als Ergebnis wird Charge **B11** nun als „Zugesagt“ auf dem Inforegister für **Chargennummern für Quellposition zugesagt** der Seite **Chargenreservierung** angezeigt und das Feld **Reservierung** enthält eine Menge von **10** für die Chargennummer **B11**. Zusätzlich wird das Feld **Lagerort** auf **FL-001** gesetzt und das Feld **Ladungsträger** auf **LP11**. (Sie können diese Felder zum Raster hinzufügen, wenn sie nicht sichtbar sind.)

Die folgenden Tabellen bieten eine Übersicht darüber, wie das System die auftragsgebundene Chargenreservierung für bestimmte Lagerortaktionen handhabt. Um den Inhalt in den Tabellen zu interpretieren, nehmen Sie an, dass jede Lagerortaktion im Kontext einer vorhandenen Lagerarbeit ausgeführt wird, die aus einer auftragsgebundenen Chargenreservierung stammt, oder dass sich die Ausführung jeder Lageraktion auf eine Arbeit dieses Typs auswirkt.

> [!NOTE]
> In diesen Tabellen gibt die Spalte „Chargenmenge verfügbar“ an, ob eine Chargenmenge zusätzlich zu der Menge verfügbar ist, die entweder bereits für die aktuellen auftragsgebundenen Reservierungen reserviert ist oder die bereits von der Lagerarbeit reserviert wurde, die aus Reservierungen dieser Art stammt.

#### <a name="override-the-pick-location-on-the-open-work"></a>Überschreiben des Entnahmeplatzes bei offener Arbeit

<table>
<thead>
<tr>
<th>Wichtige Einrichtungsparameter</th>
<th>Chargenmenge ist verfügbar</th>
<th>Wichtige Schritte für den Benutzer</th>
<th>Lagerarbeit</th>
<th>Auftragsgebundene Chargenreservierung</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Die Option <strong>Außerkraftsetzen des Entnahmeorts zulassen</strong> ist für die Arbeitskraft aktiviert.</td>
<td>Ja</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Lagerplatz überschreiben</strong> in der Warehouse Management Mobile App aus, wenn Sie mit der Entnahmearbeit beginnen.</li>
<li>Wählen Sie die Option für <strong>Vorschlagen</strong> aus.</li>
<li>Bestätigen Sie den neuen Lagerort, der basierend auf der Verfügbarkeit der Chargenmenge vorgeschlagen wird.</li>
</ol>
</td>
<td>Bei der aktuellen Arbeit werden folgende Aktionen ausgeführt:
<ul>
<li>Der Ort der Entnahmeposition wird auf den neuen Lagerort aktualisiert. (Wenn der Lagerort durch einen Ladungsträger gesteuert wird, wird ein zufällig ausgewählter Ladungsträger zur Lagerbuchung für Arbeit zugewiesen und die Arbeitskraft kann von jedem Ladungsträger mit verfügbarer Menge entnehmen.)</li>
<li>Ist die Menge am neuen Lagerort auf mehreren Ladungsträgern verfügbar, wird die ursprüngliche Entnahmeposition in mehrere Positionen aufgeteilt, um den einzelnen Ladungsträgern zu entsprechen.</li>
</ul>
</td>
<td>Nicht zutreffend</td>
</tr>
<tr>
<td>Nr.</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Lagerplatz überschreiben</strong> in der Warehouse Management Mobile App aus, wenn Sie mit der Entnahmearbeit beginnen.</li>
<li>Geben Sie einen Lagerort manuell ein.</li>
</ol>
</td>
<td>Die Aktion <strong>Standort überschreiben</strong> ist nicht möglich. Sie schlägt fehl und löst einen Fehler aus.</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Schaltfläche „Voll“ – Teilt eine Arbeitsposition aufgrund eines Überlaufs am Benutzerstandort

<table>
<thead>
<tr>
<th>Wichtige Einrichtungsparameter</th>
<th>Chargenmenge ist verfügbar</th>
<th>Wichtige Schritte für den Benutzer</th>
<th>Lagerarbeit</th>
<th>Auftragsgebundene Chargenreservierung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Die Option <strong>Aufteilung der Arbeit zulassen</strong> ist bei mobilen Geräten im Menüelement aktiviert.</td>
<td>Nicht zutreffend</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Voll</strong> in der Warehouse Management Mobile App aus, wenn Sie die Entnahmearbeit verarbeiten.</li>
<li>Geben Sie im Feld <strong>Entnahmemenge</strong> eine Teilmenge der erforderlichen Entnahme ein, um die volle Kapazität anzuzeigen.</li>
</ol>
</td>
<td>
<ul>
<li>Bei der aktuellen Arbeit wird die Menge auf die verbleibende Menge aktualisiert, die kommissioniert werden muss.</li>
<li>Für die kommissionierte Menge wird eine neue Arbeit angelegt und abgeschlossen.</li>
</ul></td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Reduzieren der entnommenen Menge für abgeschlossene Arbeit (von einer Ladung)

<table>
<thead>
<tr>
<th>Wichtige Einrichtungsparameter</th>
<th>Chargenmenge ist verfügbar</th>
<th>Wichtige Schritte für den Benutzer</th>
<th>Lagerarbeit</th>
<th>Auftragsgebundene Chargenreservierung</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Nicht zutreffend</td>
<td>Ja</td>
<td>
<ol>
<li>Öffnen Sie die Seite <strong>Entnommene Menge reduzieren</strong> über die Ladungsposition.</li>
<li>Geben Sie die gesamte Menge an, deren Entnahme rückgängig gemach werden soll.</li>
<li>Wählen Sie einen „Verschieben nach“-Ladungsträger aus.</li>
</ol>
</td>
<td>
<ul> 
<li>Arbeit, die mit der Ladungsposition verbunden sind, wird abgebrochen.</li>
<li>Für die Lagerumlagerung wird eine neue Arbeit angelegt und abgeschlossen.</li>
</ul>
</td>
<td>Die Menge wird für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>Siehe vorherige Zeile.</td>
<td>Die Menge wird für die gleiche Charge und für den gleichen Lagerort und den gleichen Ladungsträger erneut reserviert (wenn der Lagerort durch einen Ladungsträger gesteuert wird), die während des Zurücknehmens der Entnahme eingegeben wurden.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Verschieben eines Artikels innerhalb eines Lagerorts

> [!NOTE]
> Diese Lagerortaktion gilt nur für die Verlagerung vom Typ **Arbeitserstellungsprozess**, nicht für die Verlagerung nach Vorlage.

<table>
<thead>
<tr>
<th>Wichtige Einrichtungsparameter</th>
<th>Chargenmenge ist verfügbar</th>
<th>Wichtige Schritte für den Benutzer</th>
<th>Lagerarbeit</th>
<th>Auftragsgebundene Chargenreservierung</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Die Option <strong>Bewegung von Bestand mit zugeordneter Arbeit zulassen</strong> ist für die Arbeitskraft aktiviert.</td>
<td>Ja</td>
<td>
<ol>
<li>Beginnen Sie eine Verlagerung in der Warehouse Management Mobile App.</li>
<li>Geben Sie „Von“- und „Nach“-Lagerorte ein.</li>
</ol></td>
<td>
<ul>
<li>Bei allen vorhandenen Arbeiten, die von der Verlagerung betroffen ist, wird der Entnahmeort auf den neuen „Nach“-Lagerort aktualisiert.</li>
<li>Für die Lagerumlagerung wird eine neue Arbeit angelegt und abgeschlossen.</li>
</ul>
</td>
<td>Alle vorhandenen Reservierungen, die von der Mengenverlagerung vom angegebenen Lagerort betroffen sind, werden für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>Siehe vorherige Zeile.</td>
<td>Alle vorhandenen Reservierungen, die von der Mengenverlagerung vom angegebenen Lagerort betroffen sind, werden für dieselbe Charge und den neuen Zielstandort und den Ladungsträger erneut reserviert (sofern der Lagerort durch einen Ladungsträger gesteuert wird).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Stornieren der entnommenen Menge für abgeschlossene Arbeit (von einer Ladung oder Welle)

<table>
<thead>
<tr>
<th>Wichtige Einrichtungsparameter</th>
<th>Chargenmenge ist verfügbar</th>
<th>Wichtige Schritte für den Benutzer</th>
<th>Lagerarbeit</th>
<th>Auftragsgebundene Chargenreservierung</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Nicht zutreffend</td>
<td>Ja</td>
<td>
<ol>
<li>Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</li>
<li>Wählen Sie auf der Anforderungsseite die Option <strong>Artikel am aktuellen Lagerplatz belassen</strong> aus.</li>
</ol>
</td>
<td>Arbeit, die mit der Ladung verbunden ist, wird abgebrochen.</td>
<td>Die Menge wird für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>Siehe vorherige Zeile.</td>
<td>Die Menge wird für dieselbe Charge und für den Lagerort und den Ladungsträger erneut reserviert, an dem bzw. bei dem die Menge bei der Stornierung belassen wurde.</td>
</tr>
<tr>
<td>Ja</td>
<td>
<ol>
<li>Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</li>
<li>Wählen Sie auf der Anforderungsseite die Option <strong>Artikel diesem Lagerplatz zuweisen</strong> aus.</li>
</ol>
</td>
<td>
<ul>
<li>Die aktuelle Arbeit wird storniert.</li>
<li>Für die Lagerumlagerung wird eine neue Arbeit angelegt und abgeschlossen.</li>
</ul>
</td>
<td>Die Menge wird für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>Siehe vorherige Zeile.</td>
<td>Die Menge wird für dieselbe Charge und für den Lagerort und den Ladungsträger reserviert, zu dem die Menge bei der Stornierung zugewiesen war.</td>
</tr>
<tr>
<td>Ja/Nein</td>
<td>
<ol>
<li>Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</li>
<li>Wählen Sie auf der Anforderungsseite die Option <strong>Artikel an diesen Lagerplatz umlagern</strong> aus.</li>
</ol>
</td>
<td>Eine Stornierung wird nicht unterstützt.</td>
<td>Nicht zutreffend</td>
</tr>
<tr>
<td>Ja/Nein</td>
<td>
<ol>
<li>Öffnen Sie die Seite <strong>Arbeit stornieren</strong>.</li>
<li>Wählen Sie auf der Anforderungsseite die Option <strong>Artikel auf der Grundlage von Lagerplatzrichtlinien umlagern</strong> aus.</li>
</ol>
</td>
<td>Eine Stornierung wird nicht unterstützt. </td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Kurzentnahme einer Menge – Registrieren Sie die Menge als Menge, die physisch nicht am Lagerort/auf dem Ladungsträger vorhanden war, als Sie die Entnahmearbeiten durchführten

<table>
<thead>
<tr>
<th>Wichtige Einrichtungsparameter</th>
<th>Chargenmenge ist verfügbar</th>
<th>Wichtige Schritte für den Benutzer</th>
<th>Lagerarbeit</th>
<th>Auftragsgebundene Chargenreservierung</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Keine</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Nein</strong> ist.</td>
<td>Ja</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Entnahme mit unzureichender Menge</strong> in der Warehouse Management Mobile App aus, wenn Sie die Entnahmearbeit durchführen.</li>
<li>Geben Sie im Feld <strong>Entnahmemenge</strong> den Wert <strong>0</strong> (Null) ein.</li>
<li>Geben Sie im Feld <strong>Grund</strong> <strong>Keine Neuzuteilung</strong> ein.</li>
</ol>
</td>
<td>
<ul>
<li>Die aktuelle Arbeit wird geschlossen und die Entnahmemenge ist 0 (Null).</li>
<li>Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</li>
</ul>
</td>
<td>Die Menge wird für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>
<ul>
<li>Die Kurzentnahme-Aktion schlägt fehl und es wird ein Fehler ausgegeben.</li>
<li>Die aktuelle Arbeit bleibt offen.</li>
</ul>
</td>
<td>Nicht zutreffend</td>
</tr>
<tr>
<td rowspan='2'>Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Keine</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Ja</strong> ist.</td>
<td>Ja</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Entnahme mit unzureichender Menge</strong> in der Warehouse Management Mobile App aus, wenn Sie die Entnahmearbeit durchführen.</li>
<li>Geben Sie im Feld <strong>Entnahmemenge</strong> den Wert <strong>0</strong> (Null) ein.</li>
<li>Geben Sie im Feld <strong>Grund</strong> <strong>Keine Neuzuteilung</strong> ein.</li>
</ol>
</td>
<td>
<ul>
<li>Die aktuelle Arbeit wird geschlossen und die Entnahmemenge ist 0 (Null).</li>
<li>Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</li>
</ul>
</td>
<td>Alle vorhandenen Reservierungen, die von der Mengenanpassung im Lagerort der Kurzentnahme betroffen sind, werden für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>Siehe vorherige Zeile.</td>
<td>Alle vorhandenen Reservierungen, die von der Mengenanpassung im Lagerort der Kurzentnahme betroffen sind, werden entfernt.</td>
</tr>
<tr>
<td>Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Manuell</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Nein/Ja</strong> ist. Zusätzlich wird die Option <strong>Manuelle Artikelneuzuordnung zulassen</strong> für die Arbeitskraft aktiviert.</td>
<td>Ja</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Entnahme mit unzureichender Menge</strong> in der Warehouse Management Mobile App aus, wenn Sie die Entnahmearbeit durchführen.</li>
<li>Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</li>
<li>Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit manueller Neuzuteilung</strong> aus.</li>
<li>Wählen Sie den Lagerort/Ladungsträger in der Liste aus.</li>
</ol>
</td>
<td>
<ul>
<li>Bei der aktuellen Arbeit werden folgende Aktionen ausgeführt:
<ul>
<li>Die Entnahmeposition wird geschlossen und die Entnahmemenge ist 0 (Null).</li>
<li>Die Einlagerungsposition wird storniert.</li>
<li>Eine neue Entnahmeposition wird erstellt. Es wird der Lagerort/Ladungsträger verwendet, den der Benutzer ausgewählt hat.</li>
<li>Eine neue Einlagerungsposition wird erstellt.</li>
</ul>
</li>
<li>Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</li>
</ul>
</td>
<td>Nicht zutreffend</td>
</tr>
<tr>
<td>Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Manuell</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Nein</strong> ist. Zusätzlich wird die Option <strong>Manuelle Artikelneuzuordnung zulassen</strong> für die Arbeitskraft aktiviert.</td>
<td>Nr.</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Entnahme mit unzureichender Menge</strong> in der Warehouse Management Mobile App aus, wenn Sie die Entnahmearbeit durchführen.</li>
<li>Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</li>
<li>Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit manueller Neuzuteilung</strong> aus.</li>
</ol>
</td>
<td>Die Kurzentnahme-Aktion schlägt fehl und es wird ein Fehler ausgegeben.</td>
<td>Nicht zutreffend</td>
</tr>
<tr>
<td>Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Manuell</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Ja</strong> ist. Zusätzlich wird die Option <strong>Manuelle Artikelneuzuordnung zulassen</strong> für die Arbeitskraft aktiviert.</td>
<td>Nr.</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Entnahme mit unzureichender Menge</strong> in der Warehouse Management Mobile App aus, wenn Sie die Entnahmearbeit durchführen.</li>
<li>Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</li>
<li>Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit manueller Neuzuteilung</strong> aus.</li>
<li>Wählen Sie den Lagerort/Ladungsträger in der Liste aus.</li>
</ol>
</td>
<td>
<ul>
<li>Bei der aktuellen Arbeit werden folgende Aktionen ausgeführt:
<ul>
<li>Die Entnahmeposition wird geschlossen und die Entnahmemenge ist 0 (Null).</li>
<li>Die Einlagerungsposition wird storniert.</li>
</ul>
</li>
<li>Eine Lagerbuchung vom Typ <strong>Inventur</strong> und der Abgangstyp <strong>Verkauft</strong> werden erstellt, um die Anpassung darzustellen.</li>
</ul>
</td>
<td>Alle vorhandenen Reservierungen, die von der Mengenanpassung im Lagerort der Kurzentnahme/am Ladungsträger der Kurzentnahme betroffen sind, werden entfernt.</td>
</tr>
<tr>
<td>Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Automatisch</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja/Nein</strong> und <strong>Reservierungen entfernen</strong> = <strong>Ja/Nein</strong> ist.</td>
<td>Nicht zutreffend</td>
<td>
<ol>
<li>Wählen Sie das Menüelement <strong>Entnahme mit unzureichender Menge</strong> in der Warehouse Management Mobile App aus, wenn Sie die Entnahmearbeit durchführen.</li>
<li>Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</li>
<li>Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit automatischer Neuzuteilung</strong> aus.</li>
</ol>
</td>
<td>Eine Kurzentnahme mit automatischer Neuzuteilung wird nicht unterstützt.</td>
<td>Eine Kurzentnahme mit automatischer Neuzuteilung wird nicht unterstützt.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Bestandsstatus ändern

> [!NOTE]
> Diese Lagerortaktion kann von mehreren Einstiegspunkten aus durchgeführt werden. Das hier gezeigte Beispiel verwendet die Aktion **Bestandsstatusänderung** auf der Seite **Verfügbarer Lagerbestand nach Lagerplatz**.

<table>
<thead>
<tr>
<th>Wichtige Einrichtungsparameter</th>
<th>Chargenmenge ist verfügbar</th>
<th>Wichtige Schritte für den Benutzer</th>
<th>Lagerarbeit</th>
<th>Auftragsgebundene Chargenreservierung</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Auf der Registerkarte <strong>Lagerort</strong> im Datensatz <strong>Lagerort</strong> ist das Feld <strong>Reservierungen und Markierungen entfernen</strong> auf <strong>Reservierungen</strong> oder <strong>Markierungen und Reservierungen</strong> gesetzt.</td>
<td>Ja</td>
<td>
<ol>
<li>Wählen Sie einen bestimmten Lagerort aus.</li>
<li>Wählen Sie eine Position mit einem bestimmten Artikel, Lagerort und Ladungsträger (sofern der Lagerort durch einen Ladungsträger gesteuert wird).</li>
<li>Wählen Sie <strong>Bestandsstatusänderung</strong> aus.</li>
<li>Setzen Sie das Feld <strong>Bestandsstatus</strong> auf <strong>Sperrung</strong>.</li>
</ol>
</td>
<td>Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</td>
<td>
<ul>
<li>Die Menge wird für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</li>
<li>Zwei Lagerbuchungen vom Typ <strong>Bestandsstatusänderung</strong> werden erstellt, um die Änderung in der Bestandsstatusdimension darzustellen.</li>
<li>Eine Lagerbuchung vom Typ <strong>Sperrung von Lagerbestand</strong> sowie der Abgangstyp <strong>Physisch reserviert</strong> werden erstellt, um die Reservierung der gesperrten Menge darzustellen.</li>
</ul>
</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</td>
<td>
<ul>
<li>Die Reservierung wird entfernt.</li>
<li>Zwei Lagerbuchungen vom Typ <strong>Bestandsstatusänderung</strong> werden erstellt, um die Änderung in der Bestandsstatusdimension darzustellen.</li>
<li>Eine Lagerbuchung vom Typ <strong>Sperrung von Lagerbestand</strong> sowie der Abgangstyp <strong>Physisch reserviert</strong> werden erstellt, um die Reservierung der gesperrten Menge darzustellen.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Auf der Registerkarte <strong>Lagerort</strong> im Datensatz <strong>Lagerort</strong> ist das Feld <strong>Reservierungen und Markierungen entfernen</strong> auf <strong>Nein</strong> gesetzt.</td>
<td>Ja</td>
<td>
<ol>
<li>Wählen Sie einen bestimmten Lagerort aus.</li>
<li>Wählen Sie eine Position mit einem bestimmten Artikel, Lagerort und Ladungsträger (sofern der Lagerort durch einen Ladungsträger gesteuert wird).</li>
<li>Wählen Sie <strong>Bestandsstatusänderung</strong> aus.</li>
<li>Setzen Sie das Feld <strong>Bestandsstatus</strong> auf <strong>Sperrung</strong>.</li>
</ol>
</td>
<td>Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</td>
<td>Die Menge wird für dieselbe Charge erneut reserviert. Das System weist nach dem Zufallsprinzip einen Lagerort und einen Ladungsträger zu (sofern der Lagerort durch einen Ladungsträger gesteuert wird), an bzw. bei dem die Menge verfügbar ist.</td>
</tr>
<tr>
<td>Nein</td>
<td>Siehe vorherige Zeile.</td>
<td>Bestandsstatusänderungen sind für Mengen, die für Arbeit reserviert sind, nicht zulässig.</td>
<td>Bestandsstatusänderungen sind nicht zulässig.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Einschränkungen

- Die flexible Reservierungsfunktion für Dimensionen auf Lagerortebene unterstützt die folgenden Funktionen nicht:

    - Artikelgewichtsverwaltung
    - Physischer negativer Bestand
    - Reservierung kontra gegen bestellte Lieferung
    - Transportaufträge und Rohmaterialentnahme

- Die Containerkonsolidierungsregel für das Verpacken nach Richtlinieneinheit hat Einschränkungen. Für auftragsgebundene Reservierungen empfehlen wir, keine Container-Build-Vorlagen zu verwenden, bei denen das Feld **Nach Richtlinieneinheit verpacken** aktiviert ist. Beim aktuellen Design werden keine Lagerplatzrichtlinien verwendet, wenn Lagerarbeit erstellt wird. Daher wird nur die niedrigste Einheit in der Nummernkreisgruppe (der Lagereinheit) während des Containerisierungswellenschritts angewendet.

## <a name="see-also"></a>Siehe auch

- [Chargennummern in der Lagerortverwaltung](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [Reservieren derselben Charge für einen Auftrag](../sales-marketing/reserve-same-batch-sales-order.md)
- [Entnahme der ältesten Charge mit einem mobilen Gerät](pick-oldest-batch.md)
- [Chargen- und Kennzeichenbestätigung](batch-and-license-plate-confirmation.md)
- [Problembehandlung bei Reservierungen in der Lagerortverwaltung](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]