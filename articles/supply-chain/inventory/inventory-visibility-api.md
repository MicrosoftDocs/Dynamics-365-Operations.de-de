---
title: Öffentliche Inventartransparenz-APIs
description: Dieses Thema beschreibt die öffentlichen APIs, die von Inventory Visibility bereitgestellt werden.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f74bb4bd4ed66520c04261bd9f82faad7775817e
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062110"
---
# <a name="inventory-visibility-public-apis"></a>Öffentliche Inventartransparenz-APIs

[!include [banner](../includes/banner.md)]


Dieses Thema beschreibt die öffentlichen APIs, die von Inventory Visibility bereitgestellt werden.

Die öffentliche REST-API des Bestandssichtbarkeit-Add-Ins stellt mehrere spezifische Endpunkte für die Integration bereit. Es werden vier Hauptinteraktionstypen unterstützt:

- Verbuchung von Änderungen des Lagerbestands aus einem externen System in das Add-In
- Festlegen oder Außerkraftsetzen von Lagerbestandsmengen im Add-In von einem externen System
- Buchen von Reservierungsereignissen an das Add-In von einem externen System
- Abfrage aktueller Lagerbestände von einem externen System

In der folgenden Tabelle sind die derzeit verfügbaren APIs aufgeführt:

| Pfad | Methode | Beschreibung |
|---|---|---|
| /api/environment/{environmentId}/onhand | Buchen | [Ein Ereignis zur Änderung des Lagerbestands erstellen](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Buchen | [Mehrere Änderungsereignisse erstellen](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Buchen | [Festlegen/Überschreiben von Lagerbeständen](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Buchen | [Ein Ereignis für eine Reservierung erstellen](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Buchen | [Mehrere Reservierungsereignisse erstellen](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | Buchen | [Abfrage mit Hilfe der POST-Methode](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Abrufen | [Abfrage mit Hilfe der get-Methode](#query-with-get-method) |

Microsoft hat eine standardmäßige *Postman* Abfrage-Sammlung bereitgestellt. Sie können diese Sammlung in Ihre *Postman*-Software importieren, indem Sie den folgenden gemeinsamen Link verwenden: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

> [!NOTE]
> Der Teil {environmentId} des Pfades ist die Umgebungs-ID in Microsoft Dynamics Lifecycle Services (LCS).
> 
> Die Bulk-API kann maximal 512 Datensätze für jede Anfrage zurückgeben.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Finden Sie den Endpunkt entsprechend Ihrer Lifecycle Services Umgebung

Der Microservice von Inventory Visibility wird auf Microsoft Azure Service Fabric bereitgestellt, und zwar in mehreren Regionen und Gegenden. Es gibt derzeit keinen zentralen Endpunkt, der Ihre Anfrage automatisch an die entsprechende Geographie und Region weiterleiten kann. Daher müssen Sie die Informationen nach folgendem Muster zu einer URL zusammenstellen:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Die Kurzbezeichnung der Region finden Sie in der Microsoft Dynamics Lifecycle Services (LCS) Umgebung. In der folgenden Tabelle sind die Regionen aufgeführt, die derzeit verfügbar sind.

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
| Brasilien, Süden        | sbr               |
| USA, Süden-Mitte    | scus              |

Die Inselnummer gibt an, wo Ihre LCS Umgebung auf Service Fabric bereitgestellt ist. Es gibt derzeit keine Möglichkeit, diese Informationen von der Benutzerseite aus zu erhalten.

Microsoft hat eine Benutzeroberfläche (UI) in Power Apps eingebaut, so dass Sie den kompletten Endpunkt des Microservices erhalten können. Weitere Informationen finden Sie unter [Finden Sie den Dienst-Endpunkt](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Authentifizierung

Das Sicherheits-Token der Plattform wird für den Aufruf der öffentlichen API von Inventory Visibility verwendet. Daher müssen Sie ein _Azure Active Directory (Azure AD) Token_ generieren, indem Sie Ihre Azure AD Anwendung verwenden. Sie müssen dann das Azure AD-Token verwenden, um das _Zugriffstoken_ vom Sicherheitsdienst zu erhalten.

Microsoft stellt eine standardmäßige *Postman*-Token-Abfragesammlung bereit. Sie können diese Sammlung in Ihre *Postman*-Software importieren, indem Sie den folgenden gemeinsamen Link verwenden: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Gehen Sie folgendermaßen vor, um ein Sicherheitsdienst-Token zu erhalten.

1. Melden Sie sich am Azure-Portal an und suchen Sie dort die `clientId`- und `clientSecret`-Werte für Ihre Dynamics 365 Supply Chain Management-App.
1. Holen Sie ein Azure AD-Token (`aadToken`), indem Sie eine HTTP-Anforderung senden, die die folgenden Eigenschaften hat:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Methode:** `GET`
   - **Body-Inhalt (Formulardaten):**

     | Schlüssel           | Wert                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | resource      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   Sie sollten als Antwort ein Azure AD-Token (`aadToken`) erhalten. Es sollte dem folgenden Beispiel ähneln.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   Beachten Sie die folgenden Punkte:

   - Der `client_assertion`-Wert muss das Azure AD-Token (`aadToken`) sein, das Sie im vorherigen Schritt erhalten haben.
   - Der Wert von `context` muss die LCS-Umgebungs-ID sein, unter der Sie das Add-In bereitstellen möchten.
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
> Wenn Sie die *Postman*-Anforderungssammlung zum Aufrufen öffentlicher APIs für die Inventarsichtbarkeit anfordern, müssen Sie für jede Anforderung ein Bearertoken hinzufügen. Um Ihren Bearertoken zu finden, wählen Sie die Registerkarte **Autorisierung** unter der Anforderungs-URL und den **Bearertoken**-Typ aus, und kopieren Sie das Zugriffstoken, das im letzten Schritt abgerufen wurde. In späteren Abschnitten dieses Themas werden `$access_token` verwendet, um das Token darzustellen, das im letzten Schritt abgerufen wurde.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Erstellen von Ereignissen bei Lagerbestandsänderungen

Es gibt zwei APIs zum Erstellen von Ereignissen zur Änderung des Lagerbestands:

- Erzeugen eines Datensatzes: `/api/environment/{environmentId}/onhand`
- Mehrere Datensätze erstellen: `/api/environment/{environmentId}/onhand/bulk`

Die folgende Tabelle fasst die Bedeutung der einzelnen Felder im JSON-Körper zusammen.

| Feldkennung | Beschreibung |
|---|---|
| `id` | Eine eindeutige ID für das spezifische Änderungsereignis. Diese ID wird verwendet, um sicherzustellen, dass, wenn die Kommunikation mit dem Dienst während der Übermittlung fehlschlägt, dasselbe Ereignis im System nicht doppelt gezählt wird, wenn es erneut übermittelt wird. |
| `organizationId` | Die Kennung der Organisation, die mit dem Ereignis verknüpft ist. Dieser Wert wird einer Organisations- oder Datenbereichskennung im Supply Chain Management zugeordnet. |
| `productId` | Die Kennung des Produkts. |
| `quantities` | Die Menge, um die der Lagerbestand geändert werden muss. Wenn z.B. 10 neue Bücher zu einem Regal hinzugefügt werden, ist dieser Wert `quantities:{ shelf:{ received: 10 }}`. Wenn drei Bücher aus dem Regal entfernt oder verkauft werden, ist dieser Wert `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Die Datenquelle der Dimensionen, die im Buchungsänderungsereignis und in der Abfrage verwendet werden. Wenn Sie die Datenquelle angeben, können Sie die benutzerdefinierten Dimensionen aus der angegebenen Datenquelle verwenden. Inventory Visibility kann die Dimensionskonfiguration verwenden, um die angepassten Dimensionen den allgemeinen Standarddimensionen zuzuordnen. Wenn kein `dimensionDataSource`-Wert angegeben wird, können Sie nur die allgemeinen [Basisdimensionen](inventory-visibility-configuration.md#data-source-configuration-dimension) in Ihren Abfragen verwenden. |
| `dimensions` | Ein dynamisches Schlüssel-Werte-Paar. Die Werte werden einigen der Dimensionen im Supply Chain Management zugeordnet. Sie können jedoch auch angepasste Dimensionen hinzufügen (z. B. _Quelle_), um anzugeben, ob das Ereignis aus dem Supply Chain Management oder einem externen System stammt. |

> [!NOTE]
> Die Parameter `SiteId` und `LocationId` erstellen die [Partitionskonfiguration](inventory-visibility-configuration.md#partition-configuration). Daher müssen Sie sie in Dimensionen angeben, wenn Sie Ereignisse zur Änderung des Lagerbestands erstellen, Lagerbestandsmengen festlegen oder überschreiben oder Reservierungsereignisse erstellen.

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

Das folgende Beispiel zeigt einen Beispielkörperinhalt. In diesem Beispiel buchen Sie ein Änderungsereignis für das Produkt *T-Shirt*. Dieses Ereignis kommt vom Point of Sale (POS)-System, und der Debitor hat ein rotes T-Shirt an Ihr Geschäft zurückgegeben. Dieses Ereignis erhöht die Menge des Produkts *T-Shirt* um 1.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
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
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Erstellen Sie mehrere Änderungsereignisse

Diese API kann mehrere Datensätze gleichzeitig erstellen. Die einzigen Unterschiede zwischen dieser API und der [Einzelereignis-API](#create-one-onhand-change-event) sind die Werte `Path` und `Body`. Bei dieser API liefert `Body` ein Array von Datensätzen. Die maximale Anzahl von Datensätzen beträgt 512, was bedeutet, dass die Bulk-API für vorhandene Änderungen bis zu 512 Änderungsereignisse gleichzeitig unterstützen kann.

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Lagerbestände festlegen/überschreiben

Die _Setzen von Lagerbeständen_ API setzt die aktuellen Daten für das angegebene Produkt außer Kraft.

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

Das folgende Beispiel zeigt einen Beispielkörperinhalt. Das Verhalten dieser API unterscheidet sich vom Verhalten der APIs, die im Abschnitt [Erstellen von Ereignissen zur Änderung des Lagerbestands](#create-onhand-change-event) weiter oben in diesem Thema beschrieben sind. In diesem Beispiel wird die Menge des Produkts *T-Shirt* auf 1 festgelegt.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Erstellen von Reservierungsereignissen

Um die *Reserve*-API zu verwenden, müssen Sie die Funktion "Reservierung" öffnen und die Konfiguration der Reservierung abschließen. Weitere Informationen finden Sie unter [Reservierungskonfiguration (optional)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Erstellen Sie ein Ereignis für die Reservierung

Eine Reservierung kann für verschiedene Datenquelleneinstellungen vorgenommen werden. Um diese Art der Reservierung zu konfigurieren, geben Sie zuerst die Datenquelle im `dimensionDataSource`-Parameter an. Geben Sie dann im `dimensions`-Parameter die Dimensionen gemäß den Dimensionseinstellungen in der Zieldatenquelle an.

Wenn Sie die Reservierungs-API aufrufen, können Sie die Reservierungsvalidierung steuern, indem Sie den booleschen `ifCheckAvailForReserv`-Parameter im Anforderungstext angeben. Der Wert `True` bedeutet, dass die Validierung erforderlich ist, während der Wert `False` bedeutet, dass die Validierung nicht erforderlich ist. Der Standardwert ist `True`.

Wenn Sie eine Reservierung stornieren oder die Reservierung bestimmter Bestandsmengen aufheben möchten, setzen Sie die Menge auf einen negativen Wert und legen Sie den `ifCheckAvailForReserv`-Parameter auf `False` fest, um die Validierung zu überspringen.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Erstellen Sie mehrere Reservierungsereignisse

Diese API ist eine Massenversion der [Einzelereignis-API](#create-one-reservation-event).

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

## <a name="query-on-hand"></a>Lagerbestand abfragen

Verwenden Sie die _Abfrage des Lagerbestands_ API, um aktuelle Daten zum Lagerbestand Ihrer Produkte abzurufen. Die API unterstützt derzeit die Abfrage von bis zu 100 einzelnen Elementen nach dem `ProductID`-Wert. In jeder Abfrage können auch mehrere `SiteID`- und `LocationID`-Werte angegeben werden. Die Höchstgrenze ist mit `NumOf(SiteID) * NumOf(LocationID) <= 100` definiert.

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
- `productId` kann einen oder mehrere Werte enthalten. Wenn es sich um ein leeres Array handelt, werden alle Produkte zurückgegeben.
- `siteId` und `locationId` werden in der Bestandsanzeige für die Partitionierung verwendet. Sie in einer *Lagerbestand abfragen*-Anforderung mehr als einen Wert für `siteId` und `locationId` angeben. In der aktuellen Version müssen Sie die beiden Werte `siteId` und `locationId` angeben.

Der `groupByValues`-Parameter sollte Ihrer Konfiguration für die Indizierung folgen. Weitere Informationen finden Sie unter [Produktindex-Hierarchie-Konfiguration](./inventory-visibility-configuration.md#index-configuration).

Der `returnNegative`-Parameter steuert, ob die Ergebnisse negative Einträge enthalten.

Das folgende Beispiel zeigt einen Beispielkörperinhalt.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

Die folgenden Beispiele zeigen, wie Sie alle Produkte an einem bestimmten Standort und Lagerplatz abfragen.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
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
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
