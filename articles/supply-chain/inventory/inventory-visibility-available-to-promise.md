---
title: Inventory Visibility hat Lagerbestandsänderungen geplant und kann diese versprechen
description: In diesem Thema wird beschrieben, wie Sie künftige Lagerbestandsänderungen planen und ATP-Mengen (Available-to-Promise) berechnen können.
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 7456f87bede7bd0073223fa4762f96f919799e06
ms.sourcegitcommit: 38d97efafb66de298c3f504b83a5c9b822f5a62a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2022
ms.locfileid: "8763252"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Inventory Visibility hat Lagerbestandsänderungen geplant und kann diese versprechen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt, wie Sie die Funktion *Zeitplan für Lagerbestandsänderungen* festlegen, um künftige Lagerbestandsänderungen zu planen und ATP-Mengen (Available-to-Promise) zu berechnen. ATP ist die Menge eines Elements, die verfügbar ist und einem Kunden in der nächsten Periode zugesagt werden kann. Die Verwendung dieser Berechnung kann Ihre Funktionalitäten bei der Auftragsabwicklung erheblich verbessern.

Bei vielen Herstellern, Einzelhändlern oder Verkäufern reicht es nicht aus, zu wissen, was gerade im Lagerbestand ist. Sie müssen vollen Einblick in die zukünftige Verfügbarkeit haben. Diese zukünftige Verfügbarkeit sollte den zukünftigen Vorrat, den zukünftigen Bedarf und die ATP berücksichtigen.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>Aktivieren Sie die Funktionen und legen Sie sie fest

Bevor Sie ATP verwenden können, müssen Sie eine oder mehrere berechnete Messungen zur Berechnung der ATP-Mengen festlegen. Außerdem müssen Sie die Funktion einschalten und die ATP-Einstellungen unter Microsoft Power Apps festlegen.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Berechnete Messungen für ATP-Mengen festlegen

Die *ATP berechnete Kennzahl* ist eine vordefinierte berechnete Kennzahl, die in der Regel verwendet wird, um den Lagerbestand zu ermitteln, der derzeit verfügbar ist. Die *Liefermenge* ist die Summe der Größen für die physikalischen Maße, die den Modifikatortyp *Zusatz* aufweisen, und die *Nachfragemenge* ist die Summe der Größen für die physikalischen Maße, die den Modifikatortyp *Subtraktion* aufweisen.

Sie können mehrere berechnete Messungen hinzufügen, um mehrere ATP-Mengen zu berechnen. Die Gesamtzahl der unterschiedlichen physischen Measures für alle von ATP berechneten Measures sollte jedoch weniger als neun betragen.

> [!IMPORTANT]
> Ein berechnetes Measure ist eine Zusammenstellung von physikalischen Measures. Seine Formel kann nur physikalische Measures ohne Duplikate enthalten, keine berechneten Measures.

Sie legen zum Beispiel die folgende berechnete Messung fest:

**Auf Lagerbestand** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) - (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

Die Summe (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) steht für den Vorrat und die Summe (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) für den Bedarf. Die berechnete Messung kann also folgendermaßen verstanden werden:

**Auf Lagerbestand** = *Vorrat* - *Bedarf*

Sie können eine weitere berechnete Kennzahl hinzufügen, um die ATP-Menge **On-hand-physical** zu berechnen.

**On-hand-physical** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

Es gibt acht unterschiedliche physikalische Measures für diese beiden ATP-berechneten Measures: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical* und *Outbound*.

Weitere Informationen über berechnete Messungen finden Sie unter [Berechnete Messungen](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Schalten Sie die Funktion Lagerbestand ändern ein und konfigurieren Sie die ATP-Einstellungen

Führen Sie diese Schritte aus, um die Funktion *Zeitplan für Lagerbestandwechsel* in Power Apps zu aktivieren und die ATP-Einstellungen zu konfigurieren.

1. Melden Sie sich bei Power Apps an und öffnen Sie Inventory Visibility.
1. Öffnen Sie die Seite **Konfiguration**.
1. Schalten Sie auf der Registerkarte **Funktionsverwaltung** die Funktion *Zeitplan ändern* ein.
1. Wählen Sie die Registerkarte **ATP-Einstellung**.
1. Wenn Sie Inventory Visibility abfragen, erhalten Sie ein Ergebnis, das jede berechnete ATP-Kennzahl enthält, die Sie hier hinzufügen. Wählen Sie **Hinzufügen**, um eine neue berechnete Messung für ATP hinzuzufügen.
1. Stellen Sie die folgenden Felder ein:

    - **Datenquelle** - Wählen Sie die Datenquelle, die mit der berechneten Messung verknüpft ist.
    - **Berechnete Messung** - Wählen Sie die berechnete Messung aus, die mit der ausgewählten Datenquelle verknüpft ist und die Sie verwenden möchten, um den aktuell verfügbaren Lagerbestand zu ermitteln.
    - **Planungszeitraum** - Geben Sie die Anzahl der Tage ein, an denen Benutzer geplante Änderungen des Lagerbestands ansehen und senden können, wenn die ausgewählte berechnete Kennzahl verwendet wird. Benutzer, die Lagerbestandsinformationen abfragen, erhalten den Lagerbestand, die geplanten Bestandsveränderungen und die ATP für jeden Tag in diesem Zeitraum, beginnend mit dem aktuellen Datum. Wählen Sie eine ganze Zahl zwischen 1 und 7.

    > [!IMPORTANT]
    > Der Planungszeitraum umfasst das aktuelle Datum. Daher können Benutzer Lagerbestandsänderungen so planen, dass sie jederzeit ab dem aktuellen Datum (dem Tag, an dem die Änderung gesendet wird) bis zu (Planungszeitraum - 1) Tagen in der Zukunft stattfinden.

1. Wählen Sie **Speichern** aus.
1. Wiederholen Sie die Schritte 5 bis 7, bis Sie alle berechneten Messungen, die Sie für ATP benötigen, hinzugefügt haben.
1. Wenn Sie alle erforderlichen Einstellungen festgelegt haben, wählen Sie **Konfiguration aktualisieren**.

Weitere Informationen finden Sie unter [Komplettieren und Aktualisieren der Konfiguration](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Wie der Lagerbestandswechselplan und die ATP-Berechnungen funktionieren

Ein *Zeitplan für Lagerbestandsänderungen* legt die voraussichtlichen Termine und Mengen für geplante Lagerbestandsänderungen fest. Sie können einen Zeitplan für Lagerbestandsänderungen an Inventory Visibility senden, vorausgesetzt, die Daten liegen innerhalb des Zeitraums, der durch die Einstellung **Zeitplanperiode** festgelegt ist (siehe Abschnitt [Funktionen aktivieren und einrichten](#setup)). Benutzer, die Lagerbestandsinformationen abfragen, erhalten den Lagerbestand, die geplanten Lagerbestandsänderungen und die ATP für jeden Tag in diesem Zeitraum.

Geplante Änderungen sind zunächst nicht verbindlich und wirken sich daher nicht auf Ihren tatsächlichen Lagerbestand im System aus. Um die Änderungen zu bestätigen, müssen Sie ein *Änderungsereignis im Lagerbestand* senden, das die tatsächlich verfügbare Menge im Lagerbestand aktualisiert. Anschließend müssen Sie die geplante Änderung rückgängig machen, indem Sie einen Plan zur Änderung des Lagerbestands für eine entsprechende negative Menge senden.

Sie bestellen z.B. 10 Fahrräder und erwarten, dass sie morgen geliefert werden. Sie senden also einen Plan für Lagerbestandsänderungen mit einer eingehenden Menge von 10 und einem Datum für morgen. Wenn die Bestellung am nächsten Tag eintrifft, nehmen Sie die Fahrräder in Ihren physischen Lagerbestand auf. Anschließend müssen Sie die Änderung in Ihrem System bestätigen, um den tatsächlichen Lagerbestand zu aktualisieren. Um die Änderung zu bestätigen, senden Sie ein Ereignis zur Änderung des Lagerbestands mit einer eingehenden Menge von 10. Anschließend senden Sie einen Lagerbestands-Änderungsplan mit einer eingehenden Menge von -10, um die geplante Änderung rückgängig zu machen.

Wenn Sie Inventory Visibility nach Lagerbeständen und ATP-Mengen abfragen, erhalten Sie für jeden Tag in der Planperiode die folgenden Informationen:

- **Datum** - Das Datum, für das das Ergebnis gilt. Die Zeitzone ist die koordinierte Weltzeit (UTC).
- **Auf Lagerbestand** - Die tatsächliche Menge im Lagerbestand für das angegebene Datum. Diese Berechnung erfolgt auf der Grundlage der ATP-berechneten Messung, die für Inventory Visibility konfiguriert ist.
- **Geplantes Angebot** - Die Summe aller geplanten eingehenden Mengen, die zum angegebenen Datum noch nicht physisch zum sofortigen Verbrauch oder Versand verfügbar sind.
- **Geplanter Bedarf** - Die Summe aller geplanten ausgehenden Mengen, die bis zum angegebenen Datum noch nicht verbraucht oder versandt wurden.
- **ATP-Menge** - Die prognostizierte Mindestmenge an Lagerbestand, die ab dem angegebenen Datum bis zum Ende der Einteilungsperiode verfügbar ist. Diese Menge umfasst alle geplanten Mengenanpassungen. Es handelt sich um die maximale Menge, die zum aktuellen Datum für die Lieferung oder den Verbrauch an diesem Tag zugesagt werden kann.

Wenn das aktuelle Datum z.B. der 1. Februar 2022 und der Zeitplanzeitraum 7 ist, können Benutzer geplante Lagerbestandsänderungen senden, die voraussichtlich vom 1. bis zum 7. Februar 2022 stattfinden werden. In diesem Fall wird die ATP-Menge für den 3. Februar beispielsweise auf der Grundlage des Lagerbestands für diesen Tag und der geplanten Mengen vom 3. bis 7. Februar berechnet.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie sich eine Reihe von geplanten Mengenänderungen auf die Lagerbestände und ATP-Mengen auswirkt, die Inventory Visibility meldet. Es zeigt Ihnen auch, wie Sie eine geplante Änderung bestätigen, wie eine bestätigte Änderung die Ergebnisse beeinflusst und was passieren kann, wenn Sie eine geplante Änderung nicht bestätigen.

Die Ergebnisse in diesem Beispiel zeigen einen *hochgerechneten Lagerbestand* an. Dieser Wert enthält alle geplanten Aktualisierungen zur Veranschaulichung, wird aber nicht tatsächlich gemeldet, wenn Sie Inventory Visibility abfragen.

1. Die folgenden Einstellungen werden für Ihr System auf der Seite **ATP-Einstellung** in Power Apps festgelegt:

    - **ATP berechnete Messung** - Sie haben eine berechnete Messung, die den Namen *Abgabe* trägt. Er wird berechnet als *Bestand = Vorrat - Bedarf*. Sie wählen diese Messung hier aus.
    - **Planungszeitraum** - Sie wählen *7*.

1. Außerdem gelten die folgenden Bedingungen:

    - Das aktuelle Datum ist der 1. Februar 2022.
    - Der aktuelle Lagerbestand beträgt 20 Stück.

1. Für das aktuelle Datum (1. Februar 2022) senden Sie eine geplante Bedarfsmenge von 3 an Inventory Visibility. Der prognostizierte Lagerbestand beträgt also 17. Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

    | Datum | Bestand | Geplantes Angebot | Geplanter Bedarf | Hochgerechneter Lagerbestand | VfZ |
    | --- | --- | --- | --- | --- | --- |
    | 01.02.2022 | 20 | | 3 | 17 | 17 |
    | 02.02.2022 | 20 | | | 17 | 17 |
    | 03.02.2022 | 20 | | | 17 | 17 |
    | 04.02.2022 | 20 | | | 17 | 17 |
    | 05.02.2022 | 20 | | | 17 | 17 |
    | 06.02.2022 | 20 | | | 17 | 17 |
    | 07.02.2022 | 20 | | | 17 | 17 |

1. Am aktuellen Datum (1. Februar 2022) senden Sie eine geplante Vorratsmenge von 10 für den 3. Februar 2022. Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

    | Datum | Bestand | Geplantes Angebot | Geplanter Bedarf | Hochgerechneter Lagerbestand | VfZ |
    | --- | --- | --- | --- | --- | --- |
    | 01.02.2022 | 20 | | 3 | 17 | 17 |
    | 02.02.2022 | 20 | | | 17 | 17 |
    | 03.02.2022 | 20 | 10 | | 27 | 27 |
    | 04.02.2022 | 20 | | | 27 | 27 |
    | 05.02.2022 | 20 | | | 27 | 27 |
    | 06.02.2022 | 20 | | | 27 | 27 |
    | 07.02.2022 | 20 | | | 27 | 27 |

1. Am aktuellen Datum (1. Februar 2022) senden Sie die folgenden geplanten Mengenänderungen:

    - Bedarfsmenge von 15 für Februar 4, 2022
    - Vorrat von 1 für Februar 5, 2022
    - Vorrat von 3 für Februar 6, 2022

    Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

    | Datum | Bestand | Geplantes Angebot | Geplanter Bedarf | Hochgerechneter Lagerbestand | VfZ |
    | --- | --- | --- | --- | --- | --- |
    | 01.02.2022 | 20 | | 3 | 17 | 12 |
    | 02.02.2022 | 20 | | | 17 | 12 |
    | 03.02.2022 | 20 | 10 | | 27 | 12 |
    | 04.02.2022 | 20 | | September | 12 | 12 |
    | 05.02.2022 | 20 | 1 | | 13 | 13 |
    | 06.02.2022 | 20 | 3 | | 16 | 16 |
    | 07.02.2022 | 20 | | | 16 | 16 |

1. Am aktuellen Datum (1. Februar 2022) liefern Sie die geplante Bedarfsmenge von 3. Daher müssen Sie diese Änderung bestätigen, damit sie sich in Ihrem tatsächlichen Lagerbestand niederschlägt. Um die Änderung zu bestätigen, senden Sie ein Ereignis zur Bestandsänderung mit einer ausgehenden Menge von 3. Sie machen die geplante Änderung rückgängig, indem Sie einen Bestandsänderungsplan senden, der eine ausgehende Menge von -3 aufweist. Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

    | Datum | Bestand | Geplantes Angebot | Geplanter Bedarf | Hochgerechneter Lagerbestand | VfZ |
    | --- | --- | --- | --- | --- | --- |
    | 01.02.2022 | 17 | | 0 | 17 | 12 |
    | 02.02.2022 | 17 | | | 17 | 12 |
    | 03.02.2022 | 17 | 10 | | 27 | 12 |
    | 04.02.2022 | 17 | | September | 12 | 12 |
    | 05.02.2022 | 17 | 1 | | 13 | 13 |
    | 06.02.2022 | 17 | 3 | | 16 | 16 |
    | 07.02.2022 | 17 | | | 16 | 16 |

1. Am nächsten Tag (2. Februar 2022) verschiebt sich die Einteilungsperiode um einen Tag nach vorne. Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

    | Datum | Bestand | Geplantes Angebot | Geplanter Bedarf | Hochgerechneter Lagerbestand | VfZ |
    | --- | --- | --- | --- | --- | --- |
    | 02.02.2022 | 17 | | | 17 | 12 |
    | 03.02.2022 | 17 | 10 | | 27 | 12 |
    | 04.02.2022 | 17 | | September | 12 | 12 |
    | 05.02.2022 | 17 | 1 | | 13 | 13 |
    | 06.02.2022 | 17 | 3 | | 16 | 16 |
    | 07.02.2022 | 17 | | | 16 | 16 |
    | 08.02.2022 | 17 | | | 16 | 16 |

1. Zwei Tage später (4. Februar 2022) ist die Vorratsmenge von 10, die für den 3. Februar vorgesehen war, jedoch immer noch nicht eingetroffen. Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

    | Datum | Bestand | Geplantes Angebot | Geplanter Bedarf | Hochgerechneter Lagerbestand | VfZ |
    | --- | --- | --- | --- | --- | --- |
    | 04.02.2022 | 17 | | September | 2 | 2 |
    | 05.02.2022 | 17 | 1 | | 3 | 3 |
    | 06.02.2022 | 17 | 3 | | 6 | 6 |
    | 07.02.2022 | 17 | | | 6 | 6 |
    | 08.02.2022 | 17 | | | 6 | 6 |
    | 09.02.2022 | 17 | | | 6 | 6 |
    | 10.02.2022 | 17 | | | 6 | 6 |

    Wie Sie sehen, haben die geplanten (aber nicht bestätigten) Änderungen des Lagerbestands keinen Einfluss auf die tatsächliche Lagerbestandsmenge.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>Senden Sie Änderungspläne, Änderungsereignisse und ATP-Abfragen über die API

Sie können die folgenden URLs der Anwendungsprogrammierschnittstelle (API) verwenden, um Änderungspläne für den Lagerbestand, Änderungsereignisse und Abfragen zu senden.

| Pfad | Methode | Description |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Erstellen Sie eine geplante Änderung des Lagerbestands. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Erstellen Sie mehrere geplante Änderungen im Lagerbestand. |
| `/api/environment/{environmentId}/onhand` | `POST` | Erstellen Sie ein Ereignis für Lagerbestandsänderungen. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Erzeugen Sie mehrere Ereignisse. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Abfrage mit Hilfe der `POST`-Methode. |
| `/api/environment/{environmentId}/onhand` | `GET` | Abfrage mit Hilfe der `GET`-Methode. |

Weitere Informationen finden Sie unter [Inventory Visibility öffentliche APIs](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Einen Zeitplan für Lagerbestandsänderungen erstellen

Ein Zeitplan für Lagerbestandsänderungen wird erstellt, indem Sie eine `POST`-Anfrage an die entsprechende Inventory Visibility Service-URL senden (siehe den Abschnitt [Änderungszeitpläne, Änderungsereignisse und ATP-Abfragen über die API senden](#api-urls)). Sie können auch Massenanfragen senden.

Ein Zeitplan für Lagerbestandsänderungen kann nur erstellt werden, wenn das geplante Datum zwischen dem aktuellen Datum und dem Ende der aktuellen Zeitplanperiode liegt. Das DateTime-Format sollte *Tag.Monat.Jahr* (zum Beispiel, **01.02.2022**) sein. Das Zeitformat muss nur auf den Tag genau sein.

Diese API erstellt einen einzelnen Zeitplan für Lagerbestandsänderungen.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Das folgende Beispiel zeigt einen Beispielkörperinhalt ohne `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Mehrere Zeitpläne für Lagerbestandänderungen erstellen

Diese API kann mehrere Datensätze gleichzeitig erstellen. Die einzigen Unterschiede zwischen dieser API und der Einzelereignis-API sind die Werte `Path` und `Body`. Bei dieser API liefert `Body` ein Array von Datensätzen. Die maximale Anzahl an Datensätzen ist 512. Daher kann die Bulk-API für Zeitpläne für Lagerbestandsänderungen bis zu 512 geplante Änderungen gleichzeitig unterstützen.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

Das folgende Beispiel zeigt einen Beispielkörperinhalt.

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Erstellen von Ereignissen bei Lagerbestandsänderungen

Ereignisse zur Änderung des Lagerbestands werden durch Senden einer `POST`-Anfrage an die entsprechende URL des Inventory Visibility Service ausgelöst (siehe Abschnitt [Änderungszeitpläne, Änderungsereignisse und ATP-Abfragen über die API senden](#api-urls)). Sie können auch Massenanfragen senden.

> [!NOTE]
> Ereignisse zur Änderung des Lagerbestands sind keine Besonderheit der ATP-Funktionalität, sondern sind Teil der Standard-API von Inventory Visibility. Wir haben dieses Beispiel aufgenommen, weil Ereignisse bei der Arbeit mit ATP von Bedeutung sind. Ereignisse zur Änderung des Lagerbestands ähneln den Reservierungen zur Änderung des Lagerbestands, aber die Nachrichten zu den Ereignissen müssen an eine andere API-URL gesendet werden, und die Nachrichten enthalten eine `quantities` statt einer `quantityByDate`. Weitere Informationen zu den Ereignissen der Lagerbestandsänderung und anderen Funktionen der Inventory Visibility API finden Sie unter [Öffentliche APIs für Inventory Visibility](inventory-visibility-api.md#create-one-onhand-change-event).

Das folgende Beispiel zeigt einen Anfragekörper, der ein einzelnes Ereignis zur Änderung des Lagerbestands enthält.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Abfrage der geplanten Lagerbestandsänderungen und ATP-Ergebnisse

Sie können geplante Lagerbestandsänderungen und ATP-Ergebnisse abfragen, indem Sie entweder eine `POST`-Anfrage oder eine `GET`-Anfrage an die entsprechende API-URL senden (siehe den Abschnitt [Änderungspläne, Änderungsereignisse und ATP-Abfragen über die API senden](#api-urls)).

Legen Sie in Ihrer Anfrage `QueryATP` auf *wahr* fest, wenn Sie geplante Lagerbestandsänderungen und ATP-Ergebnisse abfragen möchten.

- Wenn Sie die Anfrage mit der `GET`-Methode senden, legen Sie diesen Parameter in der URL fest.
- Wenn Sie den Antrag mit der Methode `POST` senden, legen Sie diesen Parameter im Antragstext fest.

> [!NOTE]
> Unabhängig davon, ob der Parameter `returnNegative` im Abfragetext auf *wahr* oder *falsch* festgelegt ist, enthält das Ergebnis negative Werte, wenn Sie geplante Lagerbestandsänderungen und ATP-Ergebnisse abfragen. Diese negativen Werte werden berücksichtigt, denn wenn nur Bedarfsbestellungen eingeplant werden oder wenn die Vorratsmengen geringer sind als die Bedarfsmengen, werden die eingeplanten Lagerbestandsänderungen negativ sein. Wenn negative Werte nicht berücksichtigt würden, wären die Ergebnisse verwirrend. Weitere Informationen über diese Option und wie sie bei anderen Abfragetypen funktioniert, finden Sie unter [Inventory Visibility public APIs](inventory-visibility-api.md#query-with-post-method).

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Das folgende Beispiel zeigt, wie Sie einen Anfragekörper erstellen, der mit der Methode `POST` an Inventory Visibility gesendet werden kann.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>Beispiel für eine GET-Methode

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Das folgende Beispiel zeigt, wie Sie eine Anfrage-URL als `GET`-Anfrage erstellen.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Das Ergebnis dieser `GET`-Anfrage ist genau dasselbe wie das Ergebnis der `POST`-Anfrage im vorherigen Beispiel.

### <a name="query-result-example"></a>Beispiel für ein Abfrageergebnis

Die beiden vorherigen Abfragebeispiele könnten die folgende Antwort ergeben. Für dieses Beispiel ist das System mit den folgenden Einstellungen festgelegt:

- **ATP berechnete Messung:** *iv.onhand = pos.inbound – pos.outbound*
- **Planungszeitraum:** *7*

Hier sehen Sie ein Beispiel für den Antworttext.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
