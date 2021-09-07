---
title: Bestandstransparenzreservierungen
description: In diesem Thema wird beschrieben, wie Sie die Funktion "Reservierungen" festlegen, um mit Inventory Visibility Reservierungen zu erstellen, Reservierungen zu verbrauchen und/oder die Reservierung bestimmter Bestandsmengen aufzuheben.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345148"
---
# <a name="inventory-visibility-reservations"></a>Bestandstransparenzreservierungen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In diesem Thema wird beschrieben, wie Sie die Funktion "Reservierungen" festlegen, um mit Inventory Visibility Reservierungen zu erstellen, Reservierungen zu verbrauchen und/oder die Reservierung bestimmter Bestandsmengen aufzuheben.

Reservierungen markieren eine Bestandsmenge, die in der Zukunft verbraucht werden soll. Wenn Sie eine Reservierung erstellen, hindert das System andere Aufträge daran, die reservierten Waren zu reservieren oder zu verbrauchen, bis die Reservierung entweder verbraucht oder die Reservierung aufgehoben ist. Reservierungen werden mithilfe von API-Aufrufen an den Dienst Inventory Visibility erstellt, verbraucht und storniert.

Optional können Sie Microsoft Dynamics 365 Supply Chain Management (und andere Systeme von Drittanbietern) so festlegen, dass die reservierte Menge automatisch durch die Verwendung von Inventory Visibility ausgeglichen wird. Die verrechnete Menge wird aus den Datensätzen der Reservierung in Inventory Visibility gelöscht.

Wenn Sie die Reservierungsfunktion einschalten, ist Supply Chain Management automatisch bereit, Reservierungen zu verrechnen, die über Inventory Visibility vorgenommen wurden.

> [!NOTE]
> Die Offset-Funktionalität erfordert Supply Chain Management Version 10.0.22 oder höher. Wenn Sie Reservierungen mit Inventory Visibility verwenden möchten, empfehlen wir Ihnen zu warten, bis Sie Supply Chain Management auf Version 10.0.22 oder höher aktualisiert haben.

## <a name="turn-on-the-reservation-feature"></a>Einschalten der Reservierungsfunktion

Um die Funktion "Reservierung" einzuschalten, gehen Sie folgendermaßen vor.

1. Öffnen Sie in Power Apps **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Schalten Sie auf der Registerkarte **Funktionsverwaltung** die Funktion *OnHandReservierung* ein.
1. Melden Sie sich im Supply Chain Management an.
1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Bestandssichtbarkeit-Integrationsparameter**.
1. Legen Sie unter **Reservierungsversatz** die Option **Reservierungsversatz aktivieren** auf *Ja* fest.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Verwenden Sie die Funktion "Reservierung" in Inventory Visibility

Wenn Sie die Reservierungs-API aufrufen, markiert das System die Reservierung der angegebenen Waren und Mengen. Sie müssen eine Reservierungshierarchie definieren und Anfragen buchen, die dieser Reservierungshierarchie entsprechen. Die Reservierungen können dann durch direkten Aufruf der Reservierungs-APIs vorgenommen werden.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurieren Sie die Reservierungshierarchie

Die Reservierungshierarchie beschreibt die Sequenz von Dimensionen, die bei der Reservierung angegeben werden müssen. Sie funktioniert genauso wie die Indexhierarchie für Lagerbestandsabfragen.

Die Reservierungshierarchie kann sich von der Indexhierarchie unterscheiden. Diese Unabhängigkeit ermöglicht die Implementierung einer Kategorieverwaltung, bei der Benutzer die Dimensionen in Details aufschlüsseln können, um die Anforderungen für genauere Reservierungen zu spezifizieren.

Um eine Soft-Reservierungshierarchie in Power Apps zu konfigurieren, öffnen Sie die Seite **Konfiguration** und legen dann auf der Registerkarte **Soft-Reservierungszuordnung** die Reservierungshierarchie fest, indem Sie Dimensionen und ihre Hierarchieebenen hinzufügen und/oder ändern.

### <a name="call-the-reservation-api"></a>Aufrufen der Reservierungs-API

Reservierungen werden im Inventory Visibility-Dienst vorgenommen, indem Sie eine POST-Anfrage an die URL des Dienstes senden, z. B. `/api/environment/{environment-ID}/onhand/reserve`.

Für eine Reservierung muss der Anfragekörper eine Organisations-ID, eine Produkt-ID, reservierte Mengen und Dimensionen enthalten. Die Anfrage generiert eine eindeutige Reservierungs-ID für jeden Reservierungsdatensatz. Der Reservierungsdatensatz enthält die eindeutige Kombination aus der Produkt-ID und den Dimensionen.

Hier ist ein Beispiel für den Anforderungskörper, als Referenz.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Offset-Reservierungen im Supply Chain Management

Für Bestandstransaktionsstatus, die einen bestimmten Reservierungs-Offset-Modifikator enthalten, wird die Transaktion den entsprechenden Reservierungsdatensatz ausgleichen, wenn alle folgenden Bedingungen erfüllt sind:

- Die Reservierungs-ID der Bestandstransaktion stimmt mit der Reservierungs-ID des Reservierungsdatensatzes im Inventory Visibility-Dienst überein.
- Die Dimensionen der Bestandstransaktion sind identisch mit den Dimensionen des Reservierungsdatensatzes im Inventory Visibility-Dienst.
- Änderungen im Status der Bestandstransaktion lösen Auslösungen für Reservierungen aus, wenn der Status der Bestandstransaktion die Tatsache widerspiegelt, dass ein Bestellvorgang abgeschlossen oder übersprungen wurde.

Die Offset-Menge folgt der Bestandsmenge, die auf Bestandstransaktionen angegeben ist. Der Offset wird nicht wirksam, wenn keine reservierte Menge im Inventory Visibility-Dienst verbleibt.

> [!NOTE]
> Die Offset-Funktionalität ist ab der Version 10.0.22 verfügbar

### <a name="set-up-the-reserve-offset-modifier"></a>Festlegen des Reserve-Offset-Modifikators

Der Reserve-Offset-Modifikator bestimmt die Stufe der Auftragsverarbeitung, die Auslöser für Offsets ist. Die Stufe wird durch den Status der Bestandstransaktion des Auftrags nachverfolgt. Um den Reserve-Offset-Modifikator festzulegen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Inventory Visibility-Integrationsparameter \> Reservierungsoffset**.
1. Legen Sie das Feld **Reserveoffset-Modifikator** auf einen der folgenden Werte fest:

    - *Bei Bestellung* - Für den Status *Bei Transaktion* sendet eine Bestellung eine Offset-Anforderung, wenn sie erstellt wird.
    - *Reservieren* - Für den Status *Bestellte Transaktion reservieren* sendet eine Bestellung eine Offset-Anfrage, wenn sie reserviert, kommissioniert, mit Lieferschein gebucht oder in Rechnung gestellt wird. Die Anfrage wird nur einmal ausgelöst, und zwar für den ersten Schritt, wenn der genannte Vorgang stattfindet.

### <a name="set-up-reservation-ids"></a>Reservierungs-IDs festlegen

Die Reservierungs-ID kennzeichnet einen Reservierungsdatensatz in Inventory Visibility auf eindeutige Weise. Im Supply Chain Management setzen Benutzer Reservierungen auf Auftragszeilen, um den Offset für den entsprechenden Datensatz der Reservierung zu markieren.

Um Reservierungs-IDs im Supply Chain Management festzulegen, gehen Sie wie folgt vor.

1. Öffnen Sie einen Verkaufsauftrag (z. B. auf der Seite **Alle Verkaufsaufträge**).
1. Wählen Sie auf dem Inforegister **Verkaufsauftragszeilen** eine Auftragszeile aus.
1. Wählen Sie auf der Registerkarte **Verkaufsauftragszeilen** Inforegister **Zeile aktualisieren \> Bestand \> Bestandssichtbarkeits-Integration**.
1. Geben Sie die entsprechenden Reservierungs-IDs ein.

Die Änderung des Bestandsstatus stimmt mit der Einrichtung des Offset-Modifikators überein.
