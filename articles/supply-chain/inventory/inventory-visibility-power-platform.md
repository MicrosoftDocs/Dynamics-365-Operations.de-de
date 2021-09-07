---
title: Inventory Visibility App
description: Dieses Thema beschreibt die Verwendung der Inventory Visibility App.
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
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345001"
---
# <a name="inventory-visibility-app"></a>Inventory Visibility App

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dieses Thema beschreibt die Verwendung der Inventory Visibility App.

Inventory Visibility bietet eine modellbasierte App zur Visualisierung. Die App enthält drei Seiten: **Konfiguration**, **Betriebliche Sichtbarkeit** und **Inventarübersicht**. Sie hat die folgenden Funktionen:

- Es bietet eine Benutzeroberfläche (UI) für die Konfiguration des Lagerbestands und der Softreservierung.
- Es unterstützt Echtzeit-Abfragen des Lagerbestands für verschiedene Dimensionen-Kombinationen.
- Es bietet eine Benutzeroberfläche für die Buchung von Reservierungsanfragen.
- Es bietet eine angepasste Ansicht des Lagerbestands für Produkte zusammen mit allen Dimensionen

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, installieren Sie das Bestandssichtbarkeits-Add-In und legen es fest, wie in [Bestandssichtbarkeit einrichten](inventory-visibility-setup.md) beschrieben.

## <a name="configuration"></a><a name="configuration"></a>Variante

Die Seite **Konfiguration** hilft Ihnen, die Konfiguration des Lagerbestands und der Softreservierung festzulegen. Nach der Installation des Add-Ins enthält die Standardkonfiguration den Wert von Microsoft Dynamics 365 Supply Chain Management (die Datenquelle `fno`). Sie können die Standardeinstellung überprüfen. Zusätzlich können Sie die Konfiguration in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) basierend auf Ihren geschäftlichen Anforderungen und den Bestandsbuchungsanforderungen Ihres externen Systems ändern, um die Art und Weise zu standardisieren, in der Bestandsänderungen in den verschiedenen Systemen gebucht, organisiert und abgefragt werden können.

### <a name="define-data-sources"></a>Definieren von Datenquellen

Sie definieren jede *Datenquelle*, die Sie mit Inventory Visibility integrieren möchten. Inventory Visibility unterstützt die Integration mit verschiedenen Datenquellen, z. B. mit Ihrem Point of Sale (POS)-System, Supply Chain Management und anderen externen Systemen. Standardmäßig ist das Supply Chain Management als Standard-Datenquelle (`fno`) in Inventory Visibility festgelegt.

Um eine Datenquelle hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Datenquelle** die Option **Neue Datenquelle**, um eine Datenquelle hinzuzufügen.

> [!NOTE]
> Wenn Sie eine Datenquelle hinzufügen, stellen Sie sicher, dass Sie den Namen der Datenquelle, die physikalischen Kennzahlen und die Zuordnungen der Dimensionen überprüfen, bevor Sie die Konfiguration für den Dienst "Inventory Visibility" aktualisieren. Sie können diese Einstellungen nicht mehr ändern, nachdem Sie **Konfiguration aktualisieren** gewählt haben.

### <a name="set-up-dimension-mappings"></a>Festlegen von Zuordnungen von Dimensionen

Inventory Visibility bietet eine Liste von Basisdimensionen, die den Dimensionen Ihrer Datenquelle zugeordnet werden können. Dreiunddreißig Dimensionen sind für die Zuordnung verfügbar.

- Wenn Sie Supply Chain Management als eine Ihrer Datenquellen verwenden, werden standardmäßig 13 Dimensionen den Supply Chain Management Standarddimensionen zugeordnet. Zwölf weitere Dimensionen (`inventDimension1` bis `inventDimension12`) sind angepassten Dimensionen im Supply Chain Management zugeordnet. Die restlichen acht Dimensionen sind erweiterte Dimensionen, die Sie externen Datenquellen zuordnen können.
- Wenn Sie Supply Chain Management nicht als eine Ihrer Datenquellen verwenden, können Sie die Dimensionen frei zuordnen. Die folgende Tabelle zeigt die vollständige Liste der verfügbaren Dimensionen.

> [!NOTE]
> Wenn Ihre Dimension nicht in der Liste der Standarddimensionen enthalten ist und Sie eine externe Datenquelle verwenden, empfehlen wir Ihnen, die Zuordnung mit `ExtendedDimension1` bis `ExtendedDimension8` vorzunehmen.

| Dimensionstyp | Dimensionsname |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Nachverfolgung | `BatchId` |
| Nachverfolgung | `SerialId` |
| Ziel | `LocationId` |
| Ziel | `SiteId` |
| Bestand Status | `StatusId` |
| Lagerspezifisch | `WMSLocationId` |
| Lagerspezifisch | `WMSPalletId` |
| Lagerspezifisch | `LicensePlateId` |
| Sonstige | `VersionId` |
| Bestand (angepasst) | `InventDimension1` bis `InventDimension12` |
| Sonstige | `ExtendedDimension1` durch `ExtendedDimension8` |

Um Zuordnungen von Dimensionen hinzuzufügen, gehen Sie wie folgt vor.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Datenquelle** im Abschnitt **Dimensions-Zuordnungen** die Option **Hinzufügen**, um Dimensions-Zuordnungen hinzuzufügen.
1. Geben Sie im Feld **Dimensionsname** die Quelldimension an.
1. Wählen Sie im Feld **Zur Basisdimension** die Dimension in Inventory Visibility, die Sie zuordnen möchten.
1. Wählen Sie **Speichern** aus.

![Hinzufügen von Zuordnungen von Dimensionen](media/inventory-visibility-dimension-mapping.png "Hinzufügen von Zuordnungen von Dimensionen")

Wenn Ihre Datenquelle z. B. eine Produktfarbendimension enthält, können Sie diese der Basisdimension `ColorId` zuordnen, um eine angepasste Dimension `ProductColor` in der Datenquelle `exterchannel` hinzuzufügen. Sie wird dann der Basisdimension `ColorId` zugeordnet.

## <a name="create-a-physical-measure"></a>Erzeugen einer physikalischen Messung

Wenn eine Datenquelle eine Bestandsänderung an Inventory Visibility sendet, sendet sie diese Änderung unter Verwendung von *physikalischen Messungen*. Physikalische Messungen sind Modifikatoren, die die zusammengefassten Zustände von Transaktionen im Bestand widerspiegeln. Abfragen können auf den physikalischen Kennzahlen basieren.

Inventory Visibility verfügt über eine Liste von standardmäßigen physikalischen Messungen. Diese voreingestellten physikalischen Kennzahlen werden aus den Status der Transaktionen im Lagerbestand auf der Seite **Bestandsliste** im Supply Chain Management (**Bestandsverwaltung \> Abfragen und Bericht \> Bestandsliste**) übernommen.

| Modifizierer | Name |
|---|---|
| `PhysicalInvent` | Physischer Bestand |
| `ReservPhysical` | Physisch reserviert |
| `AvailPhysical` | Physisch verfügbar |
| `ReservOrdered` | Bestellt Reserviert |
| `PostedQty` | Gebuchte Menge |
| `Deducted` | Abgesetzt |
| `Picked` | Entnommen |
| `Received` | Eingegangen |
| `Registered` | Erfasst |
| `Arrived` | Angekommen |
| `Ordered` | Bestellt |
| `OnOrder` | Auf Bestellung |
| `QuotationReceipt` | Angebotseingang |
| `QuotationIssue` | Angebot Ausgabe |

Wenn die Datenquelle Supply Chain Management ist, müssen Sie die standardmäßigen physikalischen Messungen nicht neu erstellen. Für externe Datenquellen können Sie jedoch neue physikalische Messungen erstellen, indem Sie die folgenden Schritte ausführen.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Datenquelle** im Abschnitt **Physikalische Messungen** die Option **Hinzufügen**, geben Sie einen Namen für die Quelle der Messungen an und speichern Sie die Änderungen.

## <a name="define-the-product-hierarchy-index"></a>Definieren Sie den Produkthierarchie-Index

Indem Sie aggregierte Dimensionsgruppen festlegen, können Sie Inventory Visibility verwenden, um den Status des Lagerbestands abzufragen. In Inventory Visibility wird jede Dimensionsgruppe als *Index* bezeichnet. Jeder Index entspricht einer festgelegten Nummer. Sie können entscheiden, welche Dimensionen zum Einrichten der Indizierung verwendet werden, basierend auf der Art und Weise, wie Sie in Inventory Visibility abfragen.

Um Ihren Produkthierarchie-Index festzulegen, gehen Sie wie folgt vor.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Wählen Sie auf der Registerkarte **Produkthierarchie-Index** im Abschnitt **Dimensions-Zuordnungen** die Option **Hinzufügen**, um Zuordnungen von Dimensionen hinzuzufügen.
1. Standardmäßig wird eine Liste von Indizes bereitgestellt. Um einen vorhandenen Index zu ändern, wählen Sie **Bearbeiten** oder **Hinzufügen** im Abschnitt für den betreffenden Index. Um einen neuen Indexsatz zu erstellen, wählen Sie **Neuer Indexsatz**. Wählen Sie für jede Zeile in jedem Indexsatz im Feld **Dimension** aus der Liste der Basisdimensionen aus. Die Werte für die folgenden Felder werden automatisch generiert:

    - **Set-Nummer** - Dimensionen, die zur gleichen Gruppe (Index) gehören, werden zusammen gruppiert, und ihnen wird die gleiche Set-Nummer zugewiesen.
    - **Hierarchie** - Die Hierarchie wird verwendet, um die unterstützten Dimensionskombinationen zu definieren, die in einer Dimensionsgruppe (Index) abgefragt werden können. Wenn Sie z. B. eine Dimensionsgruppe festlegen, die eine Hierarchie-Sequenz von *Stil*, *Farbe* und *Größe* hat, unterstützt das System das Ergebnis von drei Abfragegruppen. Die erste Gruppe ist nur Stil. Die zweite Gruppe ist eine Kombination aus Stil und Farbe. Und die dritte Gruppe ist eine Kombination aus Stil, Farbe und Größe. Die anderen Kombinationen werden nicht unterstützt.

Weitere Informationen finden Sie unter [Produktindex-Hierarchie-Konfiguration](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Beispiel

In diesem Abschnitt finden Sie ein Beispiel, das zeigt, wie die Hierarchie funktioniert. Die folgende Tabelle zeigt eine Liste der verfügbaren Bestände für dieses Beispiel.

| Artikel | Format | Farbe | Größe | Leistung |
|---|---|---|---|---|
| I0001 | Breit | Schwarz | Klein | 1 |
| I0001 | Breit | Schwarz | Groß | 2 |
| I0001 | Breit | Red | Klein | 3 |
| I0001 | Regelmäßig | Schwarz | Klein | 4 |
| I0001 | Regelmäßig | Schwarz | Groß | 5 |
| I0001 | Regelmäßig | Red | Klein | 6 |
| I0001 | Regelmäßig | Red | Groß | 7 |

Die folgende Tabelle zeigt, wie die Indexhierarchie festgelegt wird.

| Schlüssel | Nummer festlegen | Hierarchie |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Basierend auf den vorangegangenen Einstellungen lautet die Dimensionskombination für die Abfrage der Inventory Visibility *Stil*, *Farbe* und *Größe*. Die Einrichtung der Hierarchie ermöglicht es externen Systemen, den Lagerbestand auf die folgenden Arten abzufragen:

- `()` - gruppiert nach allen. Hier ist die Ausgabe:

    - I0001, 28

- `(StyleId)` - Gruppiert nach dem Stil. Hier ist die Ausgabe:

    - I0001, Wide, 6
    - I0001, Regular, 22

- `(StyleId, ColorId)` - Gruppiert nach der Kombination von Stil und Farbe. Hier ist die Ausgabe:

    - I0001, Wide, Schwarz,3
    - I0001, Wide, Rot, 3
    - I0001, Regular, Schwarz, 9
    - I0001, Regular, Rot, 13

- `(StyleId, ColorId, SizeId)` - Gruppiert nach der Kombination von Stil, Farbe und Größe. Hier ist die Ausgabe:

    - I0001, Wide, Schwarz, Small,1
    - I0001, Wide, Schwarz, Large, 2
    - I0001, Wide, Rot, Small, 3
    - I0001, Regular, Schwarz, Small, 4
    - I0001, Regular, Schwarz, Large, 5
    - I0001, Regular, Rot, Small, 6
    - I0001, Regular, Rot, Large, 7

## <a name="set-up-a-custom-calculated-measure"></a>Eine angepasste berechnete Messung festlegen

Sie können Inventory Visibility verwenden, um sowohl physische Messungen im Bestand als auch *angepasste berechnete Kennzahlen* abzufragen.

In der Konfiguration können Sie eine Reihe von Modifikatoren festlegen, die addiert oder subtrahiert werden, um die gesamte aggregierte Ausgabemenge zu erhalten.

1. Melden Sie sich in Ihrer Power Apps-Umgebung an und öffnen Sie **Inventory Visibility**.
1. Öffnen Sie die Seite **Konfiguration**.
1. Auf der Registerkarte **Berechnete Messung** wählen Sie **Neue berechnete Messung**, um eine berechnete Messung hinzuzufügen. Legen Sie dann die Felder wie in der folgenden Tabelle beschrieben fest.

    | Feld | Wert |
    |---|---|
    | Name der neuen berechneten Messung | Geben Sie den Namen der berechneten Messung ein. |
    | Datenquelle | Das abfragende System ist eine Datenquelle. |
    | Modifier-Datenquelle | Geben Sie die Datenquelle des Modifikators ein. |
    | Modifizierer | Geben Sie den Namen des Modifikators ein. |
    | Modifikator-Typ | Wählen Sie den Modifikatortyp (*Addition* oder *Subtraktion*). |

Die folgende Tabelle zeigt ein Beispiel für die angepasste berechnete Messung `MyCustomAvailableforReservation`. Weitere Informationen zu diesem Beispiel finden Sie unter [Datenquellenkonfiguration](inventory-visibility-configuration.md#data-source-configuration).

| Datenquelle für berechnete Messungen | Berechnete Messung | Modifier-Datenquelle | Modifizierer | Modifikator-Typ |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Zuordnung von Soft-Reservierungen festlegen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Bevor Sie die **Zuordnung von Soft-Reservierungen** bearbeiten können, müssen Sie die Funktion *OnHandReservation* auf der Registerkarte **Funktionsverwaltung** einschalten.

Indem Sie die Zuordnung von der physikalischen Messung zur berechneten Messung festlegen, ermöglichen Sie dem Dienst Inventory Visibility, die Verfügbarkeit von Reservierungen automatisch zu überprüfen, basierend auf der physikalischen Messung.

Bevor Sie diese Zuordnung festlegen, müssen die physikalischen Messungen, die berechneten Messungen und ihre Datenquellen auf den Registerkarten **Datenquelle** und **Berechnete Messung** der Seite **Konfiguration** in Power Apps definiert werden (wie zuvor in diesem Thema beschrieben).

Um die Zuordnung der Soft-Reservierung zu definieren, gehen Sie wie folgt vor.

1. Definieren Sie die physikalische Kennzahl, die als Soft-Reservierungsmaßnahme dient (zum Beispiel `softreservordered`).
1. Definieren Sie auf der Registerkarte **Berechnete Kennzahl** der Seite **Konfiguration** die *zur Reservierung verfügbare* (AFR) berechnete Kennzahl, die die AFR-Berechnungsformel enthält, die Sie der physikalischen Messung zuordnen möchten. Sie könnten z.B. `availforreserv` (verfügbar für Reservierung) so festlegen, dass sie der zuvor definierten physikalischen Messung `softreservordered` zugeordnet wird. Auf diese Weise können Sie feststellen, welche Mengen, die den Bestandsstatus `softreservordered` haben, für die Reservierung verfügbar sind. Die folgende Tabelle zeigt die AFR-Berechnungsformel.

    | Modifizierer | Datenquelle | Kennzahl |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Öffnen Sie die Seite **Konfiguration**.
1. Legen Sie auf der Registerkarte **Zuordnung von Soft-Reservierungen** die Zuordnung von der physischen Messung zur berechneten Kennzahl fest. Für das vorherige Beispiel könnten Sie die folgenden Einstellungen verwenden, um `availforreserv` der zuvor definierten physikalischen Messung `softreservordered` zuzuordnen.

    | Datenquelle für physikalische Messungen | Physikalische Messung | Verfügbar für Reservierungsdatenquelle | Verfügbar für die berechnete Messung der Reservierung |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Eine weiche Reservierungshierarchie festlegen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Bevor Sie die Registerkarte **Soft-Reservierungshierarchie** bearbeiten können, müssen Sie die Funktion *OnHandReservation* auf der Registerkarte **Funktionsverwaltung** einschalten.

Die Reservierungshierarchie beschreibt die Sequenz von Dimensionen, die bei der Reservierung angegeben werden müssen. Sie funktioniert genauso wie die Produktindexhierarchie bei Lagerbestandsabfragen.

Die Reservierungshierarchie kann sich von der Hierarchie des Lagerbestands unterscheiden. Diese Unabhängigkeit ermöglicht die Implementierung einer Kategorieverwaltung, bei der Benutzer die Dimensionen in Details aufschlüsseln können, um die Anforderungen für genauere Reservierungen zu spezifizieren.

#### <a name="example"></a>Beispiel

Die folgende Reservierungshierarchie ist in Ihrem System festgelegt.

| Dimensionen | Hierarchie |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Bei dieser Reservierungshierarchie können Sie Reservierungen in den folgenden Dimensionen-Reihenfolgen vornehmen:

- `()` - Es ist keine Dimension angegeben.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Die Reihenfolge der Dimensionen sollte strikt der Sequenz der Reservierungshierarchie folgen, Dimension für Dimension. Reservierungen mit `(ColorId, StyleId)` werden in diesem Beispiel nicht zugelassen, da diese Sequenz in der Reservierungshierarchie nicht definiert ist.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Steuerelement-Verwaltung

Das Bestandssichtbarkeit-Add-In bietet Funktionen wie *AufHandReservierung* und *AufHandMostSpecificBackgroundService*. Standardmäßig sind diese Funktionen ausgeschaltet. Um sie zu verwenden, öffnen Sie die Seite **Konfiguration** in Power Apps und schalten Sie sie dann auf der Registerkarte **Funktionsverwaltung** ein.

### <a name="complete-and-update-the-configuration"></a>Abschließen und Aktualisieren der Konfiguration

Nachdem Sie die Konfiguration abgeschlossen haben, müssen Sie alle Änderungen an Inventory Visibility festschreiben. Um die Änderungen zu bestätigen, wählen Sie **Konfiguration aktualisieren** in der oberen rechten Ecke der Seite **Konfiguration** in Power Apps.

Wenn Sie zum ersten Mal **Konfiguration aktualisieren** wählen, fordert das System Ihre Anmeldeinformationen an.

- **Client Id** - Die Azure-Anwendungs-ID, die Sie für Inventory Visibility erstellt haben.
- **Mandanten-ID** - Ihre Azure-Mandanten-ID.
- **Client Secret** - Das Azure-Anwendungsgeheimnis, das Sie für Inventory Visibility erstellt haben.

Nachdem Sie sich angemeldet haben, wird die Konfiguration im Inventory Visibility-Dienst aktualisiert.

> [!NOTE]
> Stellen Sie sicher, dass Sie den Namen der Datenquelle, die physikalischen Messungen und die Zuordnungen der Dimensionen überprüfen, bevor Sie die Konfiguration für den Inventory Visibility-Dienst aktualisieren. Sie können diese Einstellungen nicht mehr ändern, nachdem Sie **Konfiguration aktualisieren** gewählt haben.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finden Sie den Dienst-Endpunkt

Wenn Sie den richtigen Dienst-Endpunkt für Inventory Visibility nicht kennen, öffnen Sie die Seite **Konfiguration** in Power Apps und wählen Sie dann **Dienst-Endpunkt anzeigen** in der oberen rechten Ecke. Die Seite zeigt den korrekten Dienst-Endpunkt an.

## <a name="operational-visibility"></a>Operative Sichtbarkeit

Die Seite **Betriebliche Sichtbarkeit** liefert die Ergebnisse einer Echtzeit-Abfrage des Lagerbestands, basierend auf verschiedenen Dimensionskombinationen. Wenn die Funktion *OnHandReservation* eingeschaltet ist, können Sie auch Reservierungsanfragen von der Seite **Operative Sichtbarkeit** aus stellen.

### <a name="on-hand-query"></a>Lagerbestand-Abfrage

Die Registerkarte **Auf-Hand-Abfrage** zeigt die Ergebnisse einer Echtzeit-Abfrage des Lagerbestands an.

Wenn Sie die Registerkarte **Bestandsabfrage** wählen, fordert das System Ihre Anmeldeinformationen an, um das Inhaber-Token zu erhalten, das für die Abfrage des Inventory Visibility-Dienstes erforderlich ist. Sie können das Inhaber-Token einfach in das Feld **BearerToken** einfügen und das Dialogfeld schließen. Sie können dann eine Anfrage für eine Lagerbestandsabfrage stellen.

Wenn das Inhaber-Token nicht gültig ist oder abgelaufen ist, müssen Sie ein neues in das Feld **BearerToken** einfügen. Geben Sie die richtigen Werte **Client ID**, **Mandanten ID**, **Client Secret** ein und wählen Sie dann **Aktualisiert**. Das System wird automatisch ein neues, gültiges Träger-Token erhalten.

Um eine Lagerbestand-Abfrage zu stellen, geben Sie die Abfrage in den Anfragekörper ein. Verwenden Sie das Muster, das in [Abfrage unter Verwendung der Post-Methode](inventory-visibility-api.md#query-with-post-method) beschrieben ist.

![Einstellungen für die On-Hand-Abfrage](media/inventory-visibility-query-settings.png "Einstellungen für die On-Hand-Abfrage")

### <a name="reservation-posting"></a>Reservierungsbuchung

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Verwenden Sie die Registerkarte **Reservierungsbuchung**, um eine Reservierungsanfrage zu buchen. Bevor Sie eine Reservierungsanfrage buchen können, müssen Sie die Funktion *OnHandReservation* einschalten. Weitere Informationen zu dieser Funktion finden Sie unter [Inventory Visibility Reservierungen](inventory-visibility-reservations.md).

Um eine Reservierungsanfrage zu stellen, müssen Sie einen Wert in den Anfragekörper eingeben. Verwenden Sie das Muster, das in [Ein Ereignis für Reservierungen erstellen](inventory-visibility-api.md#create-one-reservation-event) beschrieben ist. Wählen Sie dann **Posten**. Um die Details der Anfrageantwort zu sehen, wählen Sie **Details anzeigen**. Sie können auch den Wert **ReservationId** aus den Antwortdetails abrufen.

## <a name="inventory-summary"></a>Bestandszusammenfassung

**Bestandsübersicht** ist eine angepasste Ansicht für die *Bestandsübersicht OnHand Entität*. Sie bietet eine Bestandszusammenfassung für Produkte zusammen mit allen Dimensionen. Mit Hilfe des **Erweiterten Filters**, den Dataverse zur Verfügung stellt, können Sie eine persönliche Ansicht erstellen, die die Zeilen anzeigt, die für Sie wichtig sind. Mit den erweiterten Filteroptionen können Sie eine breite Palette von Ansichten erstellen, von einfach bis komplex. Sie lassen Sie auch gruppierte und verschachtelte Bedingungen zu den Filtern hinzufügen.

Um mehr über die Verwendung des **Erweiterten Filters** zu erfahren, siehe [Bearbeiten oder Erstellen von persönlichen Ansichten mit erweiterten Raster-Filtern](/powerapps/user/grid-filters-advanced)

Im oberen Bereich der angepassten Ansicht stehen drei Felder zur Verfügung: **Standard Dimension**, **Angepasste Dimension** und **Messung**. Mit diesen Feldern können Sie steuern, welche Spalten sichtbar sind.

Sie können die Spaltenüberschrift auswählen, um das aktuelle Ergebnis zu filtern oder zu sortieren.

Der untere Teil der angepassten Ansicht zeigt Informationen wie "50 Datensätze (29 ausgewählt)" oder "50 Datensätze." Diese Informationen beziehen sich auf die aktuell geladenen Datensätze aus dem Ergebnis des **Erweiterten Filters**. Der Text "29 ausgewählt" bezieht sich auf die Anzahl der Datensätze, die mit Hilfe des Spaltenkopf-Filters für die geladenen Datensätze ausgewählt wurden.

Unten in der Ansicht befindet sich eine Schaltfläche **Mehr laden**, mit der Sie weitere Datensätze von Dataverse laden können. Die Standardanzahl der Datensätze, die geladen wird, ist 50. Wenn Sie **Mehr laden** wählen, werden die nächsten 1.000 verfügbaren Datensätze in die Ansicht geladen. Die Zahl auf der Schaltfläche **Mehr laden** zeigt die aktuell geladenen Datensätze und die Gesamtzahl der Datensätze für das Ergebnis des **Erweiterten Filters** an.

![Lagerzusammenfassung](media/inventory-visibility-onhand-list.png "Lagerzusammenfassung")
