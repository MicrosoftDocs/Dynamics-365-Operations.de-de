---
title: Inventory Visibility konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie Inventory Visibility konfigurieren.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cd5d2cf112a9d2ccdf6226ee79f0ff488d51066b
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066669"
---
# <a name="configure-inventory-visibility"></a>Inventory Visibility konfigurieren

[!include [banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie Sie die Bestandsanzeige mit der Bestandsanzeige-App in Power Apps konfigurieren.

## <a name="introduction"></a><a name="introduction"></a>Einführung

Bevor Sie mit Inventory Visibility arbeiten können, müssen Sie die folgende Konfiguration wie in diesem Artikel beschrieben durchführen:

- [Datenquellenkonfiguration](#data-source-configuration)
- [Partitionskonfiguration](#partition-configuration)
- [Produktindex-Hierarchie-Konfiguration](#index-configuration)
- [Reservierungskonfiguration (optional)](#reservation-configuration)
- [Beispiel für die Standardkonfiguration](#default-configuration-sample)

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, installieren Sie das Bestandsanzeige-Add-In und richten es wie in [Bestandsanzeige installieren und einrichten](inventory-visibility-setup.md) beschrieben ein.

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Die Konfigurationsseite der Bestandsanzeige-App

In Power Apps hilft Ihnen die Seite **Konfiguration** der [Bestandsanzeige-App](inventory-visibility-power-platform.md) beim Festlegen der Konfiguration des Lagerbestands und der Softreservierung. Nach der Installation des Add-Ins enthält die Standardkonfiguration den Wert von Microsoft Dynamics 365 Supply Chain Management (die Datenquelle `fno`). Sie können die Standardeinstellungen überprüfen. Zusätzlich können Sie die Konfiguration basierend auf Ihren geschäftlichen Anforderungen und den Bestandsbuchungsanforderungen Ihres externen Systems ändern, um die Art und Weise zu standardisieren, in der Bestandsänderungen in den verschiedenen Systemen gebucht, organisiert und abgefragt werden können. In den verbleibenden Abschnitten dieses Artikels wird erläutert, wie die einzelnen Teile der Seite **Konfiguration** zu verwenden sind.

Nachdem die Konfiguration abgeschlossen ist, wählen Sie in der App unbedingt **Konfiguration aktualisieren** aus.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Aktivieren Sie die Bestandsanzeigefunktionen in der Funktionsverwaltung von Power Apps

Das Bestandsanzeige-Add-In fügt Ihrer Power Apps-Installation mehrere neue Funktionen hinzu. Standardmäßig sind diese Funktionen ausgeschaltet. Um sie zu verwenden, öffnen Sie die Seite **Konfiguration** und schalten Sie dann auf der Registerkarte **Funktionsverwaltung** die folgenden Funktionen nach Bedarf ein.

| Name der Funktionsverwaltung | Description |
|---|---|
| *OnHandReservation* | Mit dieser Funktion können Sie mithilfe von Inventory Visibility Reservierungen erstellen, Reservierungen verbrauchen und/oder bestimmte Bestandsmengen aufheben. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Diese Funktion bietet eine Bestandsübersicht für Produkte zusammen mit allen Dimensionen. Die Bestandsübersicht wird regelmäßig von der Bestandsanzeige synchronisiert. Weitere Informationen finden Sie unter [Bestandsübersicht](inventory-visibility-power-platform.md#inventory-summary). |
| *OnhandChangeSchedule* | Die optionale Funktion aktiviert die Funktionen Lagerbestandsänderung und Available to Promise (ATP). Weitere Informationen finden Sie unter [Inventory Visibility: verfügbarer Änderungszeitplan und verfügbar für Zusage](inventory-visibility-available-to-promise.md). |
| *Zuweisung* | Diese optionale Funktion ermöglicht Inventory Visibility, Inventarschutz (Ringfencing) und Überverkaufskontrolle zu bieten. Weitere Informationen finden Sie unter [Bestandszuordnung für Bestandsichtbarkeit](inventory-visibility-allocation.md) |
| *Lagerortartikel in Bestandsanzeige aktivieren* | Diese optionale Funktion ermöglicht Inventory Visibility, um Artikel zu unterstützen, die für Prozesse der Lagerverwaltung (WMS) aktiviert sind. Weitere Informationen finden Sie unter [Inventory Visibility-Unterstützung für WMS-Artikel](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finden Sie den Dienst-Endpunkt

Wenn Sie den richtigen Dienst-Endpunkt für Inventory Visibility nicht kennen, öffnen Sie die Seite **Konfiguration** in Power Apps und wählen Sie dann **Dienst-Endpunkt anzeigen** in der oberen rechten Ecke. Die Seite zeigt den korrekten Dienst-Endpunkt an.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Datenquellenkonfiguration

Jede Datenquelle steht für ein System, aus dem Ihre Daten stammen. Beispielhafte Datenquellennamen sind `fno` (was für „Dynamics 365 Finanz- und Betriebs-Apps“ steht) und `pos` (was für „Point of Sale“ steht). Standardmäßig ist das Supply Chain Management als Standard-Datenquelle (`fno`) in Inventory Visibility festgelegt.

> [!NOTE]
> Die Datenquelle `fno` ist für das Supply Chain Management reserviert. Wenn Ihr Inventory Visibility-Add-In in eine Supply Chain Management Umgebung integriert ist, empfehlen wir Ihnen, keine Konfigurationen zu löschen, die sich auf `fno` in der Datenquelle beziehen.

Um eine Datenquelle hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Datenquelle** die Option **Neue Datenquelle**, um eine Datenquelle hinzuzufügen.

> [!NOTE]
> Wenn Sie eine Datenquelle hinzufügen, stellen Sie sicher, dass Sie den Namen der Datenquelle, die physikalischen Kennzahlen und die Zuordnungen der Dimensionen überprüfen, bevor Sie die Konfiguration für den Dienst "Inventory Visibility" aktualisieren. Sie können diese Einstellungen nicht mehr ändern, nachdem Sie **Konfiguration aktualisieren** gewählt haben.

Die Datenquellenkonfiguration umfasst die folgenden Teile:

- Dimensionen (Zuordnung von Dimensionen)
- Physikalische Messungen
- Berechnete Messungen

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensionen (Zuordnung von Dimensionen)

Der Zweck der Dimensionskonfiguration ist die Standardisierung der Multisystem-Integration für Buchungsereignisse und Abfragen, basierend auf Dimensionskombinationen. Inventory Visibility bietet eine Liste von Basisdimensionen, die den Dimensionen Ihrer Datenquelle zugeordnet werden können. Dreiunddreißig Dimensionen sind für die Zuordnung verfügbar.

- Wenn Sie Supply Chain Management als eine Ihrer Datenquellen verwenden, werden standardmäßig 13 Dimensionen den Supply Chain Management Standarddimensionen zugeordnet. Zwölf weitere Dimensionen (`inventDimension1` bis `inventDimension12`) sind angepassten Dimensionen im Supply Chain Management zugeordnet. Die restlichen acht Dimensionen sind erweiterte Dimensionen, die Sie externen Datenquellen zuordnen können.
- Wenn Sie Supply Chain Management nicht als eine Ihrer Datenquellen verwenden, können Sie die Dimensionen frei zuordnen. Die folgende Tabelle zeigt die vollständige Liste der verfügbaren Dimensionen.

> [!NOTE]
> Wenn Ihre Dimension nicht in der Liste der Standarddimensionen enthalten ist und Sie eine externe Datenquelle verwenden, empfehlen wir Ihnen, die Zuordnung mit `ExtendedDimension1` bis `ExtendedDimension8` vorzunehmen.

| Dimensionstyp | Basis-Dimensionen |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Nachverfolgung | `BatchId` |
| Nachverfolgung | `SerialId` |
| Speicherort | `LocationId` |
| Speicherort | `SiteId` |
| Bestandsstatus | `StatusId` |
| Lagerspezifisch | `WMSLocationId` |
| Lagerspezifisch | `WMSPalletId` |
| Lagerspezifisch | `LicensePlateId` |
| Andere | `VersionId` |
| Bestand (angepasst) | `InventDimension1` bis `InventDimension12` |
| Erweiterung | `ExtendedDimension1` durch `ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> Die Dimensionen, die in der vorangehenden Tabelle aufgeführt sind, dienen nur als Referenz. Sie müssen sie nicht in Inventory Visibility definieren.
>
> (Angepasste) Dimensionen für den Bestand können für das Supply Chain Management reserviert sein. In diesem Fall können Sie stattdessen die erweiterten Dimensionen verwenden.

Externe Systeme können über die RESTful-APIs von Inventory Visibility zugreifen. Für die Integration können Sie in Inventory Visibility die _externe Datenquelle_ und die Zuordnung von den _externen Dimensionen_ zu den _Basisdimensionen_ konfigurieren. Hier ist ein Beispiel für eine Tabelle zur Zuordnung von Dimensionen.

| Externe Dimension | Basis Dimensionen |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Indem Sie eine Zuordnung von Dimensionen konfigurieren, können Sie die externen Dimensionen direkt an Inventory Visibility senden. Inventory Visibility wandelt dann die externen Dimensionen automatisch in Basisdimensionen um.

Um Zuordnungen von Dimensionen hinzuzufügen, gehen Sie wie folgt vor.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Datenquelle** im Abschnitt **Dimensions-Zuordnungen** die Option **Hinzufügen**, um Dimensions-Zuordnungen hinzuzufügen.
    ![Hinzufügen von Zuordnungen von Dimensionen](media/inventory-visibility-dimension-mapping.png "Hinzufügen von Zuordnungen von Dimensionen")

1. Geben Sie im Feld **Dimensionsname** die Quelldimension an.
1. Wählen Sie im Feld **Zur Basisdimension** die Dimension in Inventory Visibility, die Sie zuordnen möchten.
1. Wählen Sie **Speichern** aus.

Wenn Ihre Datenquelle z. B. eine Produktfarbendimension enthält, können Sie diese der Basisdimension `ColorId` zuordnen, um eine angepasste Dimension `ProductColor` in der Datenquelle `exterchannel` hinzuzufügen. Sie wird dann der Basisdimension `ColorId` zugeordnet.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Physikalische Messungen

Wenn eine Datenquelle eine Bestandsänderung an Inventory Visibility sendet, sendet sie diese Änderung unter Verwendung von *physikalischen Messungen*. Physikalische Messungen verändern die Menge und spiegeln den Status des Bestands wider. Sie können Ihre eigenen physikalischen Messungen, basierend auf Ihren Anforderungen, definieren. Abfragen können auf den physikalischen Kennzahlen basieren.

Inventory Visibility bietet eine Liste von standardmäßigen physikalischen Messungen, die mit Supply Chain Management (der Datenquelle `fno`) verknüpft sind. Diese voreingestellten physikalischen Kennzahlen werden aus den Status der Transaktionen im Lagerbestand auf der Seite **Bestandsliste** im Supply Chain Management (**Bestandsverwaltung \> Abfragen und Bericht \> Bestandsliste**) übernommen. Die folgende Tabelle enthält ein Beispiel für physikalische Messungen.

| Name der physikalischen Messung | Beschreibung |
|---|---|
| `NotSpecified` | Nicht angegeben |
| `Arrived` | Angekommen |
| `AvailOrdered` | Verfügbar Bestellt |
| `AvailPhysical` | Physisch verfügbar |
| `Deducted` | Abgesetzt |
| `OnOrder` | BeiBestellung |
| `Ordered` | Bestellt |
| `PhysicalInvent` | Physischer Bestand |
| `Picked` | Entnommen |
| `PostedQty` | Gebuchte Menge |
| `QuotationIssue` | Angebotsabgang |
| `QuotationReceipt` | Angebotszugang |
| `Received` | Eingegangen |
| `Registered` | Erfasst |
| `ReservOrdered` | Bestellt reserviert |
| `ReservPhysical` | Physisch reserviert |

Wenn die Datenquelle Supply Chain Management ist, müssen Sie die standardmäßigen physikalischen Messungen nicht neu erstellen. Für externe Datenquellen können Sie jedoch neue physikalische Messungen erstellen, indem Sie die folgenden Schritte ausführen.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Datenquelle** im Abschnitt **Physikalische Messungen** die Option **Hinzufügen**, geben Sie einen Namen für die Quelle der Messungen an und speichern Sie die Änderungen.

### <a name="calculated-measures"></a>Berechnete Messungen

Sie können Inventory Visibility verwenden, um sowohl physische Messungen im Bestand als auch *angepasste berechnete Kennzahlen* abzufragen. Berechnete Maße bieten eine angepasste Berechnungsformel, die aus einer Kombination von physikalischen Messungen besteht. Mit dieser Funktionalität können Sie eine Reihe von physikalischen Kennzahlen festlegen, die addiert werden, und/oder eine Reihe von physikalischen Kennzahlen, die subtrahiert werden, um das Formular für die angepasste Messung zu bilden.

> [!IMPORTANT]
> Ein berechnetes Measure ist eine Zusammenstellung von physikalischen Measures. Seine Formel kann nur physikalische Measures ohne Duplikate enthalten, keine berechneten Measures.

In der Konfiguration können Sie eine Reihe von Modifikatoren festlegen, die addiert oder subtrahiert werden, um die gesamte aggregierte Ausgabemenge zu erhalten.

Um eine angepasste berechnete Messung festzulegen, befolgen Sie diese Schritte.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Auf der Registerkarte **Berechnete Messung** wählen Sie **Neue berechnete Messung**, um eine berechnete Messung hinzuzufügen.
1. Legen Sie die folgenden Felder für die neue berechnete Messung fest:

    - **Neuer Name der berechneten Messung** - Geben Sie den Namen der berechneten Messung ein.
    - **Datenquelle** - Wählen Sie die Datenquelle aus, die mit dem neuen Modifikator verknüpft ist. Das abfragende System ist eine Datenquelle.

1. Wählen Sie **Hinzufügen**, um der neu berechneten Messung einen Modifikator hinzuzufügen.
1. Legen Sie die folgenden Felder für den neuen Modifikator fest:

    - **Modifikator** - Wählen Sie den Modifikatortyp (*Zugabe* oder *Subtraktion*).
    - **Datenquelle** - Wählen Sie die Datenquelle aus, in der die Messung, die den Modifikatorwert liefert, gefunden werden soll.
    - **Messung** - Wählen Sie den Namen der Messung (aus der ausgewählten Datenquelle), die den Wert für den Modifikator liefert.

1. Wiederholen Sie die Schritte 5 bis 6, bis Sie alle erforderlichen Modifikatoren hinzugefügt haben.
1. Wählen Sie **Speichern** aus.

Sie erhalten zum Beispiel das folgende Abfrageergebnis.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Sie konfigurieren dann eine berechnete Messung, die den Namen `MyCustomAvailableforReservation` trägt, wie in der folgenden Tabelle gezeigt. Diese berechnete Kennzahl wird vom Verbrauchssystem verbraucht.

| Verbrauchs-System | Berechnete Messung | Datenquelle | Physikalische Messung | Berechnungstyp |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Wenn diese Berechnungsformel verwendet wird, wird das neue Abfrageergebnis die angepasste Messung enthalten.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Die Ausgabe von `MyCustomAvailableforReservation` lautet basierend auf der Berechnungseinstellung in den angepassten Messungen 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Partitionskonfiguration

Die Partitionskonfiguration besteht derzeit aus zwei Basisdimensionen (`SiteId` und `LocationId`), die angeben, wie die Daten verteilt werden. Vorgänge unter der gleichen Partition können eine höhere Leistung zu geringeren Kalkulationen liefern. Die folgende Tabelle zeigt die Standardpartitionskonfiguration, die das Bestandssichtbarkeits-Add-In bereitstellt.

| Basis-Dimensionen | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Die Lösung enthält diese Partitionskonfiguration standardmäßig. Daher *müssen Sie sie nicht selbst definieren*.

> [!IMPORTANT]
> Passen Sie die Standardkonfiguration der Partition nicht an. Wenn Sie es löschen oder ändern, werden Sie wahrscheinlich einen unerwarteten Fehler verursachen.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Produktindex-Hierarchie-Konfiguration

In den meisten Fällen wird die Abfrage des Lagerbestands nicht nur auf der höchsten Ebene "Gesamt" erfolgen. Stattdessen möchten Sie vielleicht auch Ergebnisse sehen, die auf Basis der Bestandsdimensionen aggregiert sind.

Inventory Visibility bietet Flexibilität, indem Sie die _Indizes_ festlegen können. Diese Indizes basieren auf einer Dimension oder einer Kombination von Dimensionen. Ein Index besteht aus einer *Satznummer*, einer *Dimension* und einer *Hierarchie*, wie in der folgenden Tabelle festgelegt.

| Name | Beschreibung |
|---|---|
| Set-Nummer festlegen | Dimensionen, die zum gleichen Set (Index) gehören, werden gruppiert, und ihnen wird die gleiche Set-Nummer zugewiesen. |
| Dimensionen | Basisdimensionen, über die das Abfrageergebnis aggregiert wird. |
| Hierarchie | Die Hierarchie wird verwendet, um die unterstützten Dimensionen-Kombinationen zu definieren, die abgefragt werden können. Sie legen z. B. ein Dimensionen-Set fest, das eine Hierarchie-Sequenz von `(ColorId, SizeId, StyleId)` hat. In diesem Fall unterstützt das System Abfragen auf vier Dimensionen-Kombinationen. Die erste Kombination ist leer, die zweite ist `(ColorId)`, die dritte ist `(ColorId, SizeId)` und die vierte ist `(ColorId, SizeId, StyleId)`. Die anderen Kombinationen werden nicht unterstützt. Weitere Informationen finden Sie im folgenden Beispiel. |

Um Ihren Produkthierarchie-Index festzulegen, gehen Sie wie folgt vor.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Produkthierarchie-Index** im Abschnitt **Dimensions-Zuordnungen** die Option **Hinzufügen**, um Zuordnungen von Dimensionen hinzuzufügen.
1. Standardmäßig wird eine Liste von Indizes bereitgestellt. Um einen vorhandenen Index zu ändern, wählen Sie **Bearbeiten** oder **Hinzufügen** im Abschnitt für den betreffenden Index. Um einen neuen Indexsatz zu erstellen, wählen Sie **Neuer Indexsatz**. Wählen Sie für jede Zeile in jedem Indexsatz im Feld **Dimension** aus der Liste der Basisdimensionen aus. Die Werte für die folgenden Felder werden automatisch generiert:

    - **Set-Nummer** - Dimensionen, die zur gleichen Gruppe (Index) gehören, werden zusammen gruppiert, und ihnen wird die gleiche Set-Nummer zugewiesen.
    - **Hierarchie** - Die Hierarchie wird verwendet, um die unterstützten Dimensionskombinationen zu definieren, die in einer Dimensionsgruppe (Index) abgefragt werden können. Wenn Sie z. B. eine Dimensionsgruppe festlegen, die eine Hierarchie-Sequenz von *Stil*, *Farbe* und *Größe* hat, unterstützt das System das Ergebnis von drei Abfragegruppen. Die erste Gruppe ist nur Stil. Die zweite Gruppe ist eine Kombination aus Stil und Farbe. Und die dritte Gruppe ist eine Kombination aus Stil, Farbe und Größe. Die anderen Kombinationen werden nicht unterstützt.

> [!TIP]
> Hier sind ein paar Tipps, die Sie beim Einrichten Ihrer Indexhierarchie beachten sollten:
>
> - Basisdimensionen, die in der Partitionskonfiguration definiert sind, sollten nicht in Indexkonfigurationen definiert werden. Wenn in der Indexkonfiguration erneut eine Basisdimension definiert wird, können Sie nicht nach diesem Index abfragen.
> - Wenn Sie nur Bestand abfragen müssen, der durch alle Dimensionskombinationen aggregiert wird, können Sie einen einzelnen Index einrichten, der die Basisdimension `Empty` enthält.
> - Sie müssen mindestens eine Indexhierarchie haben (die beispielsweise die Basisdimension enthält `Empty`), andernfalls schlagen Abfragen mit dem Fehler „Es wurde keine Indexhierarchie festgelegt“ fehl.

### <a name="example"></a>Beispiel

In diesem Abschnitt finden Sie ein Beispiel, das zeigt, wie die Hierarchie funktioniert.

Die folgende Tabelle zeigt eine Liste der verfügbaren Bestände für dieses Beispiel.

| Artikel | ColorId | SizeId | StyleId | Menge |
|---|---|---|---|---|
| T-Shirt | Schwarz | Klein | Breit | 1 |
| T-Shirt | Schwarz | Klein | Regelmäßig | 2 |
| T-Shirt | Schwarz | Groß | Breit | 3 |
| T-Shirt | Schwarz | Groß | Regelmäßig | 4 |
| T-Shirt | Red | Klein | Breit | 5 |
| T-Shirt | Red | Klein | Regelmäßig | 6 |
| T-Shirt | Red | Groß | Regelmäßig | 7 |

Die folgende Tabelle zeigt, wie die Indexhierarchie festgelegt wird.

| Nummer festlegen | Dimensionen | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Mit dem Index können Sie den Lagerbestand auf die folgenden Arten abfragen:

- `()` - gruppiert nach allen

    - T-Shirt, 28

- `(ColorId)` - gruppiert nach `ColorId`

    - T-Shirt, Schwarz, 10
    - T-Shirt, Rot, 18

- `(ColorId, SizeId)` - gruppiert nach der Kombination von `ColorId` und `SizeId`

    - T-Shirt, Schwarz, Small, 3
    - T-Shirt, Schwarz, Large, 7
    - T-Shirt, Rot, Small, 11
    - T-Shirt, Rot, Large, 7

- `(ColorId, SizeId, StyleId)` - gruppiert nach der Kombination von `ColorId`, `SizeId` und `StyleId`

    - T-Shirt, Schwarz, Small, Wide, 1
    - T-Shirt, Schwarz, Small, Regular, 2
    - T-Shirt, Schwarz, Large, Wide, 3
    - T-Shirt, Schwarz, Large, Regular, 4
    - T-Shirt, Rot, Small, Wide, 5
    - T-Shirt, Rot, Small, Regular, 6
    - T-Shirt, Rot, Large, Regular, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Reservierungskonfiguration (optional)

Die Reservierungskonfiguration ist erforderlich, wenn Sie die Funktion der Soft-Reservierung verwenden möchten. Die Konfiguration besteht aus zwei grundlegenden Teilen:

- Soft-Reservierungs-Zuordnung
- Soft-Reservierungs-Hierarchie

### <a name="soft-reservation-mapping"></a>Zuordnung der Soft-Reservierung

Wenn Sie eine Reservierung vornehmen, möchten Sie vielleicht wissen, ob der Lagerbestand aktuell für die Reservierung verfügbar ist. Die Validierung ist mit einer berechneten Messung verknüpft, die eine Berechnungsformel aus einer Kombination von physikalischen Messungen darstellt.

Indem Sie die Zuordnung von der physikalischen Messung zur berechneten Messung festlegen, ermöglichen Sie dem Dienst Inventory Visibility, die Verfügbarkeit von Reservierungen automatisch zu überprüfen, basierend auf der physikalischen Messung.

Bevor Sie diese Zuordnung festlegen, müssen die physikalischen Messungen, die berechneten Messungen und ihre Datenquellen auf den Registerkarten **Datenquelle** und **Berechnete Messung** der Seite **Konfiguration** in Power Apps definiert werden (wie zuvor in diesem Artikel beschrieben).

Um die Zuordnung der Soft-Reservierung zu definieren, gehen Sie wie folgt vor.

1. Definieren Sie die physikalische Kennzahl, die als Soft-Reservierungsmaßnahme dient (zum Beispiel `SoftReservOrdered`).
1. Definieren Sie auf der Registerkarte **Berechnete Kennzahl** der Seite **Konfiguration** die *zur Reservierung verfügbare* (AFR) berechnete Kennzahl, die die AFR-Berechnungsformel enthält, die Sie der physikalischen Messung zuordnen möchten. Sie könnten z.B. `AvailableToReserve` (verfügbar für Reservierung) so festlegen, dass sie der zuvor definierten physikalischen Messung `SoftReservOrdered` zugeordnet wird. Auf diese Weise können Sie feststellen, welche Mengen, die den Bestandsstatus `SoftReservOrdered` haben, für die Reservierung verfügbar sind. Die folgende Tabelle zeigt die AFR-Berechnungsformel.

    | Berechnungstyp | Datenquelle | Physikalische Messung |
    |---|---|---|
    | Addition | `fno` | `AvailPhysical` |
    | Addition | `pos` | `Inbound` |
    | Subtraktion | `pos` | `Outbound` |
    | Subtraktion | `iv` | `SoftReservOrdered` |

    Wir empfehlen, die berechnete Messung so einzurichten, dass sie die physikalische Messung enthält, auf der die Reservierungsmessung basiert. Auf diese Weise wird die berechnete Messungsmenge durch die Reservierungsmessungsmenge beeinflusst. Daher sollte in diesem Beispiel die für `AvailableToReserve` berechnete Messung der `iv`-Datenquelle die physikalische Messung für `SoftReservOrdered` aus `iv` als Komponente enthalten.

1. Öffnen Sie die Seite **Konfiguration**.
1. Legen Sie auf der Registerkarte **Zuordnung von Soft-Reservierungen** die Zuordnung von der physischen Messung zur berechneten Kennzahl fest. Für das vorherige Beispiel könnten Sie die folgenden Einstellungen verwenden, um `AvailableToReserve` der zuvor definierten physikalischen Messung `SoftReservOrdered` zuzuordnen.

    | Datenquelle für physikalische Messungen | Physikalische Messung | Verfügbar für Reservierungsdatenquelle | Verfügbar für die berechnete Messung der Reservierung |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Wenn Sie die **Zuordnung von Soft-Reservierungen** nicht bearbeiten können, müssen Sie eventuell die Funktion *OnHandReservation* auf der Registerkarte **Funktionsverwaltung** einschalten.

Wenn Sie nun eine Reservierung für `SoftReservOrdered` vornehmen, findet Inventory Visibility automatisch `AvailableToReserve` und die zugehörige Berechnungsformel, um die Reservierungsvalidierung durchzuführen.

Sie haben z. B. den folgenden Lagerbestand in Inventory Visibility.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

In diesem Fall gilt die folgende Berechnung:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Wenn Sie also versuchen, eine Reservierung für `iv.SoftReservOrdered` vorzunehmen, und die Menge kleiner oder gleich `AvailableToReserve` (10) ist, können Sie die Reservierung durchführen.

> [!NOTE]
> Wenn Sie die Reservierungs-API aufrufen, können Sie die Reservierungsvalidierung steuern, indem Sie den booleschen `ifCheckAvailForReserv`-Parameter im Anforderungstext angeben. Der Wert `True` bedeutet, dass die Validierung erforderlich ist, während der Wert `False` bedeutet, dass die Validierung nicht erforderlich ist. Der Standardwert ist `True`.

### <a name="soft-reservation-hierarchy"></a>Soft-Reservierungs-Hierarchie

Die Reservierungshierarchie beschreibt die Sequenz von Dimensionen, die bei der Reservierung angegeben werden müssen. Sie funktioniert genauso wie die Produktindexhierarchie bei Lagerbestandsabfragen.

Die Reservierungshierarchie ist unabhängig von der Produktindexhierarchie. Diese Unabhängigkeit ermöglicht die Implementierung einer Kategorieverwaltung, bei der Benutzer die Dimensionen in Details aufschlüsseln können, um die Anforderungen für genauere Reservierungen zu spezifizieren. Die Hierarchie Ihrer Soft-Reservierung sollte `SiteId` und `LocationId` als Komponenten enthalten, da sie die Partitionskonfiguration aufbauen. Bei der Reservierung müssen Sie eine Partition für das Produkt angeben.

Hier ist ein Beispiel für eine weiche Reservierungshierarchie.

| Basis-Dimensionen | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

In diesem Beispiel können Sie Reservierungen in den folgenden Sequenzen von Dimensionen vornehmen: Bei der Reservierung müssen Sie eine Partition für das Produkt angeben. Daher ist `(SiteId, LocationId)` die grundlegende Hierarchie, die Sie verwenden können.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Eine gültige Sequenz von Dimensionen sollte strikt der Reservierungshierarchie folgen, Dimension für Dimension. Die Hierarchiesequenz `(SiteId, LocationId, SizeId)` ist z. B. nicht gültig, weil `ColorId` fehlt.

## <a name="available-to-promise-configuration-optional"></a>Verfügbare Konfiguration zum Versprechen (optional)

Sie können die Inventory Visibility festlegen, um zukünftige Lagerbestandsänderungen zu planen und ATP-Mengen (Available-to-Promise) zu berechnen. ATP ist die Menge eines Elements, die verfügbar ist und einem Kunden in der nächsten Periode zugesagt werden kann. Die Verwendung dieser Berechnung kann Ihre Funktionalitäten bei der Auftragsabwicklung erheblich verbessern. Um diese Funktion zu nutzen, müssen Sie sie auf der Registerkarte **Funktionsverwaltung** aktivieren und dann auf der Registerkarte **ATP Einstellung** festlegen. Weitere Informationen finden Sie unter [Inventory Visibility - Lagerbestände, Änderungszeitpläne und Zusagen](inventory-visibility-available-to-promise.md).

## <a name="complete-and-update-the-configuration"></a>Abschließen und Aktualisieren der Konfiguration

Nachdem Sie die Konfiguration abgeschlossen haben, müssen Sie alle Änderungen an Inventory Visibility festschreiben. Um die Änderungen zu bestätigen, wählen Sie **Konfiguration aktualisieren** in der oberen rechten Ecke der Seite **Konfiguration** in Power Apps.

Wenn Sie zum ersten Mal **Konfiguration aktualisieren** wählen, fordert das System Ihre Anmeldeinformationen an.

- **Client Id** - Die Azure-Anwendungs-ID, die Sie für Inventory Visibility erstellt haben.
- **Mandanten-ID** - Ihre Azure-Mandanten-ID.
- **Client Secret** - Das Azure-Anwendungsgeheimnis, das Sie für Inventory Visibility erstellt haben.

Nachdem Sie sich angemeldet haben, wird die Konfiguration im Inventory Visibility-Dienst aktualisiert.

> [!NOTE]
> Stellen Sie sicher, dass Sie den Namen der Datenquelle, die physikalischen Messungen und die Zuordnungen der Dimensionen überprüfen, bevor Sie die Konfiguration für den Inventory Visibility-Dienst aktualisieren. Sie können diese Einstellungen nicht mehr ändern, nachdem Sie **Konfiguration aktualisieren** gewählt haben.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Standardkonfigurationsbeispiel

Die Bestandsanzeige legt bei der Initialisierung eine Standardkonfiguration fest, die hier angegeben ist. Sie können diese Konfiguration nach Bedarf ändern.

### <a name="data-source-configuration"></a>Konfiguration der Datenquelle

#### <a name="configuration-of-the-iv-data-source"></a>Konfiguration der iv-Datenquelle

Dieser Abschnitt beschreibt, wie die Datenquelle `iv` konfiguriert wird.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Konfigurierte physikalische Messungen für die iv-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `iv` konfiguriert:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal berechnete Messung

Die berechnete Kennzahl `OrderedTotal` wird für die Datenquelle `iv` wie in der folgenden Tabelle gezeigt konfiguriert.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>OnHand berechnete Messung

Die berechnete Messung `OnHand` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>ReserviertGesamt berechnete Messung

Die berechnete Messung `ReservedTotal` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>SoftReserved berechnete Messung

Die berechnete Messung `SoftReserved` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>HardReserved berechnete Messung

Die `HardReserved` berechnete Messung ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle gezeigt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>OpenOrder berechnete Messung

Die berechnete Messung `OpenOrder` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `OnOrder` |
| Addition | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>OnHandAvailable berechnete Messung

Die berechnete Messung `OnHandAvailable` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `fno` | `ReservPhysical` |
| Subtraktion | `iv` | `SoftReservPhysical` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>AvailableToReserve berechnete Messung

Die berechnete Messung `AvailableToReserve` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |
| Subtraktion | `fno` | `ReservPhysical` |
| Subtraktion | `fno` | `ReservOrdered` |
| Subtraktion | `iv` | `SoftReservPhysical` |
| Subtraktion | `iv` | `SoftReservOrdered` |
| Subtraktion | `iv` | `ReservPhysical` |
| Subtraktion | `iv` | `ReservOrdered` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>InventorySupply berechnete Messung

Die berechnete Messung `InventorySupply` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>InventoryDemand berechnete Kennzahl

Die berechnete Messung `InventoryDemand` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `OnOrder` |
| Addition | `iom` | `OnOrder` |
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |
| Hinzufügung | `fno` | `ReservPhysical` |
| Hinzufügung | `fno` | `ReservOrdered` |
| Hinzufügung | `iv` | `ReservPhysical` |
| Hinzufügung | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Konfiguration der Datenquelle fno

Dieser Abschnitt beschreibt, wie die Datenquelle `fno` konfiguriert wird.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensionen-Zuordnungen für die fno-Datenquelle

Für die Datenquelle `fno` sind die Dimensionen-Zuordnungen konfiguriert, die in der folgenden Tabelle aufgeführt sind.

| Externe Dimension | Basis-Dimensionen |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Für die Datenquelle "fno" konfigurierte physikalische Messungen

Die folgenden physikalischen Messungen sind für die Datenquelle `fno` konfiguriert:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Konfiguration der pos-Datenquelle

Dieser Abschnitt beschreibt, wie die Datenquelle `pos` konfiguriert ist.

##### <a name="physical-measures-for-the-pos-data-source"></a>Physikalische Messungen für die pos-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `pos` konfiguriert:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity berechnete Messung

Die berechnete Kennzahl `AvailQuantity` wird für die Datenquelle `pos` wie in der folgenden Tabelle gezeigt konfiguriert.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Hinzufügung | `fno` | `AvailPhysical` |
| Hinzufügung | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Konfiguration der iom-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `iom` (intelligente Auftragsverwaltung) konfiguriert:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Konfiguration der erp-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `erp` (Enterprise Resource Planning) konfiguriert:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Partitionskonfiguration

Die folgende Tabelle zeigt die Standard-Partitionskonfiguration.

| Basis-Dimension | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Index-Konfiguration

Die folgende Tabelle zeigt die Standard-Indexkonfiguration.

| Nummer festlegen | Dimensionen | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Reservierungs-Konfiguration

Dieser Abschnitt beschreibt die standardmäßige Reservierungskonfiguration.

#### <a name="reservation-mapping"></a>Zuordnung der Reservierung

Die folgende Tabelle zeigt die standardmäßige Zuordnung von Reservierungen.

| Datenquelle für physikalische Messungen | Physikalische Messung | Verfügbar für Reservierungsdatenquelle | Verfügbar für die berechnete Messung der Reservierung |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reservierungshierarchie

Die folgende Tabelle zeigt die Standard-Reservierungshierarchie.

| Basis-Dimension | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

