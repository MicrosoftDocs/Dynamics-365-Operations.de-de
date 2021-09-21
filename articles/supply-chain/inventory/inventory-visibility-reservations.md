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
ms.openlocfilehash: acc5d5f93f3f625892aac37780a44e221b6eb5ac
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475035"
---
# <a name="inventory-visibility-reservations"></a>Bestandstransparenzreservierungen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In diesem Thema wird beschrieben, wie Sie die Funktion "Reservierungen" festlegen, um mit Inventory Visibility Reservierungen zu erstellen, Reservierungen zu verbrauchen und/oder die Reservierung bestimmter Bestandsmengen aufzuheben.

Reservierungen markieren eine Bestandsmenge, die in der Zukunft verbraucht werden soll. Wenn Sie eine Reservierung erstellen, hindert das System andere Aufträge daran, die reservierten Waren zu reservieren oder zu verbrauchen, bis die Reservierung entweder verbraucht oder die Reservierung aufgehoben ist. Reservierungen werden mithilfe von API-Aufrufen an den Dienst Inventory Visibility erstellt, verbraucht und storniert.

Optional können Sie Microsoft Dynamics 365 Supply Chain Management (und andere Systeme von Drittanbietern) so festlegen, dass die reservierte Menge automatisch durch die Verwendung von Inventory Visibility ausgeglichen wird. Die verrechnete Menge wird aus den Datensätzen der Reservierung in Inventory Visibility gelöscht.

Wenn Sie die Reservierungsfunktion einschalten, ist Supply Chain Management automatisch bereit, Reservierungen zu verrechnen, die über Inventory Visibility vorgenommen wurden.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Einschalten und Einrichten der Reservierungsfunktion

Um die Funktion "Reservierung" einzuschalten, gehen Sie folgendermaßen vor.

1. Melden Sie sich bei Power Apps an und öffnen Sie die **Bestandsanzeige**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Schalten Sie auf der Registerkarte **Funktionsverwaltung** die Funktion *OnHandReservierung* ein.
1. Melden Sie sich im Supply Chain Management an.
1. Gehen Sie zum Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** und aktivieren Sie die Funktion *Integration der Bestandssichtbarkeit mit Reservierungsversatz* (erfordert Version 10.0.22 oder höher).
1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Bestandssichtbarkeit-Integrationsparameter**, öffnen Sie die Registerkarte **Reservierungsversatz** und nehmen Sie die folgenden Einstellungen vor:
    - **Reservierungsversatz aktivieren** – Auf *Ja* festlegen, um diese Funktion zu aktivieren.
    - **Modifikator für Reservierungsversatz** – Wählen Sie den Bestandstransaktionsstatus aus, der Reservierungen verrechnet, die in der Bestandsanzeige vorgenommen wurden. Diese Einstellung legt die Auftragsbearbeitungsstufe fest, die einen Versatz auslöst. Die Stufe wird durch den Status der Bestandstransaktion des Auftrags nachverfolgt. Wählen Sie eine der folgenden Optionen:
        - *Bei Bestellung* - Für den Status *Bei Transaktion* sendet eine Bestellung eine Offset-Anforderung, wenn sie erstellt wird. Die Versatzmenge ist die Menge des erstellten Auftrags.
        - *Reservieren* - Für den Status *Bestellte Transaktion reservieren* sendet eine Bestellung eine Offset-Anfrage, wenn sie reserviert, kommissioniert, mit Lieferschein gebucht oder in Rechnung gestellt wird. Die Anfrage wird nur einmal ausgelöst, und zwar für den ersten Schritt, wenn der genannte Vorgang stattfindet. Die Versatzmenge ist die Menge, um die sich der Bestandstransaktionsstatus von *In Auftrag* zu *Bestellt reserviert* (oder zu einem späteren Status) für die entsprechende Auftragsposition geändert hat.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Verwenden Sie die Funktion "Reservierung" in Inventory Visibility

Wenn Sie die Reservierungs-API aufrufen, markiert das System die Reservierung der angegebenen Waren und Mengen. Sie müssen eine Reservierungshierarchie definieren und Anfragen buchen, die dieser Reservierungshierarchie entsprechen. Die Reservierungen können dann durch direkten Aufruf der Reservierungs-APIs vorgenommen werden.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurieren Sie die Reservierungshierarchie

Die Reservierungshierarchie beschreibt die Sequenz von Dimensionen, die bei der Reservierung angegeben werden müssen. Sie funktioniert genauso wie die Indexhierarchie für Lagerbestandsabfragen.

Die Reservierungshierarchie kann sich von der Indexhierarchie unterscheiden. Diese Unabhängigkeit ermöglicht die Implementierung einer Kategorieverwaltung, bei der Benutzer die Dimensionen in Details aufschlüsseln können, um die Anforderungen für genauere Reservierungen zu spezifizieren.

Um eine Soft-Reservierungshierarchie in Power Apps zu konfigurieren, öffnen Sie die Seite **Konfiguration** und legen dann auf der Registerkarte **Soft-Reservierungshierarchie** die Reservierungshierarchie fest, indem Sie Dimensionen und ihre Hierarchieebenen hinzufügen und/oder ändern.

Die Hierarchie Ihrer Soft-Reservierung sollte `SiteId` und `LocationId` als Komponenten enthalten, da sie die Partitionskonfiguration aufbauen.

Weitere Informationen über die Konfiguration von Reservierungen finden Sie unter [Reservierungskonfiguration](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Aufrufen der Reservierungs-API

Reservierungen werden im Inventory Visibility-Dienst vorgenommen, indem Sie eine POST-Anfrage an die URL des Dienstes senden, z. B. `/api/environment/{environment-ID}/onhand/reserve`.

Für eine Reservierung muss der Anfragekörper eine Organisations-ID, eine Produkt-ID, reservierte Mengen und Dimensionen enthalten. Die Anfrage generiert eine eindeutige Reservierungs-ID für jeden Reservierungsdatensatz. Der Reservierungsdatensatz enthält die eindeutige Kombination aus der Produkt-ID und den Dimensionen.

Wenn Sie die Reservierungs-API aufrufen, können Sie die Reservierungsvalidierung steuern, indem Sie den booleschen `ifCheckAvailForReserv`-Parameter im Anforderungstext angeben. Der Wert `True` bedeutet, dass die Validierung erforderlich ist, während der Wert `False` bedeutet, dass die Validierung nicht erforderlich ist. Der Standardwert ist `True`.

Wenn Sie eine Reservierung stornieren oder die Reservierung bestimmter Bestandsmengen aufheben möchten, setzen Sie die Menge auf einen negativen Wert und legen Sie den `ifCheckAvailForReserv`-Parameter auf `False` fest, um die Validierung zu überspringen.

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

### <a name="set-up-the-reservation-offset-modifier"></a>Einrichten des Modifikators für den Reservierungsversatz

Falls noch nicht geschehen, richten Sie den Reservierungsmodifikator wie in [Einschalten und Einrichten der Reservierungsfunktion](#turn-on) beschrieben ein.

### <a name="set-up-reservation-ids"></a>Reservierungs-IDs festlegen

Die Reservierungs-ID kennzeichnet einen Reservierungsdatensatz in Inventory Visibility auf eindeutige Weise. Im Supply Chain Management setzen Benutzer Reservierungen auf Auftragszeilen, um den Offset für den entsprechenden Datensatz der Reservierung zu markieren.

Um Reservierungs-IDs im Supply Chain Management festzulegen, gehen Sie wie folgt vor.

1. Öffnen Sie einen Verkaufsauftrag (z. B. auf der Seite **Alle Verkaufsaufträge**).
1. Wählen Sie auf dem Inforegister **Verkaufsauftragszeilen** eine Auftragszeile aus.
1. Wählen Sie auf der Registerkarte **Verkaufsauftragszeilen** Inforegister **Zeile aktualisieren \> Bestand \> Bestandssichtbarkeits-Integration**.
1. Geben Sie die entsprechenden Reservierungs-IDs ein.

Die Änderung des Bestandsstatus stimmt mit der Einrichtung des Offset-Modifikators überein.
