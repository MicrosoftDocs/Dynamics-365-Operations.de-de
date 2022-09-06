---
title: Attribute und Attributgruppen verwalten
description: Dieser Artikel beschreibt, wie Sie Attribute und Attributgruppen verwalten, um Produkte und ihre Eigenschaften in Microsoft Dynamics 365 Commerce zu beschreiben.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386971"
---
# <a name="manage-attributes-and-attribute-groups"></a>Attribute und Attributgruppen verwalten

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Attribute und Attributgruppen verwalten, um Produkte und ihre Eigenschaften in Microsoft Dynamics 365 Commerce zu beschreiben.

*Attribute* bieten Ihnen eine Möglichkeit Produkt und ihre Merkmale mit benutzerdefinierten Feldern beschreiben. Beispiele sind Speichergröße, Festplattenkapazität und „Energy Star“-Konformität.

Attribute können unterschiedlichen Commerce-Entitäten zugeordnet werden, wie Produktkategorien und Kanäle, und Standardwerte können für sie festgelegt werden. Wenn Attribute Produktkategorien oder Kanälen zugeordnet sind, erben Produkte diese Attribute und ihre Standardwerte. Standardattributwerte können auf der Einzelproduktebene, Kanalebene oder in einem Katalog überschrieben werden.

So kann beispielsweise ein Fernsehprodukt folgende Attribute haben.

| Kategorie   | Attribut           | Zulässige Werte                        | Standardwert |
|------------|---------------------|-------------------------------------------|---------------|
| TV & Video | Marke               | Jeder gültige Marken-Wert                     | Kein          |
| TV         | Bildschirmgröße         | 20–85 Inches                              | 55 Zoll     |
|            | Vertikale Auflösung | 4K (2160p), Full HD (1080p) oder HD (720p) | 4K (2160p)    |
|            | Bildschirm-Aktualisierungsrate | 60 Hz, 120 Hz oder 240 Hz                     | 60 Hz          |
|            | HDMI-Eingaben         | 0 – 10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Attribute und Attributtypen

Attribute basieren auf *Attributtypen*. Ein Attributtyp identifiziert die Art von Daten, die für ein bestimmtes Attribut eingegeben werden können. Die folgenden Attributtypen werden in Commerce unterstützt:

- **Währung** – Dieser Attributtyp unterstützt Währungswerte. Er kann begrenzt (das heißt, er unterstüzt einen Wertebereich) oder offengelassen werden.
- **DateTime** – Dieser Attributtyp unterstützt Datums- und Uhrzeitwerte. Es kann übersprungen oder offen gelassen werden.
- **Dezimal** – Dieser Attributtyp unterstützt numerische Werte, die Dezimalstellen enthalten. Er unterstützt auch Maßeinheiten. Es kann übersprungen oder offen gelassen werden.
- **Ganzzahl** – Dieser Attributtyp unterstützt numerische Werte. Er unterstützt auch Maßeinheiten. Es kann übersprungen oder offen gelassen werden.
- **Text** – Dieser Attributtyp unterstützt Textwerte. Es unterstützt auch einen vordefinierten Satz möglicher Werte, wenn die Einstellung **Feste Liste** aktiviert ist.
- **Boolesch** – Dieser Attributtyp unterstützt Binärwerte (**TRUE** oder **FALSE**).
- **Referenz** – Dieser Typ bezieht andere Attribute.

> [!NOTE]
> Durch [Einschränkungen des Azure-Suchindex](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search) wird der Attributtyp **Dezimal** für cloudbasierte Suchumgebungen nicht unterstützt. Azure Cognitive Search unterstützt die Konvertierung des Attributtyps **Dezimal** in **Edm.Double**-Zielindexfeldtypen nicht, da diese Konvertierung die Genauigkeit verringern würde.

### <a name="set-up-attribute-types"></a>Attributtypen einrichten

Folgen Sie zum Einrichten von Attributtypen den Schritten in diesem Beispielverfahren.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Wechseln Sie zu **Produktinformationsverwaltung \> Einstellungen \> Kategorien und Attribute \> Attributtypen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name des Attributtyps** **Taschentyp** ein.
1. Wählen Sie im Feld **Typ** die Option **Text**.
1. Legen Sie die Option **Feste Liste** auf **Ja** fest.
1. Wählen Sie im Inforegister **Werte** die Option **Hinzufügen**.
1. Geben Sie in der neuen Zeile im Feld **Wert** den Wert **Umhängetasche** ein.
1. Fügen Sie fünf weitere Zeilen hinzu. Geben Sie im Feld **Wert** jeweils einen anderen Wert ein: **Clutch**, **Handtasche**, **Rucksack**, **Messenger Bag** oder **Geldbörse**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name des Attributtyps** **Sonnenbrillenmarke** ein.
1. Wählen Sie im Feld **Typ** die Option **Text**.
1. Legen Sie die Option **Feste Liste** auf **Ja** fest.
1. Wählen Sie im Inforegister **Werte** die Option **Hinzufügen**.
1. Geben Sie in der neuen Zeile im Feld **Wert** den Wert **Ray-Ban** ein.
1. Fügen Sie zwei weitere Zeilen hinzu. Geben Sie im Feld **Wert** jeweils einen anderen Wert ein: **Aviator** oder **Oakley**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

![Seite „Attributtypen“.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Ein Attribut einrichten

Folgen Sie zum Einrichten eines Attributs den Schritten in diesem Beispielverfahren.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Wechseln Sie zu **Produktinformationsverwaltung \> Einstellungen \> Kategorien und Attribute \> Attribute**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name** die Bezeichnung **Taschenart** ein.
1. Wählen Sie im Feld **Name des Attributtyps** **Taschentyp** aus.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

![Attributseite.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Attributmetadaten

*Attributmetadaten* lässt Sie Optionen auswählen, um anzugeben, wie deren Attribute für jedes Produkt sich verhalten sollen. So können beispielsweise auswählen, ob Attribute erforderlich sind, ob sie zum Suchen verwendet werden können und ob sie als Filter verwendet werden können.

Für Produkte können die Attributmetadateneinstellungen auf der Einzelvorgangsebene überschrieben werden.

Die Seite **Attribute** eines Attributs enthält mehrere Optionen, die Attributmetadaten zugeordnet werden. Wenn Sie zum Beispiel die Option **Kann verfeinert werden** unter **Attributmetadaten für Commerce-Kanälen** auf **Ja** setzen, wird das Attribut zur Verfeinerung oder Filterung von Produkten in Suchergebnissen und Seiten zum Durchsuchen von Kategorien angezeigt. Um ein Attribut zu als verfeinerbar zu konfigurieren, wählen Sie zuerst **Filtereinstellungen** im Aktionsbereich aus und bestätigen Sie die Filtereinstellungen für das Attribut.

## <a name="filter-settings-for-attributes"></a>Attributfiltereinstellungen

Filtereinstellungen für Attribute lassen Sie festlegen, wie die Attributfilter in der Verkaufsstelle (POS) angezeigt werden. Um auf Filtereinstellungen für ein Attribut zuzugreifen wählen Sie auf der Seite **Attribute** des Attributs im Aktionsbereich **Filtereinstellungen** aus.

Die Seite **Filtereinstellungen** enthält die folgenden Felder:

- **Name** – Per Standard wird das Feld für den Namen des Attributs festgelegt. Allerdings kann der Wert geändert werden.
- **Anzeigeoption** - Die folgenden Ausrichtungsoptionen sind verfügbar:

    - **Einzelner Wert** – Diese Option ist für die folgenden Attributtypen verfügbar: **Boolesch**, **Währung**, **Dezimal**, **Ganzzahl** und **Text**. Es kann nur ein einziger Wert für Einschränkungen auf Produktlistenseiten ausgewählt werden, z. B. das Durchsuchen von Kategorien und Produktsuchergebnisseiten.
    - **Mehr-Wert** – Diese Option ist für die folgenden Attributtypen verfügbar: **Boolesch**, **Dezimal**, **Ganzzahl** und **Text**. Dadurch können für das Attribut im Client mehrere Werte zur Verfeinerung ausgewählt werden.

- **Anzeigeoption** - Die folgenden Ausrichtungsoptionen sind verfügbar:

    - **Liste**: Diese Option ist für alle Attributtypen verfügbar.
    - **Bereich** – Diese Option ist für die folgenden Attributtypen verfügbar: **Währung**, **Dezimal** und **Ganzzahl**.
    - **Bereich** – Diese Option ist für die folgenden Attributtypen verfügbar: **Währung**, **Dezimal** und **Ganzzahl**.
    - **Schieberegler mit Leisten** – Diese Option ist für die folgenden Attributtypen verfügbar: **Währung**, **Dezimal** und **Ganzzahl**.

- **Schwellenwert** – Diese Einstellung ist erforderlich, wenn Sie **Bereich** als Anzeigensteuerelementtyp ausgewählt haben. Sie können Werte festlegen, indem Sie ein Trennzeichen (;) als Trennzeichen verwenden.

    Zum Beispiel könnte der Schwellenwert für ein Attribut **Taschenvolumen** mit dem Attributtyp **Integer** **10, 20, 50, 100, 200, 500, 1.000. 5.000** sein. In diesem Fall enthält der POS die folgenden Bereiche. Bereiche, die keine Produkte im Resultset haben, werden grau angezeigt.

    - Weniger als 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 oder mehr

Filtereinstellungen für Attribute gelten nur für Produktattribute und können verwendet werden, um die Ergebnisse der Produktsuche und der Suche nach Kategorien zu verfeinern. Sie gelten nicht für die Debitorensuche oder Auftragssuche, obwohl die gleichen Attribute zur Anreicherung von Kunden- oder Auftragsinformationen verwendet werden können.

In den Standard-Commerce-Modulen ist kein sofort einsatzbereiter Support für die Filtereinstellungen der **Anzeigesteuerung** verfügbar, wie z. B. **Bereich**, **Schieberegler** und **Schieber mit Leisten**. Die Einstellungen **Bereich** und **Schieberegler** werden weiterhin für POS-Lösungen unterstützt, während die Einstellung **Schieberegler mit Leiste** für Legacy SharePoint-Online-Storefronts gilt und weiterhin für die Integration von Drittanbietern und für benutzerdefinierte Szenarien verfügbar ist.

Wir empfehlen, dass verfeinerbare Attribute ein Attribut vom Typ **Text** haben und die Option **Feste Liste** aktiviert ist. Sie sollten außerdem die Liste überschaubar halten (bis zu 100 bis 200 eindeutige Werte). Wenn eine Einschränkung über 1.000 oder mehr eindeutige Werte verfügt, ist es besser, ein Attribut vom Typ **Text** zu verwenden, wobei die Option **Feste Liste** deaktiviert ist.

Übersetzungen sind entscheidend für Attributnamen und ihre Werte. Für Attribute vom Typ **Text**, bei denen die Option **Feste Liste** aktiviert ist, können Sie Übersetzungen für die Attributwerte unter **Attributtyp** festlegen. Für jeden anderen Attributtyp können Sie Übersetzungen auf der Seite festlegen, auf der Sie die Attributwerte definieren. Beispielsweise können Sie für ein Attribut vom Typ **Text** Übersetzungen für den Standardwert des Attributs auf der Seite **Attribute** festlegen. Wenn Sie jedoch den Standardwert auf Produktebene überschreiben, können Sie Übersetzungen für das Attribut auf der Seite **Produktattribute** festlegen.

Nachdem ein Attribut für einen Kanal als verfeinerbar gekennzeichnet wurde, sollten Sie den Attributtyp nicht aktualisieren. Andernfalls beeinträchtigen Sie die Veröffentlichung von Produktdaten im Suchindex. Stattdessen empfehlen wir, dass Sie ein neues Attribut für einen neuen Einschränkungstyp erstellen und das vorherige Attribut zurückziehen, indem Sie es aus anderen Attributgruppen entfernen.

Die Suche nach Attributen wird unterstützt, es werden jedoch nur Ergebnisse für exakte Übereinstimmungen mit Suchwörtern abgerufen. Angenommen ein Attribut **Stoff** hat den Wert **Kaschmir-Baumwolle**. Wenn ein Kunde nach „Kash“ sucht, werden keine Produkte angezeigt, deren Stoff **Kaschmir-Baumwolle** ist. Wenn ein Kunde jedoch nach „Kaschmir“, „Baumwolle“ oder „Kaschmir-Baumwolle“ sucht, werden Produkte angezeigt, deren Stoff **Kaschmir-Baumwolle** ist.

### <a name="additional-attribute-metadata-options"></a>Weitere Optionen für Attributmetadaten

> [!NOTE]
> Diese Optionen für Attributmetadaten gelten nur für Legacy SharePoint Online-Storefront- und externe Integrationen. Weitere Informationen über diese Optionen für Attributmetadaten finden Sie unter [Überblick über Suchschemas in SharePoint Server 2013](/SharePoint/search/search-schema-overview).

Die folgenden weiteren Attributmetadatumenoptionen stehen auch auf der Seite **Attribute** zur Verfügung:

- Durchsuchbar
- Abrufbar
- Kann abgefragt werden
- Sortierbar
- Groß-/Kleinschreibung und Format ignorieren
- Vollständige Übereinstimmung

Diese Optionen waren ursprünglich für die Verbesserung der Suchfunktion für Online-Storefronts auf Basis von Legacy SharePoint vorgesehen. Sie gelten nicht unbedingt für Commerce-E-Websites oder POS-Terminals. Da die monitorlose Integration weiterhin unterstützt wird, stehen diese Optionen zum Exportieren von Attributmetadaten mithilfe des Commerce Software Development Kit (SDK) zur Verfügung. Sie können das Commerce SDK verwenden, um Produkte in einen benutzerdefinierten, optimierten externen Suchindex aufzunehmen. Auf diese Weise können Sie sicherstellen, dass nur Attribute indiziert werden, die indiziert werden sollen.

## <a name="attribute-groups"></a>Attributgruppen

Eine *Attributgruppe* dient dazu, die Attribute für eine Komponente oder Unterkomponente in einem Produktkonfigurationsmodell zu gruppieren. Sie können ein Attribut in eine oder mehrere Attributgruppen einbeziehen. Attributgruppen können Benutzer unterstützen, Produkte zu konfigurieren, da die Auswahl in einem bestimmten Kontext angeordnet ist. Sie können Attributgruppen Kategorien oder Kanäle zuweisen. Sie können Standardwerte für Attribute auch in einer Attributgruppe festlegen.

![Seite „Attributgruppen“.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Eine Attributgruppe erstellen

Folgen Sie zum Erstellen einer Attributgruppe den Schritten in diesem Beispielverfahren.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Wechseln Sie zu **Produktinformationsverwaltung \> Einstellungen \> Kategorien und Attribute \> Attributgruppen**.
1. Erstellen Sie eine Attributgruppe mit der Bezeichnung **Anzughemden**.
1. Fügen Sie die folgenden Attribute hinzu: **Reinigungsmethode**, **Kragentyp**, **Kollektion** und **Design**.

> [!NOTE]
> Die Werte der Anzeigereihenfolge von Attributen in der Attributgruppe beeinflussen und gelten nicht für die Reihenfolge der Einschränkungen in den Suchergebnissen und Kategoriedurchsuchungsergebnissen. Sie gelten nur für das Szenario „Bestellattribute“.

### <a name="assign-attribute-groups-to-categories"></a>Zuweisen von Attributgruppen zu Kategorien

Eine oder mehrere Attributgruppen können Kategorieknoten in den folgenden Arten von Kategoriehierarchien zugeordnet werden:

- Handelsprodukthierarchie
- Kanalnavigationskategoriehierarchie
- Zusätzliche Produktkategoriehierarchie

Wenn Produkte in Kategorien kategorisiert werden, die Attributgruppen zugeordnet sind, erben sie die Attribute, die in diesen Attributgruppen enthalten sind.

![Inforegister „Produktattributgruppen“ auf der Seite „Commerce-Produkthierarchie“.](media/AGRetailProdHierarchy_2022Series.png)

Folgen Sie den Schritten in diesem Beispielverfahren, um den Kategorien in der Commerce-Produkthierarchie Attributgruppen zuzuweisen.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Commerce-Produkthierarchie**.
1. Wählen Sie die Navigationshierarchie **Mode** aus.
1. Wählen Sie unter **Herrenbekleidung** die Kategorie **Hosen** und wählen Sie dann auf dem Inforegister **Produktattributgruppen** eine Attributgruppe aus mit der Bezeichnung **Herrengürtel**.
1. Wählen Sie die Kategorie **Modesonnenbrille** und überprüfen Sie die neuen Attribute in der Attributgruppe, **Modesonnenbrille** indem Sie **Attribute anzeigen** auswählen. Die Attributgruppe soll die Attribute neue **Objektivform** und **Sonnenbrillen-Marke** anzeigen.
1. Wählen Sie die Kategorie **Hosen** und überprüfen Sie die Attribute für **Herrengürtel**, indem Sie **Attribute anzeigen** auswählen. Die Attributgruppe sollte **Herrengurtmarke**, **Gurtgewebe** und **Gurtgröße**-Attribute angezeigt.

Mit dem gleichen Basisverfahren können Sie Attributgruppen Kategorien in der Kanalnavigationskategoriehierarchie und in der ergänzenden Produktkategoriehierarchie zuordnen. Verwenden Sie jedoch in Schritt 2 einen der folgenden Pfade, abhängig von der Hierarchie, der Sie Attributgruppen zuweisen möchten:

- **Kanalnavigationskategoriehierarchie:** Gehen Sie zu **Einzelhandel und Handel \> Kategorie- und Produktverwaltung \> Kanalnavigationskategorien**.
- **Ergänzende Produktkategoriehierarchie:** Gehen Sie zu **Einzelhandel und Handel \> Kategorie- und Produktverwaltung \> Ergänzende Produktkategorien**.

> [!NOTE]
> Stellen Sie sicher, dass Sie nur Attributgruppen in einer Kategoriehierarchie im Inforegister **Produktattributgruppen** verknüpfen, nicht im Inforegister **Kategorieattributwerte**. Wenn Attribute auf dem Inforegister **Kategorieattributwerte** erscheinen, wählen Sie **Kategoriehierarchie bearbeiten** im Aktionsbereich aus. Wählen Sie dann im Inforegister **Kategorieattributgruppen** die Kategorieknoten und **Entfernen** aus. Das Abrufen von Attributen nach Kategorie über Commerce Scale Unit wird nicht unterstützt.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Anzeigbare und verfeinerbare Attribute für E-Commerce-Kanäle für die Standardproduktsammlung identifizieren

Nachdem Sie verschiedene Attributgruppen Kategorien in verschiedenen Hierarchien (Commerce-Produkthierarchie- oder Kanalnavigationskategorien) zugeordnet und Attributwerte für jedes Produkt basierend auf der Kategoriezuordnung definiert haben, müssen Sie das Kennzeichen **Attribut auf Kanal anzeigen** aktivieren, um diese Attribute in einem bestimmten Kanal anzeigbar zu machen.

1. Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.
1. Wählen Sie **Attributmetadaten festlegen** und dann im linken Navigationsbereich ein Attribut aus.
1. Legen Sie im Inforegister **Kanalproduktattribute** (nicht im Inforegister **Kategorieattribute**) die Option **Attribut auf Kanal anzeigen** auf **Ja** fest, um das Attribut anzeigbar zu machen.
1. Wenn Sie möchten, dass das Attribut auch verfeinert werden kann, setzen Sie die Option **Kann verfeinert werden** auf **Ja**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Die Sichtbarkeit dimensionsbasierter Einschränkungen wie Größe, Stil und Farbe steuern

Produktabmessungen wie Größe, Stil und Farbe sind die am häufigsten verwendeten Einschränkungen. Um diese Produktdimensionen als Einschränkungen verfügbar zu machen, sollten Sie eine Attributgruppe auf Kanalebene zuordnen, die einen Verweis auf einen Attributtyp enthält, der automatisch Werte von Produktdimensionswerten erbt.

Sie können angeben, dass Produktdimensionen sichtbar und verfeinerbar sind, indem Sie Kennzeichen auf der Seite **Kanalkategorien und Produktattribute** aktualisieren. Wählen Sie den Stammknoten im Navigationsbereich aus und legen Sie dann im Inforegister **Kanalproduktattribute** die Option **Attribut auf Kanal anzeigen** auf **Ja** für die Attribute **Größe**, **Stil** und **Farbe** fest. Wenn Sie möchten, dass diese Attribute auch verfeinert werden können, setzen Sie die Option **Kann verfeinert werden** jeweils auf **Ja**.

![Festlegen von Attributmetadaten für Dimensionseinschränkungen.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Um die Attribute so zu aktivieren, dass sie im auf Demodaten basierenden Houston-Kanal verfügbar sind, befolgen Sie die Schritte in diesem Beispielverfahren.

1. Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.
1. Wählen Sie den **Houston** Kanal aus.
1. Klicken Sie im Aktivitätsbereich auf **Attributmetadaten festlegen**.
1. Wählen Sie **Mode**, und dann Kategorieknoten und dann auf dem Inforegister **Kanalproduktattribute** wählen Sie **Attribut einschließen** für jedes Attribut aus.
1. Wählen Sie **Modezubehör** und dann Kategorieknoten und dann **Modesonnenbrille** und dann auf der Registerkarte **Kanalproduktattribute** wählen Sie **Attribut einschließen** für jedes Attribut aus.
1. Wählen Sie den **Herrenkleidung** Kategorieknoten und dann **Hosen** und dann auf der Registerkarte **Kanalproduktattribute** wählen Sie **Attribut einschließen** für jedes Attribut aus.
1. Nachdem Sie die Attributmetadaten für die gewünschten Attribute und Einschränkungen aktualisiert haben, stellen Sie sicher, dass Sie Ihre Änderungen speichern und den Auftrag **Kanalaktualisierungen veröffentlichen** ausführen. Nachdem die Updates veröffentlicht wurden, müssen Sie die folgenden Aufträge ausführen: **1070** (**Kanalkonfiguration**), **1040** (**Produkte**) und **1150** (**Katalog**).

> [!NOTE]
> - Wenn Ihr Unternehmen erfordert, dass Sie häufig Produkte in der Navigationshierarchie hinzufügen oder entfernen oder dass Sie Änderungen vornehmen, wie z. B. Anzeigereihenfolgewerte aktualisieren, neue Kategorien hinzufügen und neue Attributgruppen zu Kategorien hinzufügen, empfehlen wir Ihnen, den Auftrag **Kanalaktualisierungen veröffentlichen** so zu konfigurieren, dass er als häufiger Stapelverarbeitungsauftrag ausgeführt wird. Alternativ können Sie den Auftrag **Kanalaktualisierungen veröffentlichen** manuell auslösen und dann die folgenden Commerce Data Exchange (CDX) Aufträge ausführen: **1070** (**Kanalkonfiguration**), **1040** (**Produkte**) und **1150** (**Katalog**).
> - Mit einer Option **Erben** können Sie angeben, dass ein Kanal die Attributgruppen von seinem Kanal in der übergeordneten Hierarchie übernehmen soll. Ist der Option **Erben** auf **Ja**, erbt der untergeordnete Kanalknoten alle Attributgruppen und alle Attribute in Attributgruppen.
> - Wenn die Schaltfläche **Attributmetadaten festlegen** im Aktionsbereich nicht verfügbar ist, stellen Sie sicher, dass **Navigationshierarchie** auf dem Inforegister **Allgemein** mit Ihrem Kanal verknüpft ist.
> - Sie dürfen keine Attributgruppen mit Ausnahme dimensionsbasierter Attributgruppen auf Kanalebene zuordnen (z. B. unter **Attributgruppen** auf der Seite **Kanalkategorien und Produktattribute**).
> - Nach der Einführung der Unterstützung für kundenspezifische Business-to-Business-(B2B-)Kataloge in Commerce-Version 10.0.27 wird von Ihnen erwartet, dass Sie die Einschränkungs- und Attributeinstellungen für jeden B2B-Katalog auf dieselbe Weise identifizieren, wie in diesem Artikel beschrieben.

## <a name="override-attribute-values"></a>Attributwerte überschreiben

Die Standardwerte von Attributen können auf der Produktebene überschrieben werden. Sie können für einzelne Produkte in bestimmten Katalogen überschrieben werden, die für bestimmte Kanäle ausgerichtet werden.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Überschreiben Sie die Attributwerte eines Einzelprodukts

Um die Attributwerte eines einzelnen Produkts zu überschreiben, befolgen Sie die Schritte in diesem Beispielverfahren.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Gehen Sie zu **Einzelhandel und Handel \> Kategorie und Produktverwaltung \> Freigegebene Produkte nach Kategorie**.
1. Wählen Sie den **Mode \> Mode-Accessoires \> Modische Sonnenbrille** aus.
1. Wählen Sie das erforderliche Produkt im Raster aus. Klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Verwalten** auf **Produktattribut**.
1. Wählen Sie ein Attribut im linken Bereich aus, und aktualisieren Sie anschließend den Wert im rechten Bereich.

![Seite „Produktattributwerte“.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Die Attributwerte aller Produkte in einem Katalog überschreiben

Um die Attributwerte aller Produkte in einem Katalog zu überschreiben, befolgen Sie die Schritte in diesem Beispielverfahren.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Gehen Sie zu **Einzelhandel und Handel \> Katalogverwaltung \> Alle Kataloge**.
1. Wählen Sie **Fabrikam-Basiskatalog**.
1. Wählen Sie den **Mode \> Mode-Accessoires \> Modische Sonnenbrille** aus.
1. Auf dem Inforegister **Produkte** aktivieren Sie das erforderliche Produkt aus, und wählen Sie anschließend **Attribute** über dem Produktraster aus.
1. Auf den folgenden Inforegistern aktualisieren Sie die Werte die erforderlichen Attribute:

    - Gemeinsam genutzte Produktmedien
    - Gemeinsam genutzte Produktattribute
    - Kanalmedien
    - Kanalspezifische Produktattribute

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Die Attributwerte aller Produkte in einem Kanal überschreiben

Um die Attributwerte aller Produkte in einem Kanal zu überschreiben, befolgen Sie die Schritte in diesem Beispielverfahren.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.
1. Wählen Sie den **Houston** Kanal aus.
1. Auf dem Inforegister **Produkte** aktivieren Sie das erforderliche Produkt aus, und wählen Sie anschließend **Attribute** über dem Produktraster aus.
1. Wenn keine Produkte vorrätig sind, wählen Sie **Hinzufügen** im Inforegister **Produkte** und dann die erforderlichen Produkte im Dialogfeld **Produkte hinzufügen** aus.
1. Auf den folgenden Inforegistern aktualisieren Sie die Werte die erforderlichen Attribute:

    - Gemeinsam genutzte Produktmedien
    - Gemeinsam genutzte Produktattribute
    - Kanalmedien
    - Kanalspezifische Produktattribute

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Variantenspezifische Attributwerte und mehrere Werte für Produktattribute festlegen

Um variantenspezifische Attributwerte und mehrere Werte für Produktattribute festzulegen, befolgen Sie die Schritte in diesem Beispielverfahren.

1. Melden Sie sich als Merchandising-Manager*in in Commerce headquarters an.
1. Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.
1. Wählen Sie den **Houston** Kanal aus.
1. Wählen Sie auf dem Inforegister **Produkte** die erforderliche Produktvariante und anschließend **Attribute** über dem Produktraster aus.
1. Wenn keine Produkte vorrätig sind, wählen Sie **Hinzufügen** im Inforegister **Produkte** und dann die erforderlichen Produktvarianten im Dialogfeld **Produkte hinzufügen** aus.
1. Auf den folgenden Inforegistern aktualisieren Sie die Werte die erforderlichen Attribute:

    - Gemeinsam genutzte Produktmedien
    - Gemeinsam genutzte Produktattribute
    - Kanalmedien
    - Kanalspezifische Produktattribute

#### <a name="example-of-variant-specific-attribute-configuration"></a>Beispiel einer variantenspezifischen Attributkonfiguration
        
In diesem Beispiel ist das **P001-Master**-Produkt ein Multifunktionsschuh, der drei Varianten hat: **Laufen**, **Gehen** und **Trekking**. Legen Sie für jede Variante einen einzigartigen Wert des Attributs **Aktivität** fest. Auf dem Inforegister **Produkte** der Seite **Kanalkategorien und Produktattribute** Ihres Kanals legen Sie den **Aktivität**-Attributswert für die Varianten wie in der folgenden Tabelle fest.

| Variante     | Wert Aktivitätsattribut |
|-------------|--------------------------|
| P001-Master | Sport                   |
| P001-1      | Läuft                  |
| P001-2      | Gehen                  |
| P001-3      | Trekking                 |

Wenn ein Benutzer nach „Schuh“ sucht, wird das Produkt **P001-Master** in den Suchergebnissen angezeigt. Wenn Sie das Attribut **Aktivität** als verfeinerbar konfiguriert haben, führt die Einschränkung **Aktivität** nur **Sport** als verfeinerbaren Wert auf, da dieser Wert für das Attribut **Aktivität** auf der **P001-Master**-Produktebene festgelegt wurde.

Standardmäßig sollen Attribute auf Variantenebene nur auf Produktdetailseiten (PDPs) verwendet werden. Wenn Sie eine bestimmte Produktvariante auf einem PDP auswählen, werden die Produktspezifikationen auf dem PDP für diese bestimmte Variante aktualisiert.

Damit Einschränkungen Attributwerte erfassen können, die auf Produktvariantenebene festgelegt sind, müssen Sie ein Attribut auf Produktmasterebene festlegen und das Kontrollkästchen **Mehrere Werte zulassen** auswählen und den Attributtyp auf **Text** festlegen.

Als Nächstes müssen Sie alle möglichen Werte für Ihre Produktvarianten bestimmen. Für das Attribut **Aktivität**, das in diesem Beispiel verwendet wird, sind mögliche Werte **Laufen**, **Gehen**, **Wandern**, **Trekking**, **Campen**, **Wassersport** und **Wintersport**.

Nachdem Sie bestimmt haben, wie die Werte der Variantenattribute lauten sollen, können Sie sie auf Produktmasterebene festlegen, indem Sie durch senkrechte Striche getrennte Werte verwenden. Für das Attribut **Aktivität** könnten Sie den Attributwert im Produktmaster als **Laufen|Gehen|Wandern|Trekking|Campen|Wassersport|Wintersport** festlegen.

Anschließend können Sie für jede Variante Attributwerte festlegen, indem Sie entweder durch senkrechte Striche getrennte Werte oder Einzelwerte eingeben. Für das Attribut **Aktivität** können Sie eine einzelne Produktvariante als **Laufen|Gehen|Wandern**, **Laufen**, **Laufen|Wandern|Wassersport** usw festlegen.

Nachdem Sie die Variantenattributwerte festgelegt haben, wählen Sie auf der Seite **Kanalkategorien und Produktattribute** im Aktivitätsbereich **Kanalaktualisierungen veröffentlichen** aus und führen Sie dann die Aufträge **1150**, **1040** und **1070** aus.

Nachdem die Aufträge abgeschlossen und der Suchindex aktualisiert wurde, sollten alle erwarteten Werte in den Suchergebnissen und Ergebnissen der Kategoriesuche angezeigt werden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
