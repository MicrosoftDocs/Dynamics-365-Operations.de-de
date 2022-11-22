---
title: Öffentliche Inventory Visibility-APIs
description: Dieser Artikel beschreibt die öffentlichen APIs, die von Inventory Visibility bereitgestellt werden.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762833"
---
# <a name="inventory-visibility-public-apis"></a>Öffentliche Inventory Visibility-APIs

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die öffentlichen APIs, die von Inventory Visibility bereitgestellt werden.

Die öffentliche REST-API des Bestandssichtbarkeit-Add-Ins stellt mehrere spezifische Endpunkte für die Integration bereit. Es werden vier Hauptinteraktionstypen unterstützt:

- Verbuchung von Änderungen des Lagerbestands aus einem externen System in das Add-In
- Festlegen oder Außerkraftsetzen von Lagerbestandsmengen im Add-In von einem externen System
- Buchen von Reservierungsereignissen an das Add-In von einem externen System
- Abfrage aktueller Lagerbestände von einem externen System

In der folgenden Tabelle sind die derzeit verfügbaren APIs aufgeführt:

| Pfad | Methode | Beschreibung |
|---|---|---|
| /api/environment/{environmentId}/onhand | Buchen | [Ein Ereignis zur Änderung des Lagerbestands erstellen](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | Buchen | [Mehrere Änderungsereignisse erstellen](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Buchen | [Festlegen/Überschreiben von Lagerbeständen](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Veröffentlichen | [Ein Ereignis für eine Soft-Reservierung erstellen](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Veröffentlichen | [Mehrere Soft-Reservierungsereignisse erstellen](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | Veröffentlichen | [Ein Soft-Reservierungsereignis umkehren](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Veröffentlichen | [Mehrere Soft-Reservierungsereignisse umkehren](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Buchen | [Eine geplante Änderung des Lagerbestands erstellen](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Veröffentlichen | [Erstellen Sie mehrere Lagerbestandsänderungen mit Daten](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Veröffentlichen | [Abfrage durch Verwendung der Methode POST](#query-with-post-method) (empfohlen) |
| /api/environment/{environmentId}/onhand | Abrufen | [Abfrage mit Hilfe der get-Methode](#query-with-get-method) |
| /api/umgebung/{environmentId}/onhand/exactquery | Veröffentlichen | [Exakte Abfrage durch Verwendung der Methode POST](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | Veröffentlichen | [Ein Zuweisungsereignis erstellen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | Buchen | [Ein Ereignis zum Aufheben einer Zuweisung erstellen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | Buchen | [Ein Neuzuweisungsereignis erstellen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | Buchen | [Ein Verbrauchsereignis erstellen](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | Buchen | [Zuordnungsergebnis abfragen](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Der Teil {environmentId} des Pfades ist die Umgebungs-ID in Microsoft Dynamics Lifecycle Services.
> 
> Die Bulk-API kann maximal 512 Datensätze für jede Anfrage zurückgeben.

Microsoft hat eine standardmäßige *Postman* Abfrage-Sammlung bereitgestellt. Sie können diese Sammlung in Ihre *Postman*-Software importieren, indem Sie den folgenden gemeinsamen Link verwenden: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Finden Sie den Endpunkt entsprechend Ihrer Lifecycle Services Umgebung

Der Microservice von Inventory Visibility wird auf Microsoft Azure Service Fabric bereitgestellt, und zwar in mehreren Regionen und Gegenden. Es gibt derzeit keinen zentralen Endpunkt, der Ihre Anfrage automatisch an die entsprechende Geographie und Region weiterleiten kann. Daher müssen Sie die Informationen nach folgendem Muster zu einer URL zusammenstellen:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Die Kurzbezeichnung der Region finden Sie in der Lifecycle Services Umgebung. In der folgenden Tabelle sind die Regionen aufgeführt, die derzeit verfügbar sind.

| Azure-Region        | Region Kurzname |
| ------------------- | ----------------- |
| Australien Ost      | eau               |
| Australien Südost | seau              |
| Kanada Mitte      | cca               |
| Kanada Ost         | eca               |
| Europa, Norden        | neu               |
| Europa, Westen         | weu               |
| USA, Osten             | eus               |
| USA, Westen             | wus               |
| South UK            | suk               |
| West UK             | wuk               |
| Japan, Osten          | ejp               |
| Japan, Westen          | wjp               |
| Indien, Mitte       | cin               |
| Indien, Süden         | sin               |
| Schweiz, Norden   | nch               |
| Schweiz, Westen    | wch               |
| Frankreich, Süden        | sfr               |
| Asien, Osten           | eas               |
| Asien, Südosten     | seas              |
| VAE, Norden           | nae               |
| Norwegen, Osten         | eno               |
| Norwegen, Westen         | wno               |
| Südafrika, Westen   | wza               |
| Südafrika, Norden  | nza               |

Die Inselnummer gibt an, wo Ihre Lifecycle Services Umgebung auf Service Fabric bereitgestellt ist. Es gibt derzeit keine Möglichkeit, diese Informationen von der Benutzerseite aus zu erhalten.

Microsoft hat eine Benutzeroberfläche (UI) in Power Apps eingebaut, so dass Sie den kompletten Endpunkt des Microservices erhalten können. Weitere Informationen finden Sie unter [Finden Sie den Dienst-Endpunkt](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Authentifizierung

Das Sicherheits-Token der Plattform wird für den Aufruf der öffentlichen API von Inventory Visibility verwendet. Daher müssen Sie ein *Azure Active Directory (Azure AD) Token* generieren, indem Sie Ihre Azure AD Anwendung verwenden. Sie müssen dann das Azure AD-Token verwenden, um das *Zugriffstoken* vom Sicherheitsdienst zu erhalten.

Microsoft stellt eine standardmäßige *Postman*-Token-Abfragesammlung bereit. Sie können diese Sammlung in Ihre *Postman*-Software importieren, indem Sie den folgenden gemeinsamen Link verwenden: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Gehen Sie folgendermaßen vor, um ein Sicherheitsdienst-Token zu erhalten.

1. Melden Sie sich am Azure-Portal an und suchen Sie dort die `clientId`- und `clientSecret`-Werte für Ihre Dynamics 365 Supply Chain Management-App.
1. Holen Sie ein Azure AD-Token (`aadToken`), indem Sie eine HTTP-Anforderung senden, die die folgenden Eigenschaften hat:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Methode:** `GET`
    - **Body-Inhalt (Formulardaten):**

        | Schlüssel           | Wert                                            |
        | ------------- | -------------------------------------------------|
        | client_id     | ${aadAppId}                                      |
        | client_secret | ${aadAppSecret}                                  |
        | grant_type    | client_credentials                               |
        | Bereich         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    Sie sollten als Antwort ein Azure AD-Token (`aadToken`) erhalten. Es sollte dem folgenden Beispiel ähneln.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Formulieren Sie eine Anfrage in JavaScript Object Notation (JSON), die dem folgenden Beispiel ähnelt.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Beachten Sie die folgenden Punkte:

    - Der `client_assertion`-Wert muss das Azure AD-Token (`aadToken`) sein, das Sie im vorherigen Schritt erhalten haben.
    - Der Wert von `context` muss die Lifecycle Services Umgebungs-ID sein, unter der Sie das Add-In bereitstellen möchten.
    - Legen Sie alle anderen Werte fest, wie im Beispiel gezeigt.

1. Rufen Sie einen Zugriffstoken (`access_token`) ab, indem Sie eine HTTP-Anforderung mit den folgenden Eigenschaften senden:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Methode:** `POST`
    - **HTTP-Header:** Geben Sie die API-Version an. (Der Schlüssel ist `Api-Version`, und der Wert ist `1.0`.)
    - **Body-Inhalt:** Fügen Sie die JSON-Anfrage ein, die Sie im vorherigen Schritt erstellt haben.

    Sie sollten als Antwort ein Zugriffs-Token (`access_token`) erhalten. Sie müssen dieses Token als Träger-Token verwenden, um die Inventory Visibility API aufzurufen. Hier ist ein Beispiel.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Wenn Sie die *Postman*-Anforderungssammlung zum Aufrufen öffentlicher APIs für die Inventarsichtbarkeit anfordern, müssen Sie für jede Anforderung ein Bearertoken hinzufügen. Um Ihren Bearertoken zu finden, wählen Sie die Registerkarte **Autorisierung** unter der Anforderungs-URL und den **Bearertoken**-Typ aus, und kopieren Sie das Zugriffstoken, das im letzten Schritt abgerufen wurde. In späteren Abschnitten dieses Artikels werden `$access_token` verwendet, um das Token darzustellen, das im letzten Schritt abgerufen wurde.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Erstellen von Ereignissen bei Lagerbestandsänderungen

Es gibt zwei APIs zum Erstellen von Ereignissen zur Änderung des Lagerbestands:

- Erzeugen eines Datensatzes: `/api/environment/{environmentId}/onhand`
- Mehrere Datensätze erstellen: `/api/environment/{environmentId}/onhand/bulk`

Die folgende Tabelle fasst die Bedeutung der einzelnen Felder im JSON-Körper zusammen.

| Feldkennung | Description |
|---|---|
| `id` | Eine eindeutige ID für das spezifische Änderungsereignis. Bei einer erneuten Übermittlung aufgrund eines Systemfehlers wird diese ID verwendet, um sicherzustellen, dass dasselbe Ereignis im System nicht doppelt gezählt wird. |
| `organizationId` | Die Kennung der Organisation, die mit dem Ereignis verknüpft ist. Dieser Wert wird einer Organisations- oder Datenbereichskennung im Supply Chain Management zugeordnet. |
| `productId` | Die Kennung des Produkts. |
| `quantities` | Die Menge, um die der Lagerbestand geändert werden muss. Wenn z.B. 10 neue Bücher zu einem Regal hinzugefügt werden, ist dieser Wert `quantities:{ shelf:{ received: 10 }}`. Wenn drei Bücher aus dem Regal entfernt oder verkauft werden, ist dieser Wert `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Die Datenquelle der Dimensionen, die im Buchungsänderungsereignis und in der Abfrage verwendet werden. Wenn Sie die Datenquelle angeben, können Sie die benutzerdefinierten Dimensionen aus der angegebenen Datenquelle verwenden. Inventory Visibility kann die Dimensionskonfiguration verwenden, um die angepassten Dimensionen den allgemeinen Standarddimensionen zuzuordnen. Wenn kein `dimensionDataSource`-Wert angegeben wird, können Sie nur die allgemeinen [Basisdimensionen](inventory-visibility-configuration.md#data-source-configuration-dimension) in Ihren Abfragen verwenden. |
| `dimensions` | Ein dynamisches Schlüssel-Werte-Paar. Die Werte werden einigen der Dimensionen im Supply Chain Management zugeordnet. Sie können jedoch auch angepasste Dimensionen hinzufügen (z. B. *Quelle*), um anzugeben, ob das Ereignis aus dem Supply Chain Management oder einem externen System stammt. |

> [!NOTE]
> Die Parameter `siteId` und `locationId` erstellen die [Partitionskonfiguration](inventory-visibility-configuration.md#partition-configuration). Daher müssen Sie sie in Dimensionen angeben, wenn Sie Ereignisse zur Änderung des Lagerbestands erstellen, Lagerbestandsmengen festlegen oder überschreiben oder Reservierungsereignisse erstellen.

Die folgenden Unterabschnitte enthalten Beispiele, die zeigen, wie diese APIs verwendet werden.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Ein Ereignis zur Änderung des Lagerbestands erstellen

Diese API erstellt ein einzelnes Ereignis zur Änderung des Lagerbestands.

```txt
Path:
    /api/environment/{environmentId}/onhand
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
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Das folgende Beispiel zeigt einen Beispielkörperinhalt. In diesem Beispiel verfügt das Unternehmen über ein Point-of-Sale-System (POS), das Transaktionen im Geschäft und damit Bestandsänderungen verarbeitet. Der Kunde hat ein rotes T-Shirt in Ihrem Geschäft zurückgegeben. Um die Änderung widerzuspiegeln, buchen Sie ein einziges Änderungsereignis für das Produkt *T-Shirt*. Dieses Ereignis erhöht die Menge des Produkts *T-Shirt* um 1.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Das folgende Beispiel zeigt einen Beispielkörperinhalt ohne `dimensionDataSource`. In diesem Fall sind `dimensions` die [Basisdimensionen](inventory-visibility-configuration.md#data-source-configuration-dimension). Wenn `dimensionDataSource` festgelegt ist, können `dimensions` entweder die Datenquellendimensionen oder die Basisdimensionen sein.

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Erstellen Sie mehrere Änderungsereignisse

Diese API kann Änderungsereignisse erstellen, genau wie die [Single-Event-API](#create-one-onhand-change-event) kann. Der einzige Unterschied besteht darin, dass diese API mehrere Datensätze gleichzeitig erstellen kann. Deshalb, unterscheiden sich die `Path` und `Body` Werte. Bei dieser API liefert `Body` ein Array von Datensätzen. Die maximale Anzahl an Datensätzen ist 512. Daher kann die Bulk-API für Lagerbestandsänderungen bis zu 512 Änderungsereignisse gleichzeitig unterstützen. 

Ein POS-Gerät in einem Einzelhandelsgeschäft verarbeitete beispielsweise die folgenden zwei Transaktionen:

- Eine Rücksendung von einem roten T-Shirt
- Eine Verkaufstransaktion von drei schwarzen T-Shirts

In diesem Fall können Sie beide Bestandsaktualisierungen in einen API-Aufruf einbeziehen.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Lagerbestände festlegen/überschreiben

Die *Setzen von Lagerbeständen* API setzt die aktuellen Daten für das angegebene Produkt außer Kraft. Diese Funktion wird normalerweise verwendet, um Bestandszählungsaktualisierungen durchzuführen. Beispielsweise könnte ein Geschäft während seiner täglichen Bestandszählung feststellen, dass der tatsächliche Lagerbestand für ein rotes T-Shirt 100 beträgt. Daher muss die POS-Eingangsmenge unabhängig von der vorherigen Menge auf 100 aktualisiert werden. Sie können diese API verwenden, um den vorhandenen Wert zu überschreiben.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Das folgende Beispiel zeigt einen Beispielkörperinhalt. Das Verhalten dieser API unterscheidet sich vom Verhalten der APIs, die im Abschnitt [Erstellen von Ereignissen zur Änderung des Lagerbestands](#create-onhand-change-event) weiter oben in diesem Artikel beschrieben sind. In diesem Beispiel wird die Menge des Produkts *T-Shirt* auf 1 festgelegt.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Erstellen von Reservierungsereignissen

Um die *Reserve*-API zu verwenden, müssen Sie die Funktion „Reservierung“ öffnen und die Konfiguration der Reservierung abschließen. Weitere Informationen (einschließlich eines Datenflusses und eines Beispielszenarios) finden Sie unter [Reservierungskonfiguration (optional)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Erstellen Sie ein Ereignis für die Reservierung

Eine Reservierung kann für verschiedene Datenquelleneinstellungen vorgenommen werden. Um diese Art der Reservierung zu konfigurieren, geben Sie zuerst die Datenquelle im `dimensionDataSource`-Parameter an. Geben Sie dann im `dimensions`-Parameter die Dimensionen gemäß den Dimensionseinstellungen in der Zieldatenquelle an.

Wenn Sie die Reservierungs-API aufrufen, können Sie die Reservierungsvalidierung steuern, indem Sie den booleschen `ifCheckAvailForReserv`-Parameter im Anforderungstext angeben. Der Wert `True` bedeutet, dass die Validierung erforderlich ist, während der Wert `False` bedeutet, dass die Validierung nicht erforderlich ist. Der Standardwert ist `True`.

Wenn Sie eine Reservierung umkehren oder die Reservierung bestimmter Bestandsmengen aufheben möchten, setzen Sie die Menge auf einen negativen Wert und legen Sie den `ifCheckAvailForReserv`-Parameter auf `False` fest, um die Validierung zu überprüfen. Es gibt auch eine dedizierte API zum Aufheben der Reservierung, um dasselbe zu tun. Der Unterschied besteht nur in der Art und Weise, wie die beiden APIs aufgerufen werden. Es ist einfacher, ein bestimmtes Reservierungsereignis mithilfe der `reservationId` mit der *Reservierung aufheben* API umzukehren. Weitere Informationen finden Sie im Abschnitt [Ein Reservierungsereignis aufheben](#reverse-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
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
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Das folgende Beispiel zeigt einen Beispielkörperinhalt.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Das folgende Beispiel zeigt eine erfolgreiche Antwort.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Erstellen Sie mehrere Reservierungsereignisse

Diese API ist eine Massenversion der [Einzelereignis-API](#create-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
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
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>Reservierungsereignisse umkehren

Die *Reservierung aufheben* API dient als Umkehrvorgang für [*Reservierungsereignisse*](#create-reservation-events). Sie bietet eine Möglichkeit, ein durch `reservationId` spezifiziertes Reservierungsereignis umzukehren oder die Reservierungsmenge zu verringern.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Ein Reservierungsereignis umkehren

Wenn eine Reservierung erstellt wird, wird in den Antworttext eine `reservationId` aufgenommen. Sie müssen dieselbe `reservationId` bereitstellen, um die Reservierung zu stornieren, und dieselbe `organizationId` und `dimensions` einfügen, die für den Aufruf der Reservierungs-API verwendet wird. Geben Sie abschließend einen Wert für `OffsetQty` an, der die Anzahl der Artikel darstellt, die aus der vorherigen Reservierung freigegeben werden sollen. Je nach der angegebenen `OffsetQty`, kann eine Reservierung vollständig oder teilweise umgekehrt werden. Wenn zum Beispiel *100* Einheiten von Artikeln reserviert wurden, können Sie `OffsetQty: 10` auf *10* der ursprünglich reservierten Menge festlegen.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Der folgende Code zeigt einen Beispiel für einen Antwortinhalt.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Der folgende Code zeigt einen Beispiel für einen erfolgreichen Antworttext.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Wenn im Antworttext `OffsetQty` kleiner oder gleich der Reservierungsmenge ist, ist der `processingStatus` auf *Erfolg* und die `totalInvalidOffsetQtyByReservId` auf *0* gestellt.
>
> Wenn die `OffsetQty` größer als die reservierte Menge ist, lautet der `processingStatus` *partialSuccess* und `totalInvalidOffsetQtyByReservId` zeigt die Differenz zwischen `OffsetQty` und der reservierten Menge an.
>
>Wenn die Reservierung beispielsweise eine Menge von *10* und `OffsetQty` einen Wert von *12* hat, ist `totalInvalidOffsetQtyByReservId` *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Mehrere Reservierungsereignisse umkehren

Diese API ist eine Massenversion der [Einzelereignis-API](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Lagerbestand abfragen

Verwenden Sie die *Abfrage des Lagerbestands* API, um aktuelle Daten zum Lagerbestand Ihrer Produkte abzurufen. Sie können diese API immer dann verwenden, wenn Sie den Lagerbestand kennen müssen, z. B. wenn Sie die Produktlagerbestände auf Ihrer E-Commerce-Website überprüfen möchten oder wenn Sie die Produktverfügbarkeit in verschiedenen Regionen oder in nahe gelegenen Geschäften und Lagern überprüfen möchten. Die API unterstützt derzeit die Abfrage von bis zu 5000 einzelnen Elementen nach dem `productID`-Wert. In jeder Abfrage können auch mehrere `siteID`- und `locationID`-Werte angegeben werden. Der maximale Grenzwert bestimmt sich durch die folgende Gleichung:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Abfrage mit Hilfe der Post-Methode

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

Im Hauptteil dieser Anforderung ist `dimensionDataSource` immer noch ein optionaler Parameter. Wenn er nicht festgelegt ist, wird `filters` als *Basisdimensionen* behandelt. Es gibt vier Pflichtfelder für `filters`: `organizationId`, `productId`, `siteId` und `locationId`.

- `organizationId` sollte nur einen Wert enthalten, ist jedoch nach wie vor ein Array.
- `productId` könnte einen oder mehrere Werte enthalten. Wenn es sich um ein leeres Array handelt, werden alle Produkte zurückgegeben.
- `siteId` und `locationId` werden in der Bestandsanzeige für die Partitionierung verwendet. Sie in einer *Lagerbestand abfragen*-Anforderung mehr als einen Wert für `siteId` und `locationId` angeben. In der aktuellen Version müssen Sie die beiden Werte `siteId` und `locationId` angeben.

Sie sollten den `groupByValues`-Parameter verwenden, um Ihrer Konfiguration für die Indizierung zu folgen. Weitere Informationen finden Sie unter [Produktindex-Hierarchie-Konfiguration](./inventory-visibility-configuration.md#index-configuration).

Der `returnNegative`-Parameter steuert, ob die Ergebnisse negative Einträge enthalten.

> [!NOTE]
> Wenn Sie die Funktionen Lagerbestand und ATP (Available-to-Promise) aktiviert haben, kann Ihre Abfrage auch den booleschen Parameter `QueryATP` enthalten, der steuert, ob die Abfrageergebnisse ATP-Informationen enthalten. Weitere Informationen und Beispiele finden Sie unter [Inventory Visibility Lagerbestands-Änderungstermine und verfügbares Versprechen](inventory-visibility-available-to-promise.md).

Das folgende Beispiel zeigt einen Beispielkörperinhalt. Es zeigt, dass Sie den verfügbaren Bestand von mehreren Standorten (Lagern) aus abfragen können.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Das folgende Beispiel zeigt, wie Sie alle Produkte an einem bestimmten Standort und Lagerplatz abfragen.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Abfrage mit Hilfe der get-Methode

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

Hier ist eine Beispiel-GET-URL. Diese get-Anfrage ist genau die gleiche wie das post-Beispiel, das zuvor bereitgestellt wurde.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>Exakte Bestandsabfrage

Exakt verfügbare Abfragen ähneln normalen verfügbaren Abfragen, aber sie ermöglichen es Ihnen, eine Zuordnungshierarchie zwischen einem Standort und einem Standort anzugeben. Sie haben zum Beispiel die folgenden zwei Websites:

- Standort 1, der Standort A zugeordnet ist
- Standort 2, der Standort B zugeordnet ist

Für eine regelmäßige Verfügbarkeitsabfrage, wenn Sie `"siteId": ["1","2"]` und `"locationId": ["A","B"]` angeben, fragt Bestandsanzeige automatisch das Ergebnis für die folgenden Sites und Standorte ab:

- Standort 1, Lagerplatz A
- Standort 1, Lagerplatz B
- Standort 2, Lagerplatz A
- Standort 2, Lagerplatz B

Wie Sie sehen, erkennt die normale Verfügbarkeitsabfrage nicht, dass Standort A nur an Standort 1 und Standort B nur an Standort 2 vorhanden ist. Daher macht es redundante Abfragen. Um diese hierarchische Zuordnung zu berücksichtigen, können Sie eine verfügbare exakte Abfrage verwenden und die Standortzuordnungen im Abfragetext angeben. In diesem Fall werden Sie nur Ergebnisse für Website 1, Standort A und Website 2, Standort B abfragen und erhalten.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>Exakte Abfrage unter Verwendung der POST-Methode

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Im Body-Teil dieser Anfrage ist `dimensionDataSource` ein optionaler Parameter. Wenn er nicht festgelegt ist, wird `dimensions` in `filters` als *Basis Dimensionen* behandelt. Es gibt vier Pflichtfelder für `filters`: `organizationId`, `productId`, `dimensions` und `values`.

- `organizationId` sollte nur einen Wert enthalten, ist jedoch nach wie vor ein Array.
- `productId` könnte einen oder mehrere Werte enthalten. Wenn es sich um ein leeres Array handelt, werden alle Produkte zurückgegeben.
- In dem Array `dimensions` sind `siteId` und `locationId` erforderlich, können aber mit anderen Elementen in beliebiger Reihenfolge erscheinen.
- `values` kann ein oder mehrere unterschiedliche Tupel von Werten enthalten, die `dimensions` entsprechen.

Die `dimensions` in `filters` wird automatisch zu `groupByValues` hinzugefügt.

Der `returnNegative`-Parameter steuert, ob die Ergebnisse negative Einträge enthalten.

Das folgende Beispiel zeigt einen Beispielkörperinhalt.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Das folgende Beispiel zeigt, wie Sie alle Produkte in mehreren Betrieben und Standorten abfragen können.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Verfügbar für Zusage

Sie können Inventory Visibility so festlegen, dass Sie zukünftige Änderungen des Lagerbestands planen und ATP-Mengen berechnen können. ATP ist die Menge eines Elements, die verfügbar ist und einem Kunden in der nächsten Periode zugesagt werden kann. Die Verwendung der ATP-Berechnung kann Ihre Funktionalitäten bei der Auftragsabwicklung erheblich steigern. Informationen darüber, wie Sie diese Funktion aktivieren und wie Sie mit Inventory Visibility über die API interagieren können, nachdem die Funktion aktiviert wurde, finden Sie unter [Inventory Visibility Lagerbestand ändert Zeitpläne und ist für Versprechen verfügbar](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Zuweisung

Zuweisungsbezogene APIs befinden sich in [Zuweisung der Bestandsichtbarkeit](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
