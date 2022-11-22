---
title: Inventory Visibility-Reservierungen
description: In diesem Artikel wird beschrieben, wie Sie die Funktion "Reservierungen" festlegen, um mit Inventory Visibility Reservierungen zu erstellen, Reservierungen zu verbrauchen und/oder die Reservierung bestimmter Bestandsmengen aufzuheben.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762721"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility-Reservierungen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt einen typischen Anwendungsfall für weiche Reservierungen und erklärt, wie Sie sie in Bestandsanzeige einrichten. Es enthält Informationen darüber, wie man weiche Reservierungen erstellt, sie bei physischem Verbrauch verrechnet und bestimmte Bestandsmengen anpasst oder die Reservierung aufhebt.

## <a name="sample-use-case-for-soft-reservation"></a>Beispielanwendungsfall für die weiche Reservierung

Weiche Reservierungen helfen Unternehmen dabei, eine einzige Quelle der Wahrheit für verfügbares Inventar zu erreichen, insbesondere während des Auftragserfüllungsprozesses. Diese Funktion ist nützlich für Organisationen, in denen die folgenden Bedingungen vorliegen:

- Die Organisation verfügt über mindestens zwei verschiedene Systeme, die ausgehende Bestellungen direkt entgegennehmen.
- Die Organisation ist sehr streng und möchte Doppelbuchungen von Produktbeständen verhindern, die auftreten können, wenn mehrere Systeme den letzten Bestand überbuchen können. Diese Situation wird verhindert, wenn alle Bestellsysteme sofortige Soft-Reservierungs-API-Aufrufe an Bestandsanzeige senden können, die eine einzige Informationsquelle für die Inventarverfügbarkeit bietet.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="Bestandsanzeige-Soft-Reservierungen" width="720" />](media/inventory-visibility-soft-reservation.png)

Die vorherige Abbildung zeigt, wie die weiche Reservierung funktioniert, und hebt die folgenden Vorgänge hervor:

- Ihr anfänglicher Lagerbestand wird mit Bestandsanzeige von Microsoft Dynamics 365 Supply Chain Management synchronisiert.
- Vorläufige Reservierungen werden von jedem Ihrer Bestellkanäle oder -Systeme an Bestandsanzeige gesendet. Bestandsanzeige validiert die Inventarverfügbarkeit und versucht, eine weiche Reservierung vorzunehmen. Wenn die Soft-Reservierung erfolgreich ist, fügt Bestandsanzeige die Soft-Reservierungsmenge hinzu, zieht sie von der für Reservierungen verfügbaren Menge (AFR) ab und antwortet mit einer Soft-Reservierungs-ID.
- Zu diesem Zeitpunkt bleibt Ihre physische Bestandsmenge gleich.
- Sie können dann entweder einzelne oder aggregierte weich reservierte Bestellungen (Auftragspositionen) mit Supply Chain Management synchronisieren, um harte Reservierungen vorzunehmen und an das Lager freizugeben oder die endgültige Bestandsmenge zu aktualisieren.
- Sie können das System auf [Soft-Reservierungen ausgleichen](#offset-scm) einstellen, wenn der physische Bestand im Supply Chain Management aktualisiert wird.

Soft-Reservierungen werden normalerweise mithilfe von API-Aufrufen an den Dienst zur Bestandsanzeige erstellt, verbraucht und storniert.

> [!NOTE]
> Optional können Sie Supply Chain Management (und andere Systeme von Drittanbietern) so festlegen, dass die reservierte Menge automatisch durch die Verwendung von Inventory Visibility ausgeglichen wird. Die verrechnete Menge wird aus den Datensätzen der Reservierung in Inventory Visibility gelöscht.
>
> Standardmäßig wird die Offset-Funktion automatisch eingeschaltet, wenn Sie die Soft-Reservierungsfunktion aktivieren.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Einschalten und Einrichten der Reservierungsfunktion

Um die Funktion "Reservierung" einzuschalten, gehen Sie folgendermaßen vor.

1. Melden Sie sich bei Power Apps an und öffnen Sie **Bestandsanzeige**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Schalten Sie auf der Registerkarte **Funktionsverwaltung** die Funktion *OnHandReservierung* ein.
1. Melden Sie sich bei Ihrer Supply Chain Management-Umgebung an.
1. Gehen Sie zum Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** und aktivieren Sie die Funktion *Integration der Bestandssichtbarkeit mit Reservierungsversatz* (erfordert Version 10.0.22 oder höher).
1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Bestandssichtbarkeit-Integrationsparameter**, öffnen Sie die Registerkarte **Reservierungsversatz** und nehmen Sie die folgenden Einstellungen vor:

    - **Reservierungsversatz aktivieren** – Auf *Ja* festlegen, um diese Funktion zu aktivieren.
    - **Modifikator für Reservierungsversatz** – Wählen Sie den Bestandstransaktionsstatus aus, der Reservierungen verrechnet, die in der Bestandsanzeige vorgenommen wurden. Diese Einstellung legt die Auftragsbearbeitungsstufe fest, die einen Versatz auslöst. Die Stufe wird durch den Status der Bestandstransaktion des Auftrags nachverfolgt. Wählen Sie einen der folgenden Werte aus:

        - *Bei Bestellung* – Bestellungen mit dem Status *Bei Bestellung* senden eine Offset-Anfrage, wenn sie erstellt werden. Die Versatzmenge ist die Menge des erstellten Auftrags (Position).
        - *Reservieren* – Bestellungen mit einem *Reservieren* Status senden eine Offset-Anfrage, wenn sie entweder bestellt oder physisch reserviert sind. Beim Vesetzen am *Reservieren* Status, sendet die Bestellung eine Ausgleichsanforderung bei jedem neuen Bestandsstatus, der dem reservierten, kommissionierten Status am nächsten kommt (z. B. kommissioniert, Lieferschein gebucht oder fakturiert). Dieses Verhalten tritt auch dann auf, wenn Sie die Reservierung in Supply Chain Management überspringen und zu einem anderen Bestandsstatus wechseln (z. B. wenn Sie von der Freigabe zum Lager zum Kommissionieren und Verpacken springen). Die Anfrage wird nur einmal ausgelöst. Wenn es bei der Entnahme ausgelöst wurde, wird der Versatz nicht dupliziert, wenn ein Lieferschein gebucht wird. Die Versatzmenge ist die gleiche Menge wie die Menge des Bestandstransaktionsstatus, als der Versatz ausgelöst wurde (mit anderen Worten *Bestellt reserviert*/*Physisch reservieren*, oder ein späterer Status auf der entsprechenden Bestellungsposition).

1. Melden Sie sich wieder bei der Bestandsanzeige-App an, gehen Sie zur **Konfiguration** Seite und prüfen Sie dann auf der **Soft-Reservierung** Registerkarte die Standardhierarchie für weiche Reservierungen. Fügen Sie der Hierarchie nach Bedarf neue Dimensionen hinzu.
1. Sehen Sie sich im **Legen Sie die weiche Reservierungszuordnung fest** Abschnitt die Standardeinstellungen an. Standardmäßig werden die vorläufig reservierten Bestandsmengen gegen die `softreservephysical` physikalisches Maß der Datenquelle `iv` erfasst. Die *Verfügbar für Reservierung* berechnete Messung ist `availabletoreserve` zugeordnet. Wenn Sie die `availabletoreserve` berechnetes Messung aktualisieren möchten, gehen Sie zur **Konfiguration** Seite und erweitern Sie dann auf der **Berechnete Messung** Registerkarte die berechnete Kennzahl und passen Sie sie an.

Weitere Informationen finden Sie unter [Bestandsanzeige konfigurieren](inventory-visibility-configuration.md).

> [!NOTE]
> Die Reservierungshierarchie beschreibt die Sequenz von Dimensionen, die bei der Reservierung angegeben werden müssen. Sie funktioniert auf die gleiche Weise wie die Indexhierarchie für verfügbare Abfragen, wird jedoch unabhängig verwendet, damit Benutzer Dimensionsdetails angeben können, um genauere Reservierungen vorzunehmen.
>
> Die Hierarchie Ihrer Soft-Reservierung sollte `SiteId` und `LocationId` als Komponenten enthalten, da sie die Partitionskonfiguration der Bestandsanzeige aufbauen.

Weitere Informationen über die Konfiguration von Reservierungen finden Sie unter [Reservierungskonfiguration](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Verwenden Sie die Funktion "Reservierung" in Inventory Visibility

Wenn Sie die Reservierungs-API aufrufen, markiert das System die Reservierung der angegebenen Waren und Mengen.

Hier ist ein Beispielszenario und ein Beispiel für einen API-Abfragetext. Das Unternehmen Contoso verkauft das Produkt D0002 (Cabinet) über seine E-Commerce-Website. Ein Kunde bestellt über die Website einen kleinen roten Schrank. Contoso beschließt, diese Bestellung mit den folgenden Dimensionen auszuführen:

- Organisationskennung = usmf
- Standort = 1
- Lagerort = 11
- Produkt = D0002
- Farbe = rot
- Größe = small

Contoso hat bereits eine API-Verbindung zu Inventory Visibility aus seinem eigenen E-Commerce-System eingerichtet. Wenn die Bestellung eingeht, löst das System sofort einen API-Aufruf aus, um eine weiche Reservierung für den Schrank in der Bestandsanzeige vorzunehmen.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Erstellen Sie weiche Reservierungen mit der Reservierungs-API

Reservierungen werden im Inventory Visibility-Dienst vorgenommen, indem Sie eine POST-Anfrage an die URL des Dienstes senden, z. B. `/api/environment/{environmentId}/onhand/reserve`.

Für eine Reservierung muss der Anfragekörper eine Organisations-ID, eine Produkt-ID, reservierte Mengen und Dimensionen enthalten.

Wenn Sie die Reservierungs-API aufrufen, können Sie die Reservierungsvalidierung steuern, indem Sie den booleschen `ifCheckAvailForReserv`-Parameter im Anforderungstext angeben. Der Wert `True` bedeutet, dass die Validierung erforderlich ist, während der Wert `False` bedeutet, dass die Validierung nicht erforderlich ist. Der Standardwert ist `True`.

Wenn Sie eine Reservierung stornieren oder die Reservierung bestimmter Bestandsmengen aufheben möchten, setzen Sie die Menge auf einen negativen Wert und legen Sie den `ifCheckAvailForReserv`-Parameter auf `False` fest, um die Validierung zu überspringen.

Hier ist ein Beispiel für den Anfragetext, der auf den Verkaufsauftrag im vorherigen Kontext verweist.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Eine erfolgreiche weiche Reservierungsanforderung gibt eine *Soft-Reservierungs-ID* für jeden Reservierungsdatensatz zurück. Die Soft-Reservierungs-ID ist kein eindeutiger Bezeichner für einen einzelnen Soft-Reservierungsdatensatz, sondern eine Kombination aus der Produkt-ID und Dimensionswerten, die der Soft-Reservierungsanforderung zugeordnet sind. Sie können die Soft-Reservierungs-ID in der Auftragsposition aufzeichnen, wenn Sie die erfolgreich reservierten Aufträge zum Ausgleich mit Supply Chain Management oder einem anderen ERP-System synchronisieren.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Offset-Soft-Reservierungen im Supply Chain Management

Sie können eine vorläufig reservierte Menge ausgleichen, nachdem die Menge einer Bestellung in Supply Chain Management oder einem anderen ERP-System physisch abgezogen wurde. Bestandsanzeige bietet eine Out-of-Box-Integration mit weichem Reservierungsausgleich und Supply Chain Management.

Befolgen Sie diese Schritte, um eine Soft-Reservierung zu versetzen.

1. Melden Sie sich im Supply Chain Management an.
1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Erstellen Sie den externen Verkaufsauftrag neu und fügen Sie eine Verkaufszeile hinzu, die genau dieselben Werte für Produkt-ID, Organisation, Standort, Lager und Dimensionen verwendet.
1. Wählen Sie im Inforegister **Auftragspositionen** die Auftragsposition, die Sie gerade eingegeben haben und wählen Sie dann in der Symbolleiste **Bestand \> Reservierungskennung**.
1. Führen Sie einen dieser Schritte aus:

    - Kopieren Sie die Soft-Reservierungs-ID in Ihrer Antwort auf die Soft-Reservierungsanfrage und fügen Sie sie in das Feld **Reservierungs-ID** ein.
    - Lassen Sie das Feld **Reservierungs-ID** leer, aber wählen Sie die das **Automatischer Versatz des Inventarservices** Kontrollkästchen aus. Das System bestimmt automatisch, welches Produkt und welche Produktabmessungen ausgeglichen werden sollen, basierend auf der Artikel-ID und den Dimensionswerten, die in der ausgewählten Zeile eingegeben werden.

1. Wählen Sie **OK** aus.
1. Während dieselbe Auftragsposition weiterhin ausgewählt ist, reservieren Sie die bestellte Menge physisch, indem Sie im Inforegister **Bestand \> Reservierung** auf der Menüleiste des Inforegister **Auftragspositionen** auswählen.
1. Wenn Sie zuvor das Feld **Reservierungs-Offset-Modifikator** zu *Reserviert* eingestellt haben, wird der Offset ausgelöst, wenn die Auftragsposition den Status *Physisch reservieren* oder *Reserve bestellt* hat. Ein Batch-Job wird einmal pro Minute ausgeführt, um Offset-Anfragen von Supply Chain Management mit Bestandsanzeige zu synchronisieren.

> [!NOTE]
> Für Transaktionsstatus, die einen bestimmten Reservierungs-Offset-Modifikator enthalten, wird die Transaktion den entsprechenden Reservierungsdatensatz ausgleichen, wenn alle folgenden Bedingungen erfüllt sind:
>
> - Die Reservierungs-ID der Bestandstransaktion stimmt mit der Reservierungs-ID des Reservierungsdatensatzes in der Bestandsanzeige überein.
> - Die Dimensionen der Bestandstransaktion passt zu den Dimensionen des Reservierungsdatensatzes in der Bestandsanzeige.
> - Änderungen im Status der Bestandstransaktion lösen Auslösungen für Reservierungen aus, wenn der Status der Bestandstransaktion die Tatsache widerspiegelt, dass ein Bestellvorgang abgeschlossen oder übersprungen wurde.

Offset-Mengen folgen den Bestandsmengen, die auf die relevanten Bestandstransaktionen festgelegt sind. Ein Offset wird nur wirksam, wenn keine reservierte Menge in der Bestandsanzeige verbleibt.

### <a name="cancel-or-revert-a-soft-reservation"></a>Stornieren oder stornieren Sie eine weiche Reservierung

Wenn eine ursprüngliche Bestellposition storniert oder gelöscht wird und Sie die entsprechende weiche Reservierung rückgängig machen müssen, buchen Sie eine negative Menge, die genau dieselben Informationen in Ihrem API-Abfragetext enthält.
