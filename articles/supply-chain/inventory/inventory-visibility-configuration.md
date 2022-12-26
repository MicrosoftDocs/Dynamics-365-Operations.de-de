---
title: Inventory Visibility konfigurieren
description: In diesem Artikel wird beschrieben, wie Sie Inventory Visibility konfigurieren.
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
ms.openlocfilehash: 2a368535c9644e174d1a2460ac0891c9dc1b1b3f
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850022"
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
- [Vorabladen-Konfiguration des Index (optional)](#query-preload-configuration)
- [Beispiel für die Standardkonfiguration](#default-configuration-sample)

## <a name="prerequisites"></a>Erforderliche Komponenten

Bevor Sie beginnen, installieren Sie das Bestandsanzeige-Add-In und richten es wie in [Bestandsanzeige installieren und einrichten](inventory-visibility-setup.md) beschrieben ein.

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Die Konfigurationsseite der Bestandsanzeige-App

In Power Apps hilft Ihnen die Seite **Konfiguration** der [Bestandsanzeige-App](inventory-visibility-power-platform.md) beim Festlegen der Konfiguration des Lagerbestands und der Softreservierung. Nach der Installation des Add-Ins enthält die Standardkonfiguration den Wert von Microsoft Dynamics 365 Supply Chain Management (die Datenquelle `fno`). Sie können die Standardeinstellungen überprüfen. Zusätzlich können Sie die Konfiguration basierend auf Ihren geschäftlichen Anforderungen und den Bestandsbuchungsanforderungen Ihres externen Systems ändern, um die Art und Weise zu standardisieren, in der Bestandsänderungen in verschiedenen Systemen gebucht, organisiert und abgefragt werden können. In den verbleibenden Abschnitten des Artikels wird erläutert, wie die einzelnen Teile der Seite **Konfiguration** zu verwenden sind.

Nachdem die Konfiguration abgeschlossen ist, wählen Sie in der App unbedingt **Konfiguration aktualisieren** aus.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Aktivieren Sie die Bestandsanzeigefunktionen in der Funktionsverwaltung von Power Apps

Das Bestandsanzeige-Add-In fügt Ihrer Power Apps-Installation mehrere neue Funktionen hinzu. Standardmäßig sind diese Funktionen ausgeschaltet. Um sie zu verwenden, öffnen Sie die Seite **Konfiguration** und schalten Sie dann auf der Registerkarte **Funktionsverwaltung** die folgenden Funktionen nach Bedarf ein.

| Name der Funktionsverwaltung | Description |
|---|---|
| *OnHandReservation* | Mit dieser Funktion können Sie mithilfe von Inventory Visibility Reservierungen erstellen, Reservierungen verbrauchen und/oder bestimmte Bestandsmengen aufheben. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Diese Funktion bietet eine Bestandsübersicht für Produkte zusammen mit allen Dimensionen. Die Bestandsübersicht wird regelmäßig von der Bestandsanzeige synchronisiert. Die standardmäßige Synchronisierungshäufigkeit ist einmal alle 15 Minuten und kann auf bis zu einmal alle 5 Minuten eingestellt werden. Weitere Informationen finden Sie unter [Bestandsübersicht](inventory-visibility-power-platform.md#inventory-summary). |
| *OnHandIndexQueryPreloadBackgroundService* | Diese Funktion ruft und speichert regelmäßig eine Reihe von Bestandsübersichtsdaten basierend auf Ihren vorkonfigurierten Dimensionen. Es bietet eine Bestandsübersicht, die nur die Dimensionen enthält, die für Ihr Tagesgeschäft relevant sind, und die mit Artikeln kompatibel ist, die für Lagerverwaltungsprozesse (WMS) aktiviert sind. Weitere Informationen finden Sie unter [Aktivieren und Konfigurieren vorab geladener verfügbarer Abfragen](#query-preload-configuration) und [Vorabladen einer optimierten verfügbaren Abfrage](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *OnhandChangeSchedule* | Die optionale Funktion aktiviert die Funktionen Lagerbestandsänderung und Available to Promise (ATP). Weitere Informationen finden Sie unter [Inventory Visibility: verfügbarer Änderungszeitplan und verfügbar für Zusage](inventory-visibility-available-to-promise.md). |
| *Zuweisung* | Diese optionale Funktion ermöglicht Inventory Visibility, Inventarschutz (Ringfencing) und Überverkaufskontrolle zu bieten. Weitere Informationen finden Sie unter [Bestandszuordnung für Bestandsichtbarkeit](inventory-visibility-allocation.md) |
| *Lagerortartikel in Bestandsanzeige aktivieren* | Diese optionale Funktion ermöglicht Inventory Visibility, um Artikel zu unterstützen, die für Prozesse der Lagerverwaltung (WMS) aktiviert sind. Weitere Informationen finden Sie unter [Inventory Visibility-Unterstützung für WMS-Artikel](inventory-visibility-whs-support.md). |

> [!IMPORTANT]
> Wir empfehlen, dass Sie entweder die Funktion *OnHandIndexQueryPreloadBackgroundService* oder die Funktion *OnHandMostSpecificBackgroundService* verwenden, nicht beide. Die Aktivierung beider Funktionen wirkt sich auf die Leistung aus.

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finden Sie den Dienst-Endpunkt

Wenn Sie den richtigen Dienst-Endpunkt für Inventory Visibility nicht kennen, öffnen Sie die Seite **Konfiguration** in Power Apps und wählen Sie dann **Dienstdetails anzeigen** in der oberen rechten Ecke. Die Seite zeigt den korrekten Dienst-Endpunkt an. Sie finden den Endpunkt auch in Microsoft Dynamics Lifecycle Services, wie in [Suchen Sie den Endpunkt entsprechend Ihrer Lifecycle Services-Umgebung](inventory-visibility-api.md#endpoint-lcs) beschrieben.

> [!NOTE]
> Die Verwendung eines falschen Endpunkts kann zu einer fehlgeschlagenen Installation von Bestandsanzeige und zu Fehlern führen, wenn Supply Chain Management mit Bestandsanzeige synchronisiert wird. Wenn Sie sich nicht sicher sind, was Ihr Endpunkt ist, wenden Sie sich an Ihren Systemadministrator. Endpunkt-URLs verwenden das folgende Format:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Datenquellenkonfiguration

Jede Datenquelle steht für ein System, aus dem Ihre Daten stammen. Beispiele für Datenquellennamen sind `fno` (was Supply Chain Management entspricht) und `pos` (steht für Verkaufsquelle). Standardmäßig ist das Supply Chain Management als Standard-Datenquelle (`fno`) in Inventory Visibility festgelegt.

> [!NOTE]
> Die Datenquelle `fno` ist für das Supply Chain Management reserviert. Wenn Ihr Bestandsanzeige-Add-In mit einer Supply Chain Management Umgebung integriert ist, empfehlen wir Ihnen, keine Konfigurationen zu löschen, die mit `fno` in der Datenquelle verbunden sind.

Um eine Datenquelle hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der **Datenquelle** Registerkarte **Neue Datenquelle**, um eine Datenquelle hinzuzufügen (z. B. `ecommerce` oder eine andere aussagekräftige Datenquellen-ID).

> [!NOTE]
> Wenn Sie eine Datenquelle hinzufügen, stellen Sie sicher, dass Sie den Namen der Datenquelle, die physikalischen Kennzahlen und die Zuordnungen der Dimensionen überprüfen, bevor Sie die Konfiguration für den Dienst "Inventory Visibility" aktualisieren. Sie können diese Einstellungen nicht mehr ändern, nachdem Sie **Konfiguration aktualisieren** gewählt haben.

Die Datenquellenkonfiguration umfasst die folgenden Teile:

- Dimensionen (Zuordnung von Dimensionen)
- Physikalische Messungen
- Berechnete Messungen

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensionen (Zuordnung von Dimensionen)

Der Zweck der Dimensionskonfiguration ist die Standardisierung der Multisystem-Integration für Buchungsereignisse und Abfragen, basierend auf Dimensionskombinationen. Inventory Visibility bietet eine Liste von Basisdimensionen, die den Dimensionen Ihrer Datenquelle zugeordnet werden können. Dreiunddreißig Dimensionen sind für die Zuordnung verfügbar.

- Wenn Sie Supply Chain Management als eine Ihrer Datenquellen verwenden, werden 13 Dimensionen bereits den Supply Chain Management Standarddimensionen standardmäßig zugeordnet. Die anderen 12 Dimensionen (`inventDimension1` bis `inventDimension12`) sind ebenfalls angepassten Dimensionen im Supply Chain Management zugeordnet. Die restlichen acht Dimensionen (`ExtendedDimension1` durch `ExtendedDimension8`) sind erweiterte Dimensionen, die Sie externen Datenquellen zuordnen können.
- Wenn Sie Supply Chain Management nicht als eine Ihrer Datenquellen verwenden, können Sie die Dimensionen frei zuordnen. Die folgende Tabelle zeigt die vollständige Liste der verfügbaren Dimensionen.

> [!NOTE]
> Wenn Sie Supply Chain Management verwenden und die standardmäßigen Dimensionszuordnungen zwischen Supply Chain Management und Bestandsanzeige ändern, werden die geänderten Dimensionen keine Daten synchronisieren. Wenn Ihre Dimension daher nicht auf der Liste der Standarddimensionen enthalten ist und Sie eine externe Datenquelle verwenden, empfehlen wir Ihnen, die Zuordnung mit `ExtendedDimension1` bis `ExtendedDimension8` vorzunehmen.

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
> Die Dimensionen, die in der vorangehenden Tabelle aufgeführt sind, dienen nur für Sie als Referenz. Sie müssen sie nicht in Inventory Visibility definieren.
>
> (Angepasste) Bestandsdimensionen für den Bestand können für das Supply Chain Management reserviert sein. In diesem Fall verwenden Sie stattdessen die erweiterten Dimensionen.

Externe Systeme können über die RESTful-APIs von Inventory Visibility zugreifen. Für die Integration können Sie in Inventory Visibility die *externe Datenquelle* und die Zuordnung von den *externen Dimensionen* zu den *Basisdimensionen* konfigurieren. Hier ist ein Beispiel für eine Tabelle zur Zuordnung von Dimensionen.

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
1. Wählen Sie auf der Registerkarte **Datenquelle** die Datenquelle aus, in der Sie die Dimensionszuordnung durchführen möchten. Wählen Sie im Abschnitt **Dimensions-Zuordnungen** die Option **Hinzufügen**, um Dimensions-Zuordnungen hinzuzufügen.

    ![Hinzufügen von Zuordnungen von Dimensionen](media/inventory-visibility-dimension-mapping.png "Hinzufügen von Zuordnungen von Dimensionen")

1. Geben Sie im Feld **Dimensionsname** die Quelldimension an.
1. Wählen Sie im Feld **Zur Basisdimension** die Dimension in Inventory Visibility, die Sie zuordnen möchten.
1. Wählen Sie **Speichern** aus.

Beispielsweise haben Sie bereits eine Datenquelle mit dem Namen `ecommerce` erstellt, und es enthält eine Produktfarbdimension. In diesem Fall können Sie für die Zuordnung zuerst `ProductColor` zum **Dimensionsname** Feld in der `ecommerce` Datenquelle hinzufügen und dann `ColorId` im Feld **Zur Basisdimension** auswählen.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Physikalische Messungen

Wenn eine Datenquelle eine Bestandsänderung an Inventory Visibility sendet, sendet sie diese Änderung unter Verwendung von *physikalischen Messungen*. Physikalische Messungen verändern die Menge und spiegeln den Status des Bestands wider. Sie können Ihre eigenen physikalischen Messungen, basierend auf Ihren Anforderungen, definieren. Abfragen können auf den physikalischen Kennzahlen basieren.

Inventory Visibility bietet eine Liste von standardmäßigen physikalischen Messungen, die Supply Chain Management (der Datenquelle `fno`) zugeordnet sind. Diese voreingestellten physikalischen Kennzahlen werden aus den Status der Transaktionen im Lagerbestand auf der Seite **Bestandsliste** im Supply Chain Management (**Lagerverwaltung \> Abfragen und Bericht \> Bestandsliste**) übernommen. Die folgende Tabelle enthält ein Beispiel für physikalische Messungen.

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
| `Received` | Erhalten |
| `Registered` | Erfasst |
| `ReservOrdered` | Bestellt reserviert |
| `ReservPhysical` | Physisch reserviert |

Wenn die Datenquelle Supply Chain Management ist, müssen Sie die standardmäßigen physikalischen Messungen nicht neu erstellen. Für externe Datenquellen können Sie jedoch neue physikalische Messungen erstellen, indem Sie die folgenden Schritte ausführen.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Datenquelle** die Datenquelle aus, der physische Maße hinzugefügt werden sollen (z. B. die `ecommerce` Datenquelle). Wählen Sie dann im **Physikalische Maßnahmen** Abschnitt **Hinzufügen**, und geben Sie den Measure-Namen an (z. B. `Returned` wenn Sie zurückgegebene Mengen in dieser Datenquelle in Bestandsanzeige erfassen möchten). Speichern Sie die Änderungen.

### <a name="extended-dimensions"></a>Erweiterte Dimensionen

Kunden, die externe Datenquellen in der Datenquelle verwenden möchten, können die Vorteile der Erweiterbarkeit nutzen, die Dynamics 365 bietet, indem sie [Klassenerweiterungen](../../fin-ops-core/dev-itpro/extensibility/class-extensions.md) für die `InventOnHandChangeEventDimensionSet` und erstellen `InventInventoryDataServiceBatchJobTask` Klassen.

Stellen Sie sicher, dass Sie nach dem Erstellen der Erweiterungen mit der Datenbank synchronisieren, damit die benutzerdefinierten Felder der Tabelle `InventSum` hinzugefügt werden. Sie können dann den Abschnitt Dimensionen weiter oben in diesem Artikel lesen, um Ihre benutzerdefinierten Dimensionen einer der acht erweiterten Dimensionen in `BaseDimensions` im Inventar zuzuordnen.

> [!NOTE] 
> Weitere Einzelheiten zum Erstellen von Erweiterungen finden Sie auf der [Erweiterbarkeits-Startseite](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

### <a name="calculated-measures"></a>Berechnete Messungen

Sie können Inventory Visibility verwenden, um sowohl physische Messungen im Bestand als auch *angepasste berechnete Kennzahlen* abzufragen. Berechnete Maße bieten eine angepasste Berechnungsformel, die aus einer Kombination von physikalischen Messungen besteht. Mit dieser Funktionalität können Sie eine Reihe von physikalischen Kennzahlen festlegen, die addiert werden, und/oder eine Reihe von physikalischen Kennzahlen, die subtrahiert werden, um das Formular für die angepasste Messung zu bilden.

> [!IMPORTANT]
> Ein berechnetes Measure ist eine Zusammenstellung von physikalischen Measures. Seine Formel kann nur physikalische Measures ohne Duplikate enthalten, keine berechneten Measures.

In der Konfiguration können Sie eine Reihe von berechneten Measure-Formeln definieren, die Modifikatoren von Addition und Subtraktion umfassen, um die gesamte aggregierte Ausgabemenge zu erhalten.

Um eine angepasste berechnete Messung festzulegen, befolgen Sie diese Schritte.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Auf der Registerkarte **Berechnete Messung** wählen Sie **Neue berechnete Messung**, um eine berechnete Messung hinzuzufügen.
1. Legen Sie die folgenden Felder für die neue berechnete Messung fest:

    - **Neuer Name der berechneten Messung** - Geben Sie den Namen der berechneten Messung ein.
    - **Datenquelle** - Wählen Sie die Datenquelle, die die neue berechnete Measure umfassen soll. Das abfragende System ist eine Datenquelle.

1. Wählen Sie **Hinzufügen**, um der neu berechneten Messung einen Modifikator hinzuzufügen.
1. Legen Sie die folgenden Felder für den neuen Modifikator fest:

    - **Modifikator** - Wählen Sie den Modifikatortyp (*Zugabe* oder *Subtraktion*).
    - **Datenquelle** - Wählen Sie die Datenquelle aus, in der die Messung, die den Modifikatorwert liefert, gefunden werden soll.
    - **Messung** - Wählen Sie den Namen der Messung (aus der ausgewählten Datenquelle), die den Wert für den Modifikator liefert.

1. Wiederholen Sie die Schritte 5 bis 6, bis Sie alle erforderlichen Modifikatoren und hinzugefügt haben und die Formel für Ihre berechnete Measure abgeschlossen haben.
1. Wählen Sie **Speichern** aus.

Beispielsweise arbeitet ein Modeunternehmen mit drei Datenquellen:

- `pos` – Entspricht dem Shopkanal.
- `fno` – Entspricht Supply Chain Management.
- `ecommerce`– Entspricht Ihrem Webkanal.

Ohne berechnete Kennzahlen, wenn Sie Produkt D0002 (Kabine) unter Standort 1, Lager 11 und einen `ColorID` Dimensionswert von `Red` abfragen, erhalten Sie möglicherweise das folgende Abfrageergebnis, das Bestandsmengen unter jeder vorkonfigurierten physischen Maßeinheit anzeigt. Sie haben jedoch keinen Einblick in die insgesamt für Reservierungen verfügbaren Mengen in Ihren Datenquellen.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Wenn diese Berechnungsformel verwendet wird, wird das neue Abfrageergebnis die angepasste Messung enthalten.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
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

Inventory Visibility bietet Flexibilität, indem Sie die *Indizes* festlegen können, um die Leistung Ihrer Abfragen zu verbessern. Diese Indizes basieren auf einer Dimension oder einer Kombination von Dimensionen. Ein Index besteht aus einer *Satznummer*, einer *Dimension* und einer *Hierarchie*, wie in der folgenden Tabelle festgelegt.

| Name | Beschreibung |
|---|---|
| Set-Nummer festlegen | Dimensionen, die zum gleichen Set (Index) gehören, werden gruppiert, und ihnen wird die gleiche Set-Nummer zugewiesen. |
| Dimensionen | Basisdimensionen, über die das Abfrageergebnis aggregiert wird. |
| Hierarchie | Mithilfe der Hierarchie können Sie die Leistung bestimmter Dimensionskombinationen steigern, wenn sie in „Filtern nach“ und „Gruppieren nach“-Abfrageparametern verwendet werden. Wenn Sie beispielsweise einen Dimensionssatz mit einer Hierarchiesequenz von `(ColorId, SizeId, StyleId)` einrichten, kann das System Abfragen in Bezug auf vier Dimensionskombinationen schneller verarbeiten. Die erste Kombination ist leer, die zweite ist `(ColorId)`, die dritte ist `(ColorId, SizeId)` und die vierte ist `(ColorId, SizeId, StyleId)`. Andere Kombinationen werden nicht beschleunigt. Filter sind nicht durch die Reihenfolge eingeschränkt, müssen jedoch innerhalb dieser Dimensionen liegen, wenn Sie ihre Leistung verbessern möchten. Weitere Informationen finden Sie im folgenden Beispiel. |

Um Ihren Produkthierarchie-Index festzulegen, gehen Sie wie folgt vor.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Produkthierarchie-Index** im Abschnitt **Dimensions-Zuordnungen** die Option **Hinzufügen**, um Zuordnungen von Dimensionen hinzuzufügen.
1. Standardmäßig wird eine Liste von Indizes bereitgestellt. Um einen vorhandenen Index zu ändern, wählen Sie **Bearbeiten** oder **Hinzufügen** im Abschnitt für den betreffenden Index. Um einen neuen Indexsatz zu erstellen, wählen Sie **Neuer Indexsatz**. Wählen Sie für jede Zeile in jedem Indexsatz im Feld **Dimension** aus der Liste der Basisdimensionen aus. Die Werte für die folgenden Felder werden automatisch generiert:

    - **Set-Nummer** - Dimensionen, die zur gleichen Gruppe (Index) gehören, werden zusammen gruppiert, und ihnen wird die gleiche Set-Nummer zugewiesen.
    - **Hierarchie**: Die Hierarchie steigert die Leistung bestimmter Dimensionskombinationen, wenn sie in „Filtern nach“ und „Gruppieren nach“-Abfrageparametern verwendet werden.

> [!TIP]
> Hier sind ein paar Tipps, die Sie beim Einrichten Ihrer Indexhierarchie beachten sollten:
>
> - Basisdimensionen, die in der Partitionskonfiguration definiert sind, sollten nicht in Indexkonfigurationen definiert werden. Wenn in der Indexkonfiguration erneut eine Basisdimension definiert wird, können Sie nicht nach diesem Index abfragen.
> - Wenn Sie nur Bestand abfragen müssen, der durch alle Dimensionskombinationen aggregiert wird, können Sie einen einzelnen Index einrichten, der die Basisdimension `Empty` enthält.

### <a name="example"></a>Beispiel

In diesem Abschnitt finden Sie ein Beispiel, das zeigt, wie die Hierarchie funktioniert.

Die folgende Tabelle zeigt eine Liste der verfügbaren Bestände für dieses Beispiel.

| Element | ColorId | SizeId | StyleId | Menge |
|---|---|---|---|---|
| D0002 | Schwarz | Klein | Breit | 1 |
| D0002 | Schwarz | Klein | Normal | 2 |
| D0002 | Schwarz | Groß | Breit | 3 |
| D0002 | Schwarz | Groß | Normal | 4 |
| D0002 | Rot | Klein | Breit | 5 |
| D0002 | Rot | Klein | Normal | 6 |
| D0002 | Rot | Groß | Normal | 7 |

Die folgende Tabelle zeigt, wie die Indexhierarchie festgelegt wird.

| Nummer festlegen | Dimensionen | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Mit dem Index können Sie den Lagerbestand auf die folgenden Arten abfragen:

- `()` - gruppiert nach allen

    - D0002, 28

- `(ColorId)` - gruppiert nach `ColorId`

    - D0002, Schwarz, 10
    - D0002, Rot, 18

- `(ColorId, SizeId)` - gruppiert nach der Kombination von `ColorId` und `SizeId`

    - D0002, Schwarz, Small, 3
    - D0002, Schwarz, Large, 7
    - D0002, Rot, Small, 11
    - D0002, Rot, Large, 7

- `(ColorId, SizeId, StyleId)` - gruppiert nach der Kombination von `ColorId`, `SizeId` und `StyleId`

    - D0002, Schwarz, Small, Wide, 1
    - D0002, Schwarz, Small, Regular, 2
    - D0002, Schwarz, Large, Wide, 3
    - D0002, Schwarz, Large, Regular, 4
    - D0002, Rot, Small, Wide, 5
    - D0002, Rot, Small, Regular, 6
    - D0002, Rot, Large, Regular, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Reservierungskonfiguration (optional)

Die Reservierungskonfiguration ist erforderlich, wenn Sie die Funktion der Soft-Reservierung verwenden möchten. Die Konfiguration besteht aus zwei grundlegenden Teilen:

- Soft-Reservierungs-Zuordnung
- Soft-Reservierungs-Hierarchie

### <a name="soft-reservation-mapping"></a>Zuordnung der Soft-Reservierung

Wenn Sie eine Reservierung vornehmen, möchten Sie vielleicht wissen, ob der Lagerbestand aktuell für die Reservierung verfügbar ist. Die Validierung ist mit einer berechneten Messung verknüpft, die eine Berechnungsformel aus einer Kombination von physikalischen Messungen darstellt.

Indem Sie die Zuordnung von der physikalischen Messung zur berechneten Messung festlegen, ermöglichen Sie dem Dienst Inventory Visibility, die Verfügbarkeit von Reservierungen automatisch zu überprüfen, basierend auf der physikalischen Messung.

Bevor Sie diese Zuordnung festlegen, müssen die physikalischen Messungen, die berechneten Messungen und ihre Datenquellen auf den Registerkarten **Datenquelle** und **Berechnete Messung** der Seite **Konfiguration** in Power Apps definiert werden (wie zuvor in diesem Artikel beschrieben).

Um die Zuordnung der Soft-Reservierung zu definieren, gehen Sie wie folgt vor.

1. Definieren Sie die physikalische Kennzahl, die als Soft-Reservierungsmaßnahme dient (zum Beispiel `SoftReservPhysical`).
1. Definieren Sie auf der Registerkarte **Berechnete Kennzahl** der Seite **Konfiguration** die *zur Reservierung verfügbare* (AFR) berechnete Kennzahl, die die AFR-Berechnungsformel enthält, die Sie der physikalischen Messung zuordnen möchten. Sie könnten z.B. `AvailableToReserve` (verfügbar für Reservierung) so festlegen, dass sie der zuvor definierten physikalischen Messung `SoftReservPhysical` zugeordnet wird. Auf diese Weise können Sie feststellen, welche Mengen, die den Bestandsstatus `SoftReservPhysical` haben, für die Reservierung verfügbar sind. Die folgende Tabelle zeigt die AFR-Berechnungsformel.

    | Berechnungstyp | Datenquelle | Physikalische Messung |
    |---|---|---|
    | Addition | `fno` | `AvailPhysical` |
    | Addition | `pos` | `Inbound` |
    | Subtraktion | `pos` | `Outbound` |
    | Subtraktion | `iv` | `SoftReservPhysical` |

    Wir empfehlen, die berechnete Messung so einzurichten, dass sie die physikalische Messung enthält, auf der die Reservierungsmessung basiert. Auf diese Weise wird die berechnete Messungsmenge durch die Reservierungsmessungsmenge beeinflusst. Daher sollte in diesem Beispiel die für `AvailableToReserve` berechnete Messung der `iv`-Datenquelle die physikalische Messung für `SoftReservPhysical` aus `iv` als Komponente enthalten.

1. Öffnen Sie die Seite **Konfiguration**.
1. Legen Sie auf der Registerkarte **Zuordnung von Soft-Reservierungen** die Zuordnung von der physischen Messung zur berechneten Kennzahl fest. Für das vorherige Beispiel könnten Sie die folgenden Einstellungen verwenden, um `AvailableToReserve` der zuvor definierten physikalischen Messung `SoftReservPhysical` zuzuordnen.

    | Datenquelle für physikalische Messungen | Physikalische Messung | Verfügbar für Reservierungsdatenquelle | Verfügbar für die berechnete Messung der Reservierung |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Wenn Sie die **Zuordnung von Soft-Reservierungen** nicht bearbeiten können, müssen Sie eventuell die Funktion *OnHandReservation* auf der Registerkarte **Funktionsverwaltung** einschalten.

Wenn Sie nun eine Reservierung für `SoftReservPhysical` vornehmen, findet Inventory Visibility automatisch `AvailableToReserve` und die zugehörige Berechnungsformel, um die Reservierungsvalidierung durchzuführen.

Sie haben z. B. den folgenden Lagerbestand in Inventory Visibility.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Wenn Sie also versuchen, eine Reservierung für `iv.SoftReservPhysical` vorzunehmen, und die Menge kleiner oder gleich `AvailableToReserve` (10) ist, ist die Soft-Reservierungsanfrage erfolgreich.

> [!NOTE]
> Wenn Sie die Reservierungs-API aufrufen, können Sie die Reservierungsvalidierung steuern, indem Sie den booleschen `ifCheckAvailForReserv`-Parameter im Anforderungstext angeben. Ein Wert von `True` bedeutet, dass die Validierung erforderlich ist, während ein Wert von `False` bedeutet, dass die Validierung nicht erforderlich ist (obwohl Sie am Ende möglicherweise eine negative `AvailableToReserve` Menge erhalten, erlaubt Ihnen das System immer noch eine Soft-Reservierung). Der Standardwert ist `True`.

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

## <a name="turn-on-and-configure-preloaded-on-hand-queries-optional"></a><a name="query-preload-configuration"></a>Vorgeladene Bestandsanfragen aktivieren und konfigurieren (optional)

Bestandsanzeige ruft und speichert regelmäßig eine Reihe von Bestandsübersichtsdaten basierend auf Ihren vorkonfigurierten Dimensionen. Dies bietet folgende Vorteile:

- Eine übersichtlichere Ansicht, die eine Bestandsübersicht speichert, die nur die Dimensionen enthält, die für Ihr Tagesgeschäft relevant sind.
- Eine Bestandsübersicht, die mit Artikeln kompatibel ist, die für Lagerverwaltungsprozesse (WMS) aktiviert sind.

Siehe [Vorladen einer rationalisierten Abfrage des Lagerbestands](inventory-visibility-power-platform.md#preload-streamlined-onhand-query) für weitere Informationen zum Arbeiten mit dieser Funktion nach der Einrichtung

> [!IMPORTANT]
> Wir empfehlen, dass Sie entweder die Funktion *OnHandIndexQueryPreloadBackgroundService* oder die Funktion *OnHandMostSpecificBackgroundService* verwenden, nicht beide. Die Aktivierung beider Funktionen wirkt sich auf die Leistung aus.

Um diese Funktion einzurichten, führen Sie folgende Schritte aus.

1. Melden Sie sich bei der Bestandsanzeige-Power App an.
1. Gehen Sie zu **Konfiguration \> Funktionsverwaltung und Einstellungen**.
1. Wenn die Funktion *OnHandIndexQueryPreloadBackgroundService* bereits aktiviert ist, empfehlen wir, sie vorerst zu deaktivieren, da der Bereinigungsprozess sehr lange dauern kann. Sie aktivieren sie später in diesem Verfahren erneut.
1. Öffnen Sie die Registerkarte **Preload-Einstellung** .
1. Wählen Sie im Abschnitt **Schritt 1: Preload-Speicher bereinigen** die Option **Bereinigen** aus, um die Datenbank zu bereinigen und bereit zu machen, um Ihre neuen Gruppieren-nach-Einstellungen zu akzeptieren.
1. Geben Sie im Abschnitt **Schritt 2: Gruppieren nach-Werten einrichten** im Feld **Ergebnis gruppieren nach** ein Komma ein -getrennte Liste von Feldnamen, nach denen Sie Ihre Abfrageergebnisse gruppieren können. Sobald Sie Daten in der Preload-Speicherdatenbank haben, können Sie diese Einstellung erst ändern, wenn Sie die Datenbank wie im vorherigen Schritt beschrieben bereinigen.
1. Gehen Sie zu **Konfiguration \> Funktionsverwaltung und Einstellungen**.
1. Aktivieren Sie die Funktion *OnHandIndexQueryPreloadBackgroundService*.
1. Wählen Sie **UKonfiguration aktualisieren** in der oberen rechten Ecke der Seite **Konfiguration**, um die Änderungen zu bestätigen

## <a name="complete-and-update-the-configuration"></a>Abschließen und Aktualisieren der Konfiguration

Nachdem Sie die Konfiguration abgeschlossen haben, müssen Sie alle Änderungen an Inventory Visibility festschreiben. Befolgen Sie diese Schritte, um Ihre Änderungen zu speichern.

1. Wählen Sie in Power Apps auf der **Konfiguration** Seite **Update-Konfiguration** in der oberen rechten Ecke. 
1. Das System fordert Anmeldeinformationen an. Geben Sie die folgenden Werte ein:

    - **Client Id** - Die Azure-Anwendungs-ID, die Sie für Inventory Visibility erstellt haben.
    - **Mandanten-ID** - Ihre Azure-Mandanten-ID.
    - **Client Secret** - Das Azure-Anwendungsgeheimnis, das Sie für Inventory Visibility erstellt haben.

    Weitere Informationen zu diesen Anmeldeinformationen und wie Sie sie finden, finden Sie unter [Installieren und Einrichten des Bestandsanzeige Add-Ins](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Stellen Sie sicher, dass Sie den Namen der Datenquelle, die physikalischen Messungen und die Zuordnungen der Dimensionen überprüfen, bevor Sie die Konfiguration aktualisieren. Sie können diese Einstellungen nicht mehr ändern, nachdem Sie sie aktualisiert haben.

1. Wählen Sie nach der Anmeldung erneut **Konfiguration aktualisieren** aus. Das System übernimmt Ihre Einstellungen und zeigt die Änderungen an.

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

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

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
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reservierungshierarchie

Die folgende Tabelle zeigt die Standard-Reservierungshierarchie.

| Basis-Dimensionen | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
