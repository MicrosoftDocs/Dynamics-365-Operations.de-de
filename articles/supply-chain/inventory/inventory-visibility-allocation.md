---
title: Inventory Visibility-Bestandszuteilung
description: In diesem Artikel wird erläutert, wie Sie die Bestandzuweisungsfunktion einrichten und verwenden, mit der Sie dedizierten Bestand reservieren können, um sicherzustellen, dass Sie Ihre profitabelsten Kanäle oder Kunden bedienen können.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: f79497a24a5b4dd501bb0d13d9eaca7e98672533
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306113"
---
# <a name="inventory-visibility-inventory-allocation"></a>Bestandszuordnung für Bestandsichtbarkeit

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>Unternehmenshintergrund und -zweck

In vielen Fällen müssen Hersteller, Einzelhändler und andere Inhaber von Lieferkettenunternehmen Lagerbestände für wichtige Vertriebskanäle, Standorte oder Kunden oder für bestimmte Verkaufsveranstaltungen vorab zuordnen. Die Bestandszuteilung ist eine typische Praxis im operativen Planungsprozess des Vertriebs und wird durchgeführt, bevor die eigentlichen Vertriebsaktivitäten stattfinden und ein Auftrag erstellt wird.

Beispielsweise hat ein Fahrradhersteller einen begrenzten verfügbaren Lagerbestand für ein sehr beliebtes Fahrrad. Dieses Unternehmen führt sowohl Online- als auch In-Store-Verkäufe durch. In jedem Vertriebskanal hat das Unternehmen einige wichtige Unternehmenspartner (Marktplätze und große Einzelhändler), die verlangen, dass ein bestimmter Teil des verfügbaren Fahrradbestands für sie reserviert wird. Daher muss das Fahrradunternehmen in der Lage sein, die Lagerverteilung über die Kanäle hinweg auszugleichen und auch die Erwartungen seiner VIP-Partner zu erfüllen. Der beste Weg, beide Ziele zu erreichen, ist die Bestandszuordnung, sodass jeder Kanal und Einzelhändler bestimmte zugeteilte Mengen erhalten kann, die später an Kunden verkauft werden können.

Die Bestandszuteilung hat zwei grundlegende Geschäftszwecke:

- **Inventarschutz (Ringfencing)** – Organisationen möchten eingeschränkte oder begrenzte Bestände priorisierten Kanälen, Regionen, VIP-Kunden und Tochterunternehmen vorab zuordnen. Die Zuteilungsfunktion „Bestandssichtbarkeit“ zielt darauf ab, den zugteilten Bestand zu schützen, sodass andere Zuteilungen, Reservierungen oder andere Verkaufsanforderungen den zuvor zugeteilten Bestand nicht beeinflussen.
- **Überverkaufskontrolle** – Die Bestandsichtbarkeits-Zuteilungsfunktion zielt darauf ab, die zuvor zugeteilten Mengen einzuschränken, damit die empfangende Partei (z. B. ein Kanal oder eine Kundengruppe) sie nicht übermäßig verbraucht, wenn die tatsächliche Verkaufstransaktion auf einer Soft Reservierung in Kraft tritt.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Zuteilungsdefinition im Dienst zur Bestandsanzeige

Obwohl die Zuteilungsfunktion im Dienst zur Bestandsanzeige keine physischen Bestandsmengen reserviert, bezieht sie sich auf die verfügbare physische Bestandsmenge, um ihre anfängliche *für die Zuteilung verfügbare* Menge des virtuellen Pools zu definieren. Die Inventarzuteilung in der Bestandsanzeige ist eine weiche Zuteilung. Dies geschieht, bevor die eigentlichen Verkaufstransaktionen stattfinden, und hängt nicht von Aufträgen ab. Beispielsweise können Sie Ihren wichtigsten Vertriebskanälen oder großen Einzelhändlern Lagerbestände zuteilen, bevor Endkunden den Vertriebskanal oder das Einzelhandelsgeschäft besuchen, um sie zu kaufen.

Der Unterschied zwischen Bestandszuteilung und [Soft-Bestandsreservierung](inventory-visibility-reservations.md) ist, dass Soft-Reservierungen normalerweise mit tatsächlichen Verkaufstransaktionen (Auftragspositionen) verknüpft sind. Wenn Sie die Funktionen für Zuteilung und vorläufige Reservierung zusammen verwenden möchten, empfehlen wir daher, dass Sie zuerst eine Bestandszuteilung durchführen und dann eine vorläufige Reservierung für die zugeteilten Mengen vornehmen. Weitere Informationen finden Sie unter [Eine Soft-Reservierung nutzen](#consume-to-soft-reserved).

Mit der Bestandszuteilungsfunktion können Verkaufsplaner oder Betreuer von Hauptkunden wichtige Bestände über Zuteilungsgruppen (z. B. Kanäle, Regionen und Kundengruppen) hinweg verwalten und vorab zuordnen. Es unterstützt auch die Verfolgung, Anpassung und Analyse der Nutzung in Echtzeit anhand zugewiesener Mengen, sodass eine rechtzeitige Auffüllung oder Neuzuweisung erfolgen kann. Diese Fähigkeit, in Echtzeit Einblick in die Zuteilung, die Nutzung und die Zuteilungsbilanz zu haben, ist besonders bei Schnellverkaufs- oder Werbeveranstaltungen wichtig.

## <a name="terminology"></a>Terminologie

Die folgenden Begriffe und Konzepte sind bei Diskussionen über die Bestandszuteilung hilfreich:

- **Zuteilungsgruppe** – die Gruppe, der die Zuteilung gehört, z. B. ein Vertriebskanal, eine Kundengruppe oder eine Auftragsart.
- **Zuteilungsgruppenwert** – Der Wert jeder Zuteilungsgruppe. Zum Beispiel könnte *Netz* oder *Laden* der Wert der Vertriebskanalzuteilungsgruppe sein, wohingegen *VIP* oder *Normal* der Wert der Kundenzuteilungsgruppe sein kann.
- **Zuteilungshierarchie** – Ein Mittel, um Zuteilungsgruppen hierarchisch zusammenzufassen. Sie können beispielsweise *Kanal* als Hierarchiestufe 1, *Region* als Stufe 2 und *Kundengruppe* als Stufe 3 definieren. Während der Bestandszuteilung müssen Sie die Reihenfolge der Zuteilungshierarchie befolgen, wenn Sie den Wert der Zuteilungsgruppe angeben. Sie können beispielsweise 200 rote Fahrräder dem *Netz*-Kanal, der *London*-Region und der *VIP*-Kundengruppe zuteilen.
- **Für Zuteilung verfügbar** – der *virtuellen gemeinsamen Pool*, der die Menge angibt, die für eine weitere Zuteilung verfügbar ist. Es handelt sich um ein berechnetes Maß, das Sie mithilfe Ihrer eigenen Formel frei definieren können. Wenn Sie auch die Soft-Reservierungsfunktion verwenden, empfehlen wir Ihnen, dieselbe Formel zu verwenden, um „für Zuweisung verfügbar“ und „für Reservierung verfügbar“ zu berechnen.
- **Zugeteilt** – ein physisches Maß, das das zugeteilte Kontingent zeigt, das von den Zuteilungsgruppen genutzt werden kann.
- **Genutzt** – ein physisches Maß, das anzeigt, dass die Mengen, die genutzt wurden, mit der ursprünglich zugeteilten Menge verglichen werden. Wenn Zahlen zu dieser Maßeinheit hinzugefügt werden, wird die zugeteilte physische Maßeinheit automatisch reduziert.

Die folgende Abbildung zeigt den Geschäfts-Workflow für die Bestandszuteilung.

![Bestandsanzeige des Geschäfts-Workflows für die Zuzteilung.](media/inventory-visibility-allocation-flow.png "Bestandsanzeige des Geschäfts-Workflows für die Zuzteilung.")

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

Der Prozess zum Konfigurieren der Zuteilungsfunktion besteht aus zwei Schritten:

- Richten Sie die [Datenquelle](inventory-visibility-configuration.md#data-source-configuration) und ihre [Maße](inventory-visibility-configuration.md#data-source-configuration-physical-measures) ein.
- Richten Sie den Namen und die Hierarchie der Zuteilungsgruppe ein.

### <a name="predefined-data-source"></a>Vordefinierte Datenquelle

Wenn Sie die Zuteilungsfunktion aktivieren und die Konfigurationsaktualisierungs-API aufrufen, erstellt Bestandsanzeige eine vordefinierte Datenquelle und mehrere anfängliche Kennzahlen.

Die Datenquelle hat den Namen `@iv`

Hier sind die ersten physikalischen Maßnahmen:

- `@iv`
  - `@allocated`
  - `@cumulative_allocated`
  - `@consumed`
  - `@cumulative_consumed`

Hier sind die ersten berechneten Maßnahmen:

- `@iv`
  - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Fügen Sie andere physische Measures zu dem berechneten Measure „für Zuordnung verfügbar“ hinzu

Um die Zuteilung zu verwenden, müssen Sie die berechnete Kennzahl „für Zuteilung verfügbar“ (`@iv.@available_to_allocate`) einrichten. Sie haben zum Beispiel `fno`-Datenquelle und das `onordered`-Measure, die `pos`-Datenquelle und das `inbound`-Measure, und Sie möchten die Zuteilung für „Verfügbar“ für die Summe von `fno.onordered` und `pos.inbound` durchführen. In diesem Fall, sollte `@iv.@available_to_allocate` bestimmte `pos.inbound` und `fno.onordered` Elemente in der Formel enthalten. Hier ist ein Beispiel:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Die Datenquelle `@iv` ist eine vordefinierte Datenquelle und die in `@iv` mit dem Präfix `@` festgelegten physischen Measures sind vordefinierte Measures. Diese Measures sind eine vordefinierte Konfiguration für die Zuordnungsfunktion, also ändern oder löschen Sie sie nicht, da Sie sonst wahrscheinlich auf unerwartete Fehler stoßen, wenn Sie die Zuordnungsfunktion verwenden.
>
> Sie können der vordefinierten berechneten Measure `@iv.@available_to_allocate` neue physische Measures hinzufügen, aber Sie dürfen ihren Namen nicht ändern.

### <a name="change-the-allocation-group-name"></a>Den Namen der Zuteilungsgruppe ändern

Es können maximal acht Zuteilungsgruppennamen eingestellt werden. Die Gruppen haben eine Hierarchie.

Sie legen die Gruppennamen auf der Seite **Power App-Konfiguration für Bestandsanzeige** fest. Um diese Seite zu öffnen, öffnen Sie die App für die Bestandsanzeige in Ihrer Microsoft Dataverse-Umgebung und wählen Sie **Konfiguration \> Zuteilung** aus.

Wenn Sie beispielsweise vier Gruppennamen verwenden und diese auf \[`channel`, `customerGroup`, `region`, `orderType`\] festlegen, sind diese Namen für zuteilungsbezogene Anforderungen gültig, wenn Sie die Konfigurationsaktualisierungs-API aufrufen.

### <a name="allocation-using-tips"></a>Zuteilung mit Tipps

- Für jedes Produkt sollte die Zuteilungsfunktion dieselbe *Dimensionsebene* gemäß der von Ihnen in der [Konfiguration der Produktindexhierarchie](inventory-visibility-configuration.md#index-configuration) festgelegten Produktindexhierarchie verwenden. Angenommen, Ihre Indexhierarchie ist \[`Site`, `Location`, `Color`, `Size`\]. Wenn Sie eine bestimmte Menge für ein Produkt auf Dimensionsebene \[`Site`, `Location`, `Color`\] zuweisen, sollten Sie dieses Produkt, das nächste Mal wenn Sie es zuweisen möchten, auch auf derselben Ebene zuweisen \[`Site`, `Location`, `Color`\]. Wenn Sie die Ebene \[`Site`, `Location`, `Color`, `Size`\] oder \[`Site`, `Location`\] verwenden, werden die Daten inkonsistent sein.
- Das Ändern des Namens der Zuteilungsgruppe wirkt sich nicht auf die im Dienst gespeicherten Daten aus.
- Die Zuteilung sollte erfolgen, nachdem das Produkt die positive verfügbare Menge hat.
- Um Produkte von einer Gruppe *Zuordnungsebene* zu einer Untergruppe zuzuweisen, verwenden Sie die `Reallocate` API. Sie haben beispielsweise eine Zuordnungsgruppenhierarchie \[`channel`, `customerGroup`, `region`, `orderType`\] und Sie möchten ein Produkt aus der Zuordnungsgruppe zuordnen \[Online, VIP\] zur Unterverteilungsgruppe \[Online, VIP, EU\] verwenden Sie die `Reallocate` API, um die Menge zu verschieben. Wenn Sie die `Allocate` API verwenden, wird die Menge aus dem virtuellen gemeinsamen Pool zuordnen.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a>Verwenden der Zuteilungs-API

Derzeit sind fünf Zuteilungs-APIs geöffnet:

- POST /api/environment/{environmentId}/allocation/allocate
- POST /api/environment/{environmentId}/allocation/unallocate
- POST /api/environment/{environmentId}/allocation/reallocate
- POST /api/environment/{environmentId}/allocation/consume
- POST /api/environment/{environmentId}/allocation/query

#### <a name="allocate"></a>Zuordnen

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
    "id": "???",
    "productId": "Bike",
    "groups": {
        "channel": "Online",
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

#### <a name="unallocate"></a>Zuteilung aufheben

Verwenden Sie die `Unallocate`-API zur Umkehrung der `Allocate`-Operation. Negative Mengen sind in einer `Allocate`-Operation nicht zulässig. Der Text von `Unallocate` ist identisch mit dem Text von `Allocate`.

#### <a name="reallocate"></a>Neu zuordnen

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
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Online",
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

#### <a name="consume"></a>Verbrauchsgüter

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
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
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

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Nutzung als Soft-Reservierung

Die `Consume`-API kann die zugewiesene Menge auch als Soft-Reservierung nutzen. In diesem Fall reduziert die `Consume`-Operation die zugewiesene Menge und nimmt dann eine Soft-Reservierung für diese Menge vor. Um diesen Ansatz zu verwenden, müssen Sie auch die [Soft-Reservierung](inventory-visibility-reservations.md)-Funktion der Bestandansicht verwenden.

Beispielsweise haben Sie einen Soft-Reservierungsmodifikator (Measue) als `iv.softreserved` festgelegt. Die folgende Formel wird für das als Reserve verfügbare berechnete Measure verwendet:

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
        "channel": "Online",
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

#### <a name="query"></a>Abfrage

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
        "channel": "Online",
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
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
