---
title: Inventory Visibility-Bestandszuteilung
description: In diesem Artikel wird erläutert, wie Sie die Bestandzuweisungsfunktion einrichten und verwenden, mit der Sie dedizierten Bestand reservieren können, um sicherzustellen, dass Sie Ihre profitabelsten Kanäle oder Kunden bedienen können.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762671"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility-Bestandszuteilung

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Unternehmenshintergrund und -zweck

Organisationen müssen ihren Lagerbestand häufig ihren wichtigsten Vertriebskanälen, Kundengruppen, Regionen und Werbeveranstaltungen vorab zuordnen, um sicherzustellen, dass der vorab zugeteilte Bestand vor jeder anderen Verwendung geschützt ist und nur über für die relevante Verkaufstransaktionen verbraucht werden kann Zuweisung. Die Bestandszuteilung in Bestandsanzeige ist eine Komponente des operativen Planungsprozesses des Vertriebs und wird durchgeführt, bevor die eigentlichen Vertriebsaktivitäten stattfinden oder ein Auftrag erstellt wird.

Beispielsweise stellt ein Unternehmen namens Contoso ein beliebtes Fahrrad her. Da eine kürzliche Unterbrechung der Lieferkette den gesamten Transportbestand dieses Fahrrads beeinträchtigt hat, verfügt Contoso leider nur über begrenzte Lagerbestände und muss diese optimal nutzen. Contoso führt sowohl Online- als auch In-Store-Verkäufe durch. In jedem Vertriebskanal hat das Unternehmen einige wichtige Unternehmenspartner (Marktplätze und große Einzelhändler), die verlangen, dass ein bestimmter Teil des verfügbaren Fahrradbestands für sie reserviert wird. Daher muss das Fahrradunternehmen in der Lage sein, die Lagerverteilung über die Kanäle hinweg auszugleichen und auch die Erwartungen seiner VIP-Partner zu erfüllen. Der beste Weg, beide Ziele zu erreichen, ist die Bestandszuordnung, sodass jeder Kanal und Einzelhändler bestimmte zugeteilte Mengen erhalten kann, die später an Kunden verkauft werden können.

Die Bestandszuteilung hat zwei grundlegende Geschäftszwecke:

- **Inventarschutz (Ringfencing)** – Organisationen möchten eingeschränkte oder begrenzte Bestände priorisierten Kanälen, Regionen, VIP-Kunden und Tochterunternehmen vorab zuordnen. Die Zuteilungsfunktion „Bestandssichtbarkeit“ zielt darauf ab, den zugteilten Bestand zu schützen, sodass andere Zuteilungen, Reservierungen oder andere Verkaufsanforderungen den zuvor zugeteilten Bestand nicht beeinflussen.
- **Überverkaufskontrolle** – Die Bestandsichtbarkeits-Zuteilungsfunktion zielt darauf ab, die zuvor zugeteilten Mengen einzuschränken, damit die empfangende Partei (z. B. ein Kanal oder eine Kundengruppe) sie nicht übermäßig verbraucht, wenn die tatsächliche Verkaufstransaktion auf einer Soft Reservierung in Kraft tritt.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Zuteilungsdefinition im Dienst zur Bestandsanzeige

### <a name="allocation-virtual-pool"></a>Zuweisung virtueller Pool

Obwohl die Zuteilungsfunktion in der Bestandsanzeige keine physischen Bestandsmengen reserviert, bezieht sie sich auf die verfügbare physische Bestandsmenge, um ihre anfängliche *für die Zuteilung verfügbare* Menge des virtuellen Pools zu definieren. Die Inventarzuteilung in der Bestandsanzeige ist eine weiche Zuteilung. Dies geschieht, bevor die eigentlichen Verkaufstransaktionen stattfinden, und hängt nicht von Aufträgen ab. Beispielsweise können Sie Ihren wichtigsten Vertriebskanälen oder großen Einzelhändlern Lagerbestände zuteilen, bevor Endkunden den Vertriebskanal oder das Einzelhandelsgeschäft besuchen, um sie zu kaufen.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Unterschied zwischen Bestandszuordnung und weicher Reservierung

[Weiche Reservierungen](inventory-visibility-reservations.md) sind in der Regel mit tatsächlichen Verkaufstransaktionen (Auftragspositionen) verknüpft. Sowohl die Zuweisung als auch die weiche Reservierung können unabhängig voneinander verwendet werden, aber wenn Sie sie zusammen verwenden möchten, sollte die weiche Reservierung nach der Zuweisung erfolgen. Wir empfehlen, dass Sie zuerst eine Bestandszuteilung durchführen und dann eine vorläufige Reservierung für die zugeteilten Mengen vornehmen, um einen Verbrauch gegen die Zuteilung nahezu in Echtzeit zu erreichen. Weitere Informationen finden Sie unter [Eine Soft-Reservierung nutzen](#consume-to-soft-reserved).

Mit der Bestandszuteilungsfunktion können Verkaufsplaner oder Betreuer von Hauptkunden wichtige Bestände über Zuteilungsgruppen (z. B. Kanäle, Regionen und Kundengruppen) hinweg verwalten und vorab zuordnen. Es unterstützt auch die Verfolgung, Anpassung und Analyse der Nutzung in Echtzeit anhand zugewiesener Mengen, um sicherzustellen, dass eine rechtzeitige Auffüllung oder Neuzuweisung erfolgen kann. Diese Fähigkeit, in Echtzeit Einblick in die Zuteilung, die Nutzung und die Zuteilungsbilanz zu haben, ist besonders bei Schnellverkaufs- oder Werbeveranstaltungen wichtig.

## <a name="terminology"></a>Terminologie

Die folgenden Begriffe und Konzepte sind bei Diskussionen über die Bestandszuteilung hilfreich:

- **Zuteilungsgruppe** – die Gruppe, der die Zuteilung gehört, z. B. ein Vertriebskanal, eine Kundengruppe oder eine Auftragsart.
- **Zuteilungsgruppenwert** – Der Wert jeder Zuteilungsgruppe. Zum Beispiel könnte *Netz* oder *Laden* der Wert der Vertriebskanalzuteilungsgruppe sein, wohingegen *VIP* oder *Normal* der Wert der Kundenzuteilungsgruppe sein kann.
- **Zuteilungshierarchie** – Ein Mittel, um Zuteilungsgruppen hierarchisch zusammenzufassen. Sie können beispielsweise *Kanal* als Hierarchiestufe 1, *Region* als Stufe 2 und *Kundengruppe* als Stufe 3 definieren. Während der Bestandszuteilung müssen Sie die Reihenfolge der Zuteilungshierarchie befolgen, wenn Sie den Wert der Zuteilungsgruppe angeben. Sie können beispielsweise 200 rote Fahrräder dem *Netz*-Kanal, der *London*-Region und der *VIP*-Kundengruppe zuteilen.
- **Für Zuteilung verfügbar** – der *virtuellen gemeinsamen Pool*, der die Menge angibt, die für eine weitere Zuteilung verfügbar ist. Es handelt sich um ein berechnetes Maß, das Sie mithilfe Ihrer eigenen Formel frei definieren können. Wenn Sie auch die Soft-Reservierungsfunktion verwenden, empfehlen wir Ihnen, dieselbe Formel zu verwenden, um „für Zuweisung verfügbar“ und „für Reservierung verfügbar“ zu berechnen.
- **Zugeteilt** – ein physisches Maß, das das zugeteilte Kontingent zeigt, das von den Zuteilungsgruppen genutzt werden kann. Es wird gleichzeitig abgezogen, dass die verbrauchte Menge hinzugefügt wird.
- **Genutzt** – ein physisches Maß, das anzeigt, dass die Mengen, die genutzt wurden, mit der ursprünglich zugeteilten Menge verglichen werden. Wenn Zahlen zu dieser Maßeinheit hinzugefügt werden, wird die zugeteilte physische Maßeinheit automatisch reduziert.

Die folgende Abbildung zeigt den Geschäfts-Workflow für die Bestandszuteilung.

![Bestandsanzeige des Geschäfts-Workflows für die Zuzteilung.](media/inventory-visibility-allocation-flow.png "Bestandsanzeige des Geschäfts-Workflows für die Zuzteilung.")

Die folgende Abbildung zeigt die Zuordnungshierarchie und Zuordnungsgruppen. Der hier angezeigte *virtuelle gemeinsame Pool* ist die zur Zuordnung verfügbare Menge.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="Bestandsanzeige-Bestandszuteilung Hierarchie" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

## <a name="set-up-inventory-allocation"></a>Bestandszuteilung einrichten

Die Bestandszuteilungsfunktion besteht aus den folgenden Komponenten:

- Die vordefinierte, zuteilungsbezogene Datenquelle, physischen Maße und berechneten Maße.
- Anpassbare Zuteilungsgruppen mit maximal acht Ebenen.
- Eine Reihe von Anwendungsprogrammierschnittstellen (APIs) für die Zuteilung:

    - zuordnen
    - Neu zuordnen
    - Zuordnung aufheben
    - nutzen
    - abfragen

Der Prozess zum Konfigurieren der Zuteilungsfunktion besteht aus drei Schritten:

- Aktivieren Sie die Funktion in der Bestandsanzeige-App, indem Sie zu **Konfiguration \> Funktionsverwaltung und -einstellungen \> Zuteilung** gehen.
- Richten Sie die [Datenquelle](inventory-visibility-configuration.md#data-source-configuration) und ihre [Maße](inventory-visibility-configuration.md#data-source-configuration-physical-measures) ein.
- Richten Sie den Namen und die Hierarchie der Zuteilungsgruppe ein.

### <a name="predefined-data-source"></a>Vordefinierte Datenquelle

Wenn Sie die Zuteilungsfunktion aktivieren und die Konfigurationsaktualisierungs-API aufrufen, erstellt Bestandsanzeige eine vordefinierte Datenquelle und mehrere anfängliche Kennzahlen.

Die Datenquelle hat den Namen `@iv` Es enthält eine Reihe von standardmäßigen physikalischen Maßen. Sie können sie in der Bestandsanzeige-App anzeigen, indem Sie zu **Konfiguration \> Datenquelle**. Sie sollten **Datenquelle – @IV** sehen. Erweitern Sie die `@iv` Datenquelle, um die Liste der ersten physikalischen Maßnahmen anzuzeigen:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Wählen Sie die **Berechnete Maßnahmen** Registerkarte, um die ursprünglich berechnete Kennzahl mit dem Namen `@iv.@available_to_allocate` anzeigen:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Fügen Sie andere physische Measures zu dem berechneten Measure „für Zuordnung verfügbar“ hinzu

Um die Zuteilung zu verwenden, müssen Sie die Formel für die berechnete Kennzahl „für Zuteilung verfügbar“ (`@iv.@available_to_allocate`) korrekt einrichten. Sie haben zum Beispiel die `fno`-Datenquelle und das `onordered`-Measure, und die `pos`-Datenquelle und das `inbound`-Measure, und Sie möchten die Zuteilung für „Verfügbare Menge“ für die Summe von `fno.onordered` und `pos.inbound` durchführen. In diesem Fall, sollte `@iv.@available_to_allocate` bestimmte `pos.inbound` und `fno.onordered` Elemente in der Formel enthalten. Hier ist ein Beispiel:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Die Datenquelle `@iv` ist eine vordefinierte Datenquelle und die in `@iv` mit dem Präfix `@` festgelegten physischen Measures sind vordefinierte Measures. Diese Measures sind eine vordefinierte Konfiguration für die Zuordnungsfunktion, also ändern oder löschen Sie sie nicht, da Sie sonst wahrscheinlich auf unerwartete Fehler stoßen, wenn Sie die Zuordnungsfunktion verwenden.
>
> Sie können der vordefinierten berechneten Measure `@iv.@available_to_allocate` neue physische Measures hinzufügen, aber Sie dürfen ihren Namen nicht ändern.

### <a name="manage-allocation-groups"></a>Zuteilungsgruppen verwalten

Es können maximal acht Zuteilungsgruppennamen eingestellt werden. Die Gruppen haben eine Hierarchie. Befolgen Sie diese Schritte, um Zuteilungsgruppen anzuzeigen und zu aktualisieren.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration** und wählen Sie dann auf der **Zuteilung** Registerkarte **Konfiguration bearbeiten**. Standardmäßig gibt es eine Zuordnungshierarchie mit vier Ebenen: `Channel` (oberste Schicht), `customerGroup` (zweite Schicht), `Region` (dritte Schicht) und `OrderType` (vierte Schicht).
1. Sie können eine vorhandene Zuordnungsgruppe entfernen, indem Sie das **X** daneben auswählen. Sie können der Hierarchie auch neue Zuordnungsgruppen hinzufügen, indem Sie den Namen jeder neuen Gruppe direkt in das Feld eingeben.

    > [!IMPORTANT]
    > Seien Sie vorsichtig, wenn Sie die Zuweisungshierarchiezuordnung löschen oder ändern. Zur Anleitung siehe [Tipps zur Verwendung der Zuordnung](#allocation-tips).

1. Wenn Sie die Konfiguration der Zuordnungsgruppe und der Hierarchieeinstellungen abgeschlossen haben, speichern Sie Ihre Änderungen und wählen Sie dann **Konfiguration aktualisieren** oben rechts aus. Die Werte der konfigurierten Zuweisungsgruppen werden aktualisiert, wenn Sie eine Zuweisung erstellen, indem Sie entweder die Benutzeroberfläche oder API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate) verwenden. Einzelheiten zu beiden Ansätzen finden Sie weiter unten in diesem Artikel.

Wenn Sie vier Gruppennamen verwenden und diese auf \[`channel`, `customerGroup`, `region`, `orderType`\] festlegen, sind diese Namen für zuteilungsbezogene Anforderungen gültig, wenn Sie die Konfigurationsaktualisierungs-API aufrufen.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>Tipps zur Verwendung der Zuteilung

- Für jedes Produkt sollte die Zuteilungsfunktion dieselbe *Dimensionsebene* gemäß der von Ihnen in der [Konfiguration der Produktindexhierarchie](inventory-visibility-configuration.md#index-configuration) festgelegten Produktindexhierarchie verwenden. Angenommen, Ihre Indexhierarchie ist \[`Site`, `Location`, `Color`, `Size`\]. Wenn Sie eine bestimmte Menge für ein Produkt auf Dimensionsebene \[`Site`, `Location`, `Color`\] zuweisen, sollten Sie dieses Produkt, das nächste Mal wenn Sie es zuweisen möchten, auch auf derselben Ebene zuweisen \[`Site`, `Location`, `Color`\]. Wenn Sie die Ebene \[`Site`, `Location`, `Color`, `Size`\] oder \[`Site`, `Location`\] verwenden, werden die Daten inkonsistent sein.
- **Zuordnungsgruppen und Hierarchie ändern:** Wenn bereits Allokationsdaten im System vorhanden sind, führt das Löschen vorhandener Allokationsgruppen oder eine Verschiebung in der Allokationsgruppenhierarchie zu einer Beschädigung der bestehenden Zuordnung zwischen den Allokationsgruppen. Stellen Sie daher sicher, dass Sie alle alten Daten manuell bereinigen, bevor Sie Ihre neue Konfiguration aktualisieren. Da sich das Hinzufügen neuer Zuordnungsgruppen zur untersten Hierarchie jedoch nicht auf vorhandene Zuordnungen auswirkt, müssen Sie die Daten nicht bereinigen.
- Die Zuordnung gelingt nur, wenn das Produkt eine positive `available_to_allocate` Menge hat.
- Um Produkte von einer Gruppe *Zuordnungsebene* zu einer Untergruppe zuzuweisen, verwenden Sie die `Reallocate` API. Sie haben beispielsweise eine Zuordnungsgruppenhierarchie \[`channel`, `customerGroup`, `region`, `orderType`\] und Sie möchten ein Produkt aus der Zuordnungsgruppe zuordnen \[Online, VIP\] zur Unterverteilungsgruppe \[Online, VIP, EU\] verwenden Sie die `Reallocate` API, um die Menge zu verschieben. Wenn Sie die `Allocate` API verwenden, wird die Menge aus dem virtuellen gemeinsamen Pool zuordnen.
- Um die allgemeine Produktverfügbarkeit (den gemeinsamen Pool) anzuzeigen, verwenden Sie die [Verfügbar abfragen](inventory-visibility-api.md#query-on-hand) API, um den Bestandsbetrag *Für Zuteilung verfügbar* anzufordern. Auf der Grundlage dieser Informationen können Sie dann Zuordnungsentscheidungen treffen.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>Verwenden der Zuteilungs-API

Derzeit sind fünf Zuteilungs-APIs geöffnet:

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – Diese API wird verwendet, um die erste Zuteilung zu erstellen.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** – Diese API wird verwendet, um die zugeteilte Menge zurückzusetzen oder zu entfernen.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – Diese API wird verwendet, um die zugeteilte Menge von einer bestehende Zuweisung zu anderen Zuteilungsgruppen zu verschieben.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – Diese API wird verwendet, um die zugeteilte Menge abzuführen (zu verwenden).
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – Diese API wird verwendet, um bestehende Zuteilungsdatensätze gegen Zuteilungsgruppen und Hierarchie zu prüfen.

### <a name="allocate"></a>Zuordnen

Rufen Sie die `Allocate`-API zum Zuteilen eines Produkts mit bestimmten Dimensionen auf. Hier ist das Schema für den Anforderungstext.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Beispiel: Sie möchten dem Produkt *Fahrrad*, Standort *1*, Lagerplatz *11*, Farbe *rot*, Kanal *Online*, Kundengruppe *VIP* und Region *US* eine Menge von 10 zuteilen. Um diese Zuteilung vorzunehmen, können Sie einen Aufruf tätigen, der den folgenden Textinhalt hat.

```json
{
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Der Menge muss immer größer als 0 (null) sein.

### <a name="unallocate"></a>Zuteilung aufheben

Verwenden Sie die `Unallocate`-API zur Umkehrung der `Allocate`-Operation. Negative Mengen sind in einer `Allocate`-Operation nicht zulässig. Der Text von `Unallocate` ist identisch mit dem Text von `Allocate`.

### <a name="reallocate"></a>Neu zuordnen

Verwenden Sie die `Reallocate`-API, um eine zugeordnete Menge in eine andere Gruppenkombination zu verschieben. Hier ist das Schema für den Anforderungstext.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "groups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Beispielsweise können Sie zwei Fahrräder mit den Dimensionen \[Standort=1, Lagerplatz=11, Farbe=rot\] aus der Zuteilungsgruppe \[Online, VIP, USA\] in die Zuteilungsgruppe \[Online, VIP, EU\] verschieben, und zwar durch den Anruf der `Reallocate`-API und die Bereitstellung des folgenden Textkörpers.

```json
{
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

### <a name="consume"></a>Verbrauchsgüter

Verwenden Sie die `Consume`-API zum Buchen der Nutzungsmenge gegen die Zuteilung. Beispielsweise können Sie diese API verwenden, um die zugeordnete Menge in einige reale Kennzahlen zu verschieben. Hier ist das Schema für den Anforderungstext.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Beispielsweise gibt es acht zugeordnete Fahrräder mit den Dimensionen \[Standort=1, Lagerplatz=11, Farbe=rot\] für Zuteilungsgruppe \[Online, VIP, USA\]. Es wird die folgende Verfügbarkeitsformel verwendet:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

Die acht Fahrräder werden vom `pos.inbound`-Mesure zugeteilt.

Jetzt sind drei Fahrräder verkauft und werden aus dem Zuteilungspool genommen. Um diese diese Verschiebung zu registrieren, können Sie einen Aufruf tätigen, der den folgenden Anforderungstext hat.

```json
{
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Nach diesem Aufruf wird die zugeteilte Menge für das Produkt um 3 reduziert. Darüber hinaus generiert die Bestandsansicht ein Ereignis für verfügbare Änderungen, wobei `pos.inbound` = *-3* ist. Alternativ können Sie den `pos.inbound`-Wert behalten, wie er ist, und nur die zugeteilte Menge nutzen. In diesem Fall müssen Sie jedoch entweder ein anderes physikalisches Measure erstellen, um die genutzte Mengen beizubehalten, oder das vordefinierte Measure `@iv.@consumed` verwenden.

Beachten Sie in dieser Anforderung, dass das physikalische Measure, das Sie im Anforderungstext der Nutzung verwenden, den entgegengesetzten Modifikatortyp (Addition oder Subtraktion) verwenden sollte, verglichen mit dem im berechneten Measure verwendeten Modifikatortyp. In diesem Nutzungstext hat, `iv.inbound` also den Wert `Subtraction`, nicht `Addition`.

Die `fno`-Datenquelle kann nicht im Nutzungstext verwendet werden, da wir immer behauptet haben, dass die Bestandsichtbarkeit keine Daten für die `fno`-Datenquelle ändern kann. Der Datenfluss ist unidirektional, d. h. alle Mengenänderungen für die `fno`-Datenquelle müssen aus Ihrer Supply Chain Management-Umgebung stammen.

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Nutzung als Soft-Reservierung

Die `Consume`-API kann die zugewiesene Menge auch als Soft-Reservierung nutzen. In diesem Fall reduziert die `Consume`-Operation die zugewiesene Menge und nimmt dann eine Soft-Reservierung für diese Menge vor. Um diesen Ansatz zu verwenden, müssen Sie auch die [Soft-Reservierung](inventory-visibility-reservations.md)-Funktion der Bestandansicht verwenden.

Beispielsweise haben Sie einen Soft-Reservierung physischer Measue als `iv.softreserved` festgelegt. Die folgende Formel wird für das als Reserve verfügbare berechnete Measure verwendet:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

Um diese Einrichtung mit der Zuteilungsfunktion zu verwenden, fügen Sie `@iv.@allocated` zu `iv.available_to_reserve` hinzu, um die folgende Formel zu erstellen:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

Dann aktualisieren Sie `@iv.@available_to_allocate` auf den gleichen Wert.

Wenn Sie eine Menge von 3 nutzen und diese Menge direkt reservieren möchten, können Sie einen Anruf tätigen, der den folgenden Anforderungstext hat.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

Beachten Sie, dass in dieser Anfrage `iv.softreserved` den Wert `Addition`, nicht `Subtraction`, hat.

### <a name="query"></a>Abfrage

Verwenden Sie die `Query`-API zum Abrufen von zuteilungsbezogenen Informationen für einige Produkte. Sie können Dimensionsfilter und Zuteilungsgruppenfilter verwenden, um die Ergebnisse einzugrenzen. Die Dimensionen müssen genau mit denen übereinstimmen, die Sie abrufen möchten, z. B. \[Standort=1, Lagerplatz=11\] wird nicht verwandte Ergebnisse im Vergleich zu \[Standort=1, Lagerplatz=11, Farbe=rot\].

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Verwenden Sie zum Beispiel \[Standort=1, Lagerplatz=11, Farbe=rot\] und leere Gruppenfelder, um alle Zuteilungsdatensätze zu erhalten:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Verwenden Sie \[Standort=1, Lagerplatz=11, Farbe=rot\] und Gruppen \[Kanal=Online, Kundengruppe=VIP, Region=USA\], um die Zuteilungsdatensätze für diese Gruppe zu erhalten:

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Verwenden Sie die Zuordnungsbenutzeroberfläche

Sie können Zuweisungen manuell über die Benutzeroberfläche verwalten, indem Sie die Bestandsanzeige-App öffnen und zu **Operative Sichtbarkeit \> Zuteilung** gehen. Von dort aus können Sie alle Aktionen ausführen, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="create-an-allocation"></a>Eine Zuteilung erstellen

Befolgen Sie diese Schritte, um eine Zuweisung aus der **Zuteilung** Seite der Bestandsanzeige App zu erstellen.

1. Wählen Sie **Zuteilen**.
1. Legen Sie die Werte für Basisfelder, Dimensionen und Zielzuordnungsgruppen fest. (Wenn Sie die Erfassungsdatenquelle im Abschnitt **Maße** auswählen, verwenden Sie zunächst die Dropdown-Liste, um die Abmessungen anzugeben (z. B. `siteId`). Geben Sie dann Dimensionswerte in die angezeigten Felder ein.)
1. Wählen Sie **Senden**.

### <a name="consume-an-allocation"></a>Verbrauchen Sie eine Zuteilung

Wählen Sie **Verbrauchen**, um eine Zuteilung zu verbrauchen. Um sicherzustellen, dass Sie innerhalb der richtigen Zuordnungsgruppe und -hierarchie verbrauchen, geben Sie dieselben Gruppen von Organisations- und Dimensionsdetails ein, die Sie beim Erstellen der Zuordnung eingegeben haben.

### <a name="reallocate-an-allocation"></a>Eine Zuteilung neu zuordnen

Wählen Sie **Neu zuordnen**, um vorhandene zugeteilte Menge von einem Satz von Zuteilungsgruppen zu einem anderen verschieben.

### <a name="query-existing-allocations"></a>Vorhandene Zuordnungen abfragen

Wählen Sie **Abfrage**, und geben Sie dann Produkt-, Organisations-, Dimensions- und Zuordnungsgruppenwerte ein, um Abfrageergebnisse vorhandener Zuordnungen zu erhalten.
