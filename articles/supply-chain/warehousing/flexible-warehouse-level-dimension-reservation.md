---
title: Flexible Reservierungsrichtlinie für Dimensionen auf Lagerortebene
description: In diesem Thema wird die Bestandsreservierungsrichtlinie beschrieben, mit der Unternehmen, die Produkte mit Chargenverfolgung verkaufen und für die Logistik WMS-fähige Vorgänge ausführen, bestimmte Chargen für Debitorenaufträge reservieren können, obwohl die mit den Produkten verknüpfte Reservierungshierarchie die Reservierung bestimmter Chargen nicht zulässt.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0fe9ed9f2bebe8683f3b8bb37b33e8a63b9521f6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205666"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Flexible Reservierungsrichtlinie für Dimensionen auf Lagerortebene

[!include [banner](../includes/banner.md)]

Wenn eine Bestandsreservierungshierarchie vom Typ „Charge unterhalb\[Lagerort\]“mit Produkten verknüpft ist, können Unternehmen, die Produkte mit Chargenverfolgung verkaufen und ihre Logistik als Operationen ausführen, die für das Microsoft Dynamics 365 Warehouse Management System (WMS) aktiviert sind, bestimmte Chargen dieser Produkte nicht für Debitorenaufträge reservieren. In diesem Thema wird die Bestandsreservierungsrichtlinie beschrieben, mit der diese Unternehmen bestimmte Chargen reservieren können, auch wenn die Produkte mit einer „Charge unterhalb\[Lagerort\]“-Reservierungshierarchie verknüpft sind.

## <a name="inventory-reservation-hierarchy"></a>Bestandreservierungshierarchie

In diesem Abschnitt wird die vorhandene Bestandsreservierungshierarchie zusammengefasst. Der Schwerpunkt liegt auf der Art und Weise, wie Artikel mit Chargenverfolgung und Seriennummernverfolgung gehandhabt werden.

Die Bestandsreservierungshierarchie gibt vor, dass hinsichtlich von Lagerdimensionen, der Bedarfsauftrag die obligatorischen Dimensionen von Standort-, Lager- und Bestandsstatus trägt, während die Lagerlogik für die Zuweisung eines Lagerplatzes für die angeforderten Mengen und das Reservieren des Lagerplatzes zuständig ist. Mit anderen Worten, bei den Interaktionen zwischen dem Bedarfsauftrag und den Lagervorgängen wird erwartet, dass der Bedarfsauftrag angibt, von wo der Auftrag versendet werden muss (d. h., von welchem Standort und von welchem Lagerort). Das Lager verlässt sich dann auf seine Logik, um die erforderliche Menge in den Lagerstätten zu finden.

Um jedoch das Betriebsmodell des Unternehmens widerzuspiegeln, unterliegen die Rückverfolgungsangaben (Chargen- und Seriennummern) einer größeren Flexibilität. Eine Bestandsreservierungshierarchie kann Szenarien berücksichtigen, bei denen die folgenden Bedingungen zutreffen:

- Das Unternehmen verlässt sich auf seine Lagerort-Arbeitsgänge für die Verwaltung der Kommissionierung von Mengen mit Chargen- oder Seriennummern, nachdem die Mengen in einem Lager gefunden wurden. Dieses Modell wird häufig als *Charge unterhalb\[Lagerort\]* bezeichnet. Es wird normalerweise verwendet, wenn die Chargen- oder Seriennummer eines Produkts für die Debitoren nicht wichtig ist, die eine Nachfrage beim verkaufenden Unternehmen stellen.
- Wenn Chargen- oder Seriennummern Teil der Auftragsspezifikation eines Debitors sind und im Bedarfsauftrag aufgeführt werden, werden die Lagerortarbeitsgänge, die für die Suche nach den Mengen im Lager eingesetzt werden, durch die angegebenen Nummern eingeschränkt und können diese nicht ändern. Dieses Modell wird häufig als *Charge oberhalb\[Lagerort\]* bezeichnet.

In diesen Szenarien besteht die Herausforderung darin, dass jedem freigegebenen Produkt nur eine Bestandsreservierungshierarchie zugeordnet werden kann. Damit das WMS nachverfolgte Artikel verarbeiten kann, können, nachdem die Hierarchiezuweisung bestimmt, wann die Chargen- oder Seriennummer reserviert werden sollte (entweder wenn der Bedarfsauftrag entgegengenommen wird oder während der Lagerentnahme), diese Zeiten nicht ad-hoc geändert werden.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Flexible Reservierung für chargenverfolgte Artikel

### <a name="business-scenario"></a>Geschäftsszenario

In diesem Szenario verwendet ein Unternehmen eine Bestandsstrategie, bei der Fertigwaren anhand von Chargennummern verfolgt werden. Diese Firma verwendet auch die WMS-Arbeitsauslastung. Da diese Auslastung eine gut gerüstete Logik für die Planung und Durchführung von Kommissionierungs- und Versandvorgängen für Artikel hat, für die Chargen aktiviert sind, werden die meisten Fertigprodukte mit der Bestandsreservierungshistorie „Charge unterhalb\[Lagerort\]“ verknüpft. Der Vorteil dieser Art des operativen Einrichtung besteht darin, dass Entscheidungen (die im Grunde genommen Reservierungsentscheidungen sind) darüber, welche Chargen kommissioniert werden sollen und wo sie im Lager abgelegt werden sollen, verschoben werden, bis mit der Kommissionierung begonnen wird. Sie werden nicht schon gemacht, wenn der Kunde bestellt.

Obwohl die Reservierungshistorie „Charge unterhalb\[Lagerort\]“ den Geschäftszielen des Unternehmens dient, fordern viele der etablierten Unternehmenskunden bei der Nachbestellung die gleiche Charge an, wie beim vorherigen Kauf. Aus diesem Grund ist das Unternehmen bestrebt, die Regeln für die Chargenreservierung flexibel zu gestalten, sodass, je nachdem, ob der Kunde den gleichen Artikel wünscht, die folgenden Verhaltensweisen auftreten:

- Eine Chargennummer kann aufgezeichnet und reserviert werden, wenn der Auftrag vom Verkäufer entgegengenommen wird. Sie kann während des Lagerortbetriebs nicht geändert werden und/oder aufgrund anderer Bedarfe verwendet werden. Dieses Verhalten hilft zu gewährleisten, dass die bestellte Chargennummer an den Kunden gesendet wird.
- Wenn die Chargennummer für den Kunden nicht wichtig ist, kann der Lagerbetrieb während der Kommissionierungsarbeiten eine Chargennummer bestimmen, nachdem die Kundenauftragsregistrierung und -reservierung durchgeführt wurden.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Reservierung einer bestimmten Charge im Auftrag zulassen

Um der gewünschten Flexibilität bei der Chargenreservierung für Artikel, die mit einer „Charge unterhalb\[Lagerort\]“-Bestandsreservierungshistorie verknüpft sind, gerecht zu werden, müssen Bestandsverwalter das Kontrollkästchen für **Reservierung für Bedarfsauftrag zulassen** für die **Chargennummer**-Ebene auf der Seite **Bestandsreservierungshierarchien** aktivieren.

![Bestandreservierungshierarchie flexibler machen](media/Flexible-inventory-reservation-hierarchy.png)

Wenn die **Chargennummer**-Ebene in der Hierarchie ausgewählt wird, werden alle Dimensionen über dieser Ebene und bis zur **Lagerort**-Ebene wird automatisch ausgewählt. (Standardmäßig sind alle Dimensionen über der **Lagerort**-Ebene ausgewählt.) Dieses Verhalten spiegelt eine Logik wider, bei der alle Dimensionen im Bereich zwischen Chargennummer und Lagerort automatisch reserviert werden, nachdem Sie eine bestimmte Chargennummer aus der Auftragsposition reserviert haben.

> [!NOTE]
> Das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** gilt nur für die Reservierungshierarchieebenen, die unterhalb der Lagerortdimension liegen.
>
> **Chargennummer** ist die einzige Ebene in der Hierarchie, die für die flexible Reservierungsrichtlinie offen ist. Mit anderen Worten, Sie können das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** nicht für die Ebenen **Lagerort**, **Ladungsträger** oder **Seriennummer** aktivieren.
>
> Wenn Ihre Reservierungshierarchie die Seriennummerdimension enthält (die immer unterhalb der **Chargennummer**-Ebene liegen muss), und wenn Sie die chargenspezifische Reservierung für die Chargennummer aktiviert haben, wird das System weiterhin die Seriennummernreservierung und die Kommissionierungsvorgänge basierend auf den Regeln durchführen, die für die Reservierungsrichtlinie „Serie unterhalb\[Lagerort\]“ gelten.

Sie können jederzeit eine chargenspezifische Reservierung für eine vorhandene „Charge unterhalb\[Lagerort\]“-Reservierungsrichtlinie in Ihrer Bereitstellung zulassen. Diese Änderung wirkt sich nicht auf Reservierungen und offene Lagerarbeiten aus, die vor der Änderung erstellt wurden. Das Kontrollkästchen ***Reservierung für Bedarfsauftrag zulassen** kann aber nicht deaktiviert werden, wenn Lagerbuchungen vom Abgangstyp **Bestellt reserviert**, **Physisch reserviert** oder **Bestellt** für mindestens einen Artikel vorhanden sind, der mit der Reservierungshistorie verknüpft ist.

> [!NOTE]
> Wenn die vorhandene Reservierungshierarchie eines Artikels keine Chargenspezifikation für den Auftrag zulässt, können Sie ihn einer Reservierungshierarchie zuordnen, die eine Chargenspezifikation zulässt, vorausgesetzt, die Struktur der Hierarchieebene ist in beiden Hierarchien gleich. Verwenden Sie die **Reservierungshierarchie für Artikel ändern**-Funktion, um die Neuzuweisung durchzuführen. Diese Änderung ist möglicherweise relevant, wenn Sie die flexible Chargenreservierung für eine Teilmenge von Artikeln mit Chargenverfolgung verhindern möchten, aber für den Rest des Produktportfolios zulassen möchten.

Unabhängig davon, ob Sie das Kontrollkästchen **Reservierung für Bedarfsauftrag zulassen** aktiviert haben, wird dennoch die standardmäßige Lagerort-Operationslogik angewendet, die für eine „Charge unterhalb\[Lagerort\]“-Reservierungshierarchie gilt, wenn Sie keine bestimmte Chargennummer für den Artikel in einer Auftragsposition reservieren möchten.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Reservieren einer bestimmten Chargennummer für eine Kundenbestellung

Nachdem die „Charge unterhalb\[Lagerort\]“-Bestandsreservierungshierarchie eines Artikels mit Chargenverfolgung so eingerichtet ist, dass bestimmte Chargennummern für Aufträge reserviert werden können, können Verarbeiter von Aufträgen, je nach Kundenwunsch, die Kundenaufträge für den gleichen Artikel auf eine der folgenden Arten aufnehmen:

- **Auftragsdetails ohne Angabe einer Chargennummer eingeben** – Dieser Ansatz sollte verwendet werden, wenn die Chargenspezifikation des Produkts für den Kunden nicht wichtig ist. Alle bestehenden Prozesse, die mit der Abwicklung eines Auftrags dieser Art verbunden sind, bleiben im System unverändert. Es sind keine zusätzlichen Überlegungen seitens der Benutzer erforderlich.
- **Bestelldetails eingeben und eine bestimmte Chargennummer reservieren** – Dieser Ansatz sollte verwendet werden, wenn der Kunde eine bestimmte Charge anfordert. In der Regel fordern Kunden eine bestimmte Charge an, wenn sie ein zuvor erworbenes Produkt erneut bestellen. Diese Art der chargenspezifischen Reservierung wird als *auftragsgebundene Reservierung* bezeichnet.

Die folgenden Regeln gelten, wenn Mengen verarbeitet werden und eine Chargennummer für eine bestimmte Bestellung vorgegeben ist:

- Um die Reservierung einer bestimmten Chargennummer für einen Artikel zuzulassen, für den die Reservierungsrichtlinie „Charge unterhalb\[Lagerort\]“ gilt, muss das System alle Dimensionen bis zum Lagerort reservieren. Dieser Bereich umfasst normalerweise die Ladungsträgerdimension.
- Lagerplatzrichtlinien werden nicht verwendet, wenn Kommissionierungsarbeiten für eine Verkaufsposition angelegt werden, die die auftragsgebundene Chargenreservierung verwendet.
- Während der Verarbeitung von Lagerarbeit für auftragsgebundene Chargen dürfen weder der Benutzer noch das System die Chargennummer ändern. (Diese Verarbeitung umfasst auch die Ausnahmebehandlung.)

Das folgende Beispiel zeigt den vollständigen Ablauf.

## <a name="example-scenario"></a>Beispielszenario

Für dieses Beispielmüssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a>Einrichten einer Bestandsreservierungshierarchie, um eine chargenspezifische Reservierung zu ermöglichen

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

### <a name="enter-sales-order-details"></a>Auftragsdetails eingeben

1. Wechseln Sie zu **Vertrieb und Marketing** \> **Aufträge** \> **Alle Aufträge**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Auftragskopf im Feld **Debitorenkonto** **US-003** ein.
4. Fügen Sie eine Position für den neuen Artikel hinzu und geben Sie als Menge **10** ein. Stellen Sie sicher, dass das Feld **Lagerort** auf **24** gesetzt ist.
5. Wählen Sie im Inforegister **Auftragspositionen** **Bestand**und dann in der Gruppe **Verwalten** **Chargenreservierung** aus. Die Seite **Chargenreservierung** zeigt eine Liste der Chargen, die für die Reservierung für die Bestellposition verfügbar sind. In diesem Beispiel wird eine Menge von **20** für die Chargennummer **B11** und eine Menge von **10** für die Chargennummer **B22** angezeigt. Beachten Sie, dass auf die Seite **Chargenreservierung** nicht von einer Position aus zugegriffen werden kann, wenn der Artikel in dieser Position mit einer „Charge unterhalb\[Lagerort\]“-Reservierungshierarchie verknüpft ist, es sei denn, diese ist so eingerichtet, dass chargenspezifische Reservierungen möglich sind.

    > [!NOTE]
    > Um eine bestimmte Charge für einen Auftrag zu reservieren, müssen Sie die Seite **Chargenreservierung** verwenden.
    >
    > Wenn Sie die Chargennummer direkt in die Auftragsposition eingeben, verhält sich das System so, als hätten Sie einen bestimmten Chargenwert für einen Artikel eingegeben, für den die „Charge unterhalb\[Lagerort\]“-Reservierungsrichtlinie gilt. Wenn Sie die Position speichern, erhalten Sie eine Warnmeldung. Wenn Sie bestätigen, dass die Chargennummer direkt in der Bestellposition angegeben werden soll, wird die Position nicht von der normalen Lagerortverwaltungslogik verarbeitet.
    >
    > Wenn Sie die Menge über die Seite **Reservierung** reservieren, wird keine bestimmte Charge reserviert und die Ausführung der Lagerortoperationen für die Position folgt den Regeln, die im Rahmen der Reservierungsrichtlinie „Charge unterhalb\[Lagerort\]“ gelten.

    Im Allgemeinen funktioniert und interagiert diese Seite genauso wie sie bei Artikeln funktioniert und interagiert, die mit einer Reservierungshierarchie vom Typ „Charge oberhalb\[Lagerort\]“ verknüpft sind. Es gelten jedoch folgende Ausnahmen:

    - Das Inforegister **Chargennummern für Quellposition zugesagt** zeigt die Chargennummern an, die für die Bestellposition reserviert sind. Die Chargenwerte im Raster werden während des gesamten Erfüllungszyklus der Auftragsposition einschließlich der Phasen der Lagerortverarbeitung angezeigt. Im Gegensatz dazu werden auf dem Inforegister **Übersicht** regelmäßige Auftragspositionsreservierungen (also Reservierungen für die Dimensionen oberhalb der **Lagerort**-Ebene) im Raster bis zu dem Punkt angezeigt, wenn Lagerarbeiten generiert werden. Die Arbeitsentität übernimmt dann die Positionsreservierung und die Positionsreservierung erscheint nicht mehr auf der Seite. Das Inforegister **Chargennummern für Quellposition zugesagt** sorgt mit dafür, dass der Auftragsverarbeiter die Chargennummern, die für den Kundenauftrag zugesagt wurden, während des gesamten Lebenszyklus bis hin zur Rechnungsstellung anzeigen kann.
    - Zusätzlich zur Reservierung einer bestimmten Charge kann ein Benutzer den spezifischen Lagerort und Ladungsträger manuell auswählen und auf die automatische Auswahl durch das System verzichten. Diese Funktion hängt mit dem Design des auftragsgebunden Chargenreservierungsmechanismus zusammen. Wie bereits erwähnt: Wenn eine Chargenummer für einen Artikel reserviert ist, für den die Reservierungsrichtlinie „Charge unterhalb\[Lagerort\]“ gilt, muss das System alle Dimensionen bis zum Lagerort reservieren. Aus diesem Grund gelten für die Lagerarbeit die gleichen Lagerdimensionen, die von den Benutzern reserviert wurden, die diese Aufträge bearbeitet haben. Sie zeigt möglicherweise nicht immer die Artikellagerplatzierung, die für Kommissionierungsarbeiten zweckmäßig oder möglich ist. Wenn Auftragsbearbeiter die Einschränkungen des Lagerorts kennen, möchten sie möglicherweise die spezifischen Lagerorte und Ladungsträger manuell auswählen, wenn sie eine Charge reservieren. In diesem Fall muss der Benutzer die **Dimensionen anzeigen**-Funktionalität auf dem Seitenkopf nutzen und den Lagerort und den Ladungsträger zum Raster im Inforegister **Übersicht** hinzufügen.

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
    - Die Chargennummer wird nicht an der Entnahmeposition angezeigt (im Gegensatz zur Arbeitsposition, die für einen Artikel mit verknüpfter „Charge oberhalb\[Lagerort\]“-Reservierungshierarchie erstellt wird.) Stattdessen werden die von-Chargennummer und alle anderen Lagerdimensionen in der Lagerbuchung der Arbeitsposition angezeigt, auf die von den verknüpften Lagerbuchungen verwiesen wird.

        ![Lagerort-Lagerbuchungen für Arbeit, die aus einer auftragsgebundenen Reservierung stammt](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Nachdem die Arbeit erstellt wurde, wird die Lagerbuchung, bei der das Feld **Referenz** auf **Auftragsgebundene Reservierung** gesetzt ist, entfernt. Die Lagerbuchung, bei das Feld **Referenz** auf **Arbeit** gesetzt ist, enthält nun die physische Reservierung für alle Lagerdimensionen der Menge.

        Arbeitsgänge am Arbeitsort können auf die übliche Art und Weise abgewickelt werden. Die Anweisungen auf dem Mobilgerät weisen die Arbeitskraft jedoch an, eine bestimmte Chargennummer auszuwählen. In Lagerortumgebungen, bei denen Lagerorte durch Ladungsträger gesteuert werden, kann eine Arbeitskraft, nachdem sie den Lagerort erreicht hat, der die gleiche Charge auf mehreren Ladungsträgern lagert, von einem beliebigen Ladungsträger entnehmen, der nicht bereits reserviert ist (beispielsweise von einer anderen auftragsgebundenen Reservierung oder einer Arbeit, die von einer Reservierung diesen Typs stammt).

        Wenn es sich als unpraktisch herausstellt, von dem Lagerort zu entnehmen, der in der Arbeitsposition angegeben ist, kann der Lagerortoperator eine der folgenden Aktionen verwenden, um die Kommissionierung der bestimmten Charge zu einem passenderen Lagerort umleiten.

        - Der Standardaktion **Lagerplatzüberschreibung** auf einem mobilen Gerät (vorausgesetzt, die Lagerort-Arbeitskräfte-Einstellung **Außerkraftsetzen des Entnahmeorts zulassen** ist aktiviert)
        - Die Aktion **Lagerplatz ändern** auf der Seite **Arbeitslistendetails**. 

2. Beenden Sie auf dem mobilen Gerät die Kommissionierung und Platzierung der Arbeit.

    Die Menge von **10** für Chargennummer **B11** wird nun für die Auftragsposition und im Lagerort **Baydoor** platziert. Zu diesem Zeitpunkt kann es auf den LKW verladen und an die Adresse des Kunden versendet werden.

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a>Ausnahmebehandlung von Lagerarbeit mit auftragsgebundenen Chargennummern

Die Lagerarbeit für die Kommissionierung von auftragsgebundenen Chargennummern unterliegt denselben standardmäßigen Lagerortausnahmebehandlungen und -Aktionen wie die reguläre Arbeit. Im Allgemeinen kann die offene Arbeit oder Arbeitsposition storniert werden. Sie kann unterbrochen werden, weil ein Lagerort voll ist, sie kann kurz entnommen werden und sie kann aufgrund einer Bewegung aktualisiert werden. Ebenso kann die kommissionierte Arbeit, die bereits erledigt wurde, reduziert oder rückgängig gemacht werden.

Für alle diese Ausnahmebehandlungsaktionen gilt die folgende Grundregel: Die für den Kunden reservierte Chargennummer kann niemals durch eine andere Chargennummer ersetzt werden, ihre Lagerdimensionen (Lagerort und Ladungsträger) können jedoch durch eine manuelle Aktualisierung seitens des Benutzers geändert werden oder durch eine automatische Aktualisierung seitens des Systems. Die automatische Aktualisierung basiert auf der gleichen zufälligen Zuweisung von Lagerdimensionen, die galten, als eine bestimmte Charge automatisch reserviert wurde, aber keine Lagerdimensionen angegeben waren.

### <a name="example-scenario"></a>Beispielszenario

Ein Beispiel für dieses Szenario ist eine Situation, in der zuvor abgeschlossene Arbeiten teilweise rückgängig gemacht wird, indem die Funktion **Entnommene Menge reduzieren** verwendet wird. Bei diesem Beispiel wird das vorherige Bespiel dieses Themas fortgesetzt.

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
<li>Wählen Sie den Menüeintrag <strong>Standort überschreiben</strong> in der Warehouse Mmobile App (WMA) aus, wenn Sie mit der Entnahmearbeit beginnen.</li>
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
<td>Nein</td>
<td>
<ol>
<li>Wählen Sie den Menüeintrag <strong>Standort überschreiben</strong> in WMA aus, wenn Sie mit der Entnahmearbeit beginnen.</li>
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
<li>Wählen Sie den Menüeintrag <strong>Voll</strong> in WMA aus, wenn Sie Entnahmearbeit verarbeiten.</li>
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
<li>Starten Sie eine Verlagerung in WMA.</li>
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
<li>Wählen Sie den Menüeintrag <strong>ShortPick</strong> in WMA aus, wenn Sie Entnahmearbeit ausführen.</li>
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
<li>Wählen Sie den Menüeintrag <strong>ShortPick</strong> in WMA aus, wenn Sie Entnahmearbeit ausführen.</li>
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
<li>Wählen Sie den Menüeintrag <strong>ShortPick</strong> in WMA aus, wenn Sie Entnahmearbeit ausführen.</li>
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
<td>Nein</td>
<td>
<ol>
<li>Wählen Sie den Menüeintrag <strong>ShortPick</strong> in WMA aus, wenn Sie Entnahmearbeit ausführen.</li>
<li>Geben Sie im Feld für <strong>Menge der Kurzentnahme</strong> den Wert <strong>0</strong> (Null) ein.</li>
<li>Wählen Sie im Feld <strong>Grund</strong> <strong>Kurze Entnahme mit manueller Neuzuteilung</strong> aus.</li>
</ol>
</td>
<td>Die Kurzentnahme-Aktion schlägt fehl und es wird ein Fehler ausgegeben.</td>
<td>Nicht zutreffend</td>
</tr>
<tr>
<td>Eine Arbeitsausnahme vom Typ <strong>Kurzentnahme</strong> wird eingerichtet, wenn <strong>Artikelneuzuteilung</strong> = <strong>Manuell</strong>, <strong>Bestandsregulierung</strong> = <strong>Ja</strong> und <strong>Reservierungen entfernen</strong> = <strong>Ja</strong> ist. Zusätzlich wird die Option <strong>Manuelle Artikelneuzuordnung zulassen</strong> für die Arbeitskraft aktiviert.</td>
<td>Nein</td>
<td>
<ol>
<li>Wählen Sie den Menüeintrag <strong>ShortPick</strong> in WMA aus, wenn Sie Entnahmearbeit ausführen.</li>
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
<li>Wählen Sie den Menüeintrag <strong>ShortPick</strong> in WMA aus, wenn Sie Entnahmearbeit ausführen.</li>
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
