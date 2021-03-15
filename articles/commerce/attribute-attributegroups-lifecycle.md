---
title: Attribute und Attributgruppen verwalten
description: In diesem Thema wird beschrieben, wie Sie Attribute verwendet, um ein Produkt und dessen Eigenschaften über benutzerdefinierte Felder zu beschreiben.
author: ashishmsft
manager: AnnBe
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: 70e2b52dd140660fe98c6ff07248a033ba4bd635
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979972"
---
# <a name="manage-attributes-and-attribute-groups"></a>Attribute und Attributgruppen verwalten

[!include [banner](includes/banner.md)]

*Attribute* enthalten eine weitere Möglichkeit, ein Produkt und dessen Eigenschaften nach benutzerdefinierte Felder (wie **Speichergröße**, **Festplattenkapazität**, **Ist der kompatible Energiestern**, usw.) zu beschreiben. Attribute können unterschiedlichen Commerce-Entitäten zugeordnet werden, wie Produktkategorien und Kanäle, und Standardwerte können für sie festgelegt werden. Produkte erben deren Attribute und Standardwerte für diese Attribute, wenn sie Produktkategorien oder Kanälen zugeordnet sind. Die Standardwerte können auf der Einzelproduktebene, Kanalebene oder in einem Katalog überschrieben werden.


So kann beispielsweise ein Fernsehprodukt folgende Attribute haben.

| Kategorie   | Attribut                | Zulässige Werte          | Standardwert |
|------------|--------------------------|-----------------------------|---------------|
| TV & Video | Marke                    | Jeder gültige Marken-Wert       | None          |
| TV         | Bildschirmgröße              | 20–80 Inches                | None          |
|            | Vertikale Auflösung      | 480i, 720p, 1080i oder 1080p | 1080p         |
|            | Bildschirm-Aktualisierungsrate      | 60 Hz, 120 Hz oder 240 Hz       | 60 Hz          |
|            | HDMI-Eingaben              | 0 – 10                        | 3             |
|            | DVI-Eingaben               | 0 – 10                        | 1             |
|            | Zusammengesetzte Eingaben         | 0 – 10                        | 2             |
|            | Komponenten-Eingaben         | 0 – 10                        | 1             |
| LCD        | 3D-fähig                 | Ja oder Nein                   | Ja           |
|            | 3D-aktiviert               | Ja oder Nein                   | Nr.            |
| Plasma     | Betriebstemperatur von      | 32–110 Grad              | 32            |
|            | Betriebstemperatur bis        | 32–110 Grad              | 100           |
| Projektion | Projektionstubus-Garantie | 6, 12 oder 18 Monate         | 12            |
|            | \# des Projektionstubus   | 1 – 5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Attribute und Attributtypen

Attribute basieren auf *Attributtypen*. Der Attributtyp identifiziert die Art von Daten, die für ein bestimmtes Attribut eingegeben werden können. Die folgenden Attributtypen werden unterstützt:

- **Währung** – Dieser Attributtyp unterstützt Währungswerte. Er kann begrenzt (das heißt, er unterstüzt einen Wertebereich) oder offengelassen werden.
- **DateTime** – Dieser Attributtyp unterstützt Datums- und Uhrzeitwerte. Es kann übersprungen oder offen gelassen werden.
- **Dezimal** – Dieser Attributtyp unterstützt numerische Werte, die Dezimalstellen enthalten. Er unterstützt auch Maßeinheiten. Es kann übersprungen oder offen gelassen werden.
- **Ganzzahl** – Dieser Attributtyp unterstützt numerische Werte. Er unterstützt auch Maßeinheiten. Es kann übersprungen oder offen gelassen werden.
- **Text** – Dieser Attributtyp unterstützt Textwerte. Er unterstützt auch einen vordefinierten Satz möglicher Werte *Aufzählung*.
- **Boolesch** – Dieser Attributtyp unterstützt Binärwerte (**TRUE** oder **FALSE**).
- **Referenz** – Dieser Typ bezieht andere Attribute.

### <a name="set-up-attribute-types"></a>Attributtypen einrichten

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Wechseln Sie zu **Produktinformationsverwaltung** &gt; **Einrichtung** &gt; **Kategorien und Attribute** &gt; **Attributtypen**.
3. Erstellen Sie zwei **Text**-Attributtypen Typ, setzen Sie die Option **Feste Liste** auf **Ja** fest, und fügen Sie anschließend einer Werteliste hinzu:

    - Nennen Sie einen Attributtyp **Objektivform** und fügen Sie die folgenden Werte hinzu: **Oval**, **Quadrat** und **Rechteck**.
    - Nennen Sie den anderen Attributtyp **Sonnenbrillen-Marke** und fügen die folgenden Werte hinzu: **Rayban**, **Flieger** und **Oakley**.

![Attributtypen](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Ein Attribut einrichten

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Wechseln Sie zu **Produktinformationsverwaltung** &gt; **Einrichtung** &gt; **Kategorien und Attribute** &gt; **Attribute**.
3. Erstellt ein Attribut mit der Bezeichnung **Objektiv**.
4. Legt das Feld **Attributtyp** auf **Objektivform** fest.

![Attribute](media/Attribute.png)

## <a name="attribute-metadata"></a>Attributmetadaten

*Attributmetadaten* lässt Sie Optionen auswählen, um anzugeben, wie deren Attribute für jedes Produkt sich verhalten sollen. So können beispielsweise auswählen, ob Attribute erforderlich sind, ob sie zum Suchen verwendet werden können und ob sie als Filter verwendet werden können.

Für Produkte können die Attributmetadateneinstellungen auf der Einzelvorgangsebene überschrieben werden. Diese Funktion wurde weiter unten in diesem Thema erläutert.

Sie sehen möglicherweise, dass die Seite **Attribute** Optionen enthält, die Attributmetadaten zugeordnet werden. Unter **Attributmetadaten für POS** betrifft eine Option mit der Bezeichnung **Kann verfeinert werden** das Verhalten der Attributwerte der Verkaufsstelle (POS) oder die Art, wie das System diese Attributwerte behandelt. Nur Attribute, für die möglicherweise die Option **Kann verfeinert werden** auf **Ja** festgelegt wurde, zeigt die Verfeinerung oder die Filter von Produkten im POS:

Hierbei gelten die verbleibenden Attributmetadatumenoptionen auf der Seite **Attribute**

- Durchsuchbar
- Abrufbar
- Kann abgefragt werden
- Sortierbar
- Mehrere Werte zulassen
- Groß-/Kleinschreibung und Format ignorieren
- Vollständige Übereinstimmung

Diese Optionen waren ursprünglich für die Verbesserung der Suchfunktion, die ursprünglich für das Onlinetool Schaufenster vorgesehen war. Obwohl Commerce den Online-Storefront nicht umfasst, enthält dieses das eCommerce Publishing Software Development Kit (SDK). Debitoren können dieses SDK verwenden, um Produkte in einen Suchenindex ihrer Wahl zu sperren. Obgleich die Produktdaten importiert werden, sollten Kunden in der Lage sein, noch durchsuchbare Daten, Daten die abgerufen werden können etc. zu unterscheiden.. Auf diese Weise können sie den optimalen Index erstellen, um sicherzustellen, dass sie nur Attribute indexieren, *die ihrer Meinung nach* indiziert werden sollen.

Informationen über den Zweck dieser verbleibenden Optionen finden Sie unter [Überblick über Suchschemas in SharePoint Server 2013](https://technet.microsoft.com/library/jj219669.aspx).

## <a name="filter-settings-for-attributes"></a>Attributfiltereinstellungen

Filtereinstellungen für Attribute lassen Sie die Filter definieren, z. B für Attribute, die im POS angezeigt werden. Um auf Filtereinstellungen für ein Attribut zuzugreifen wählen Sie auf der Seite **Attribute** das Attribut aus, und klicken Sie dann im Aktivitätsbereich auf **Filtereinstellungen**.

Die Seite **Filteranzeigeneinstellungen** enthält die folgenden Felder:

- **Name** – Per Standard wird das Feld für den Namen des Attributs festgelegt. Allerdings kann der Wert geändert werden.
- **Anzeigeoption** - Die folgenden Ausrichtungsoptionen sind verfügbar:

    - **Einzelner Wert** – Diese Option ist für die folgenden Attributtypen verfügbar: **Boolesch**, **Währung**, **Dezimal**, **Ganzzahl** und **Text**. Diese Option ermöglicht Einzelwert-Auswahl für diese Attribute im Client für Verfeinerung.
    - **Mehr-Wert** – Diese Option ist für die folgenden Attributtypen verfügbar: **Boolesch**, **Dezimal**, **Ganzzahl** und **Text**. Diese Option ermöglicht Mehrwert-Auswahl für diese Attribute im Client für Verfeinerung.

- **Anzeigeoption** - Die folgenden Ausrichtungsoptionen sind verfügbar:

    - **Liste** Diese Option ist für alle Bedarfstypen verfügbar.
    - **Bereich** – Diese Option ist für die folgenden Attributtypen verfügbar: **Währung**, **Dezimal** und **Ganzzahl**.
    - **Bereich** – Diese Option ist für die folgenden Attributtypen verfügbar: **Währung**, **Dezimal** und **Ganzzahl**.
    - **Schieberegler mit Leisten** – Diese Option ist für die folgenden Attributtypen verfügbar: **Währung**, **Dezimal** und **Ganzzahl**.

- **Schwellenwert** – Diese Einstellung ist erforderlich, wenn Sie **Bereich** als Anzeigensteuerelementtyp ausgewählt haben. Sie können Werte festlegen, indem Sie ein Trennzeichen (;) als Trennzeichen verwenden.

    Zum Beispiel für den Filter wie **Behälter-Volumen**, ein Schwellenwert kann **10; 20; 50; 100; 200; 500; 1000; 5000** sein. In diesem Fall enthält der POS die folgenden Bereiche. Sämtliche Bereiche, die keine Produkte im Resultset haben, werden grau angezeigt.

    - Weniger als 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 oder mehr

![Attributfiltereinstellungen](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Attributgruppen

Nachdem Attribute definiert wurden, können sie den Attributgruppen zugewiesen werden. Eine *Attributgruppe* dient dazu, die Attribute einer Komponente oder Unterkomponente in einem Produktkonfigurationsmodell zu gruppieren. Sie können ein Attribut in eine oder mehrere Attributgruppen einbeziehen. Attributgruppen können Benutzer unterstützen, Produkte zu konfigurieren, da die Auswahl in einem bestimmten Kontext angeordnet ist. Sie können Attributgruppen Kategorien oder Kanäle zuweisen.

Sie können Standardwerte für Attribute auch festlegen, die in einer Attributgruppe enthalten sind. So fügen Sie ein Attribut für Farbe einer Attributgruppe hinzu und wählen **Blau** als standardmäßigen Attributwert aus. In diesem Fall, wenn die Attributgruppe zu einem Produkt hinzugefügt wird, das als Farbe eines der Attribute enthält, erscheint **Blau** als die Standardfarbe für dieses Produkt.

![Attributgruppen](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Eine Attributgruppe erstellen

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Wechseln Sie zu **Produktinformationsverwaltung** &gt; **Einrichtung** &gt; **Kategorien und Attribute** &gt; **Attributtypen**.
3. Erstellen Sie eine Attributgruppe mit der Bezeichnung **Modische Sonnenbrille**.
4. Fügen Sie die folgenden Attributen hinzu: **Objektivform** und **Sonnenbrillen-Marke**.

### <a name="assign-attribute-groups-to-categories"></a>Zuweisen von Attributgruppen zu Kategorien

Mindestens eine Attributgruppe kann mit Kategorieknoten in den folgenden Arten von Kategoriehierarchien zugeordnet werden: Produkthierarchie (Commerce)-, Kanalnavigationskategoriehierarchie und ergänzende Produktkategorie der Hierarchie. Wenn Produkte kategorisiert wurden, erben sie die Attribute, die in den Attributgruppen enthalten sind.

![Produkthierarchie – Produktattributgruppen](media/AGRetailProdHierarchy.PNG)

Gehen Sie folgendermaßen vor, um Attributgruppen zu den Kategorien in der Produkthierarchie (Commerce) zuzuweisen.

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Gehen Sie zu **Retail and Commerce** &gt; **Kategorie und Produktverwaltung** &gt; **Produkthierarchie (Commerce)**.
3. Wählen Sie **Modenavigationshierarchie** aus.
4. Wählen Sie unter **Männerkleidung** die Kategorie **Hosen**, und klicken Sie dann auf dem Inforegister **Produktattributgruppen** eine Attributgruppe aus mit der Bezeichnung **Herrengurt**.
5. Wählen Sie die Kategorie **Modesonnenbrille** und überprüfen Sie die neuen Attribute in der Attributgruppe, **Modesonnenbrille** indem Sie **Attribute anzeigen** auswählen.

    Die Attributgruppe soll die Attribute neue **Objektivform** und **Sonnenbrillen-Marke** anzeigen.

6. Wählen Sie unter **Männerkleidung** die Kategorie **Hosen**, und überprüfen Sie die Attribute für **Herrengurt**, indem Sie **Attribute anzeigen** auswählen.

    Die Attributgruppe sollte **Herrengurtmarke**, **Gurtgewebe** und **Gurtgröße**-Attribute angezeigt.

> [!NOTE]
> Diese Prozedur kann auch verwendet werden, um in Attributgruppen zu kategorisieren in der Kanalnavigationskategoriehierarchie und in der Hierarchie ergänzende Produktkategorie. In Schritt 2 verwenden Sie die folgenden Navigationspfade:
>
> - Einzelhandel und Handel &gt; Kategorie und Produktverwaltung &gt; Kanalnavigationskategorien
> - Einzelhandel und Handel &gt; Kategorie und Produktverwaltung &gt; Ergänzende Produktkategorien

### <a name="assign-attribute-groups-to-stores"></a>Zuweisen von Attributgruppen zu Geschäften

Eine oder mehrere Attributgruppen kann zu einem oder mehreren Geschäften in der Geschäftshierarchie zugeordnet werden. Wenn Produkte für bestimmte Geschäfte erweitert wurden, erben sie die Attribute, die in den Attributgruppen enthalten sind.

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Wählen Sie **Einzelhandel und Handel** &gt; **Kanaleinstellung** &gt; **Kanalkategorien und Produktattribute**.
3. Weisen Sie dem Houston-Kanal Attributgruppen zu:

    1. Wählen Sie den **Houston** Kanal aus.
    2. Auf dem Inforegister **Attributgruppe** aktivieren Sie **Hinzufügen**, und dann **Name** im Feld, und wählen Sie **SharePointProvisionedProductAttributeGroup** aus.
    3. Wählen Sie wieder **Hinzufügen** und klicken Sie dann im Feld **Name** und wählen Sie **Herrengurt** aus.
    4. Wählen Sie wieder **Hinzufügen** und klicken Sie dann im Feld **Name** und wählen Sie **Modesonnenbrille** aus.

        > [!NOTE]
        > Eine Option ermöglicht es anzugeben, dass dieser Kanal die Attributgruppen von seinem Kanal in der übergeordneten Hierarchie übernehmen soll. Ist der Option **Erben** auf **Ja**, erbt der untergeordnete Kanalknoten alle Attributgruppen und alle Attribute in Attributgruppen.

4. Aktivieren Sie die Attribute, sodass sie im Houston-Kanal verfügbar sind:

    1. Klicken Sie im Aktivitätsbereich auf **Attributmetadaten festlegen**.
    2. Wählen Sie **Mode**, und dann Kategorieknoten und dann auf dem Inforegister **Kanalproduktattribute** wählen Sie **Attribut einschließen** für jedes Attribut aus.
    3. Wählen Sie **Modezubehör** und dann Kategorieknoten und dann **Modesonnenbrille** und dann auf der Registerkarte **Kanalproduktattribute** wählen Sie **Attribut einschließen** für jedes Attribut aus.
    4. Wählen Sie den **Herrenkleidung** Kategorieknoten und dann **Hosen** und dann auf der Registerkarte **Kanalproduktattribute** wählen Sie **Attribut einschließen** für jedes Attribut aus.

![Kanalkategorien und Produktattribute – Attributgruppen](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Überschreiben von Attributwerten

Die Standardwerte von Attributen können auf der Produktebene überschrieben werden. Die Standardwerte von Attributen können für einzelne Produkte in bestimmten Katalogen überschrieben werden, die für bestimmte Kanäle ausgerichtet werden.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Überschreiben Sie die Attributwerte eines Einzelprodukts

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Gehen Sie zu **Einzelhandel und Handel** &gt; **Kategorie und Produktverwaltung** &gt; **Freigegebene Produkte nach Produkthierarchie**.
3. Wählen Sie den Kategorieknoten &gt; **Mode** &gt; **Mode-Accessoires** **Mode-Sonnenbrille** aus.
4. Wählen Sie das erforderliche Produkt im Raster aus. Klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Verwalten** auf **Produktattribut**.
5. Wählen Sie ein Attribut im linken Bereich aus, und aktualisieren Sie anschließend den Wert im rechten Bereich.

![Produkthierarchie – Produktattributgruppen](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Überschreiben Sie die Attributwerte eines Einzelprodukts in einem Katalog

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Gehen Sie zu **Einzelhandel und Handel** &gt; **Katalogverwaltung** &gt; **Alle Kataloge**.
3. Wählen Sie **Fabrikam-Basiskatalog**.
4. Wählen Sie den Kategorieknoten &gt; **Mode** &gt; **Mode-Accessoires** **Mode-Sonnenbrille** aus.
5. Auf dem Inforegister **Produkte** aktivieren Sie das erforderliche Produkt aus, und wählen Sie anschließend **Attribute** über dem Produktraster aus.
6. Auf den folgenden Inforegistern aktualisieren Sie die Werte die erforderlichen Attribute:

    - Gemeinsam genutzte Produktmedien
    - Gemeinsam genutzte Produktattribute
    - Kanalmedien
    - Kanalspezifische Produktattribute

    > [!NOTE]
    > Wenn Produktmedien freigegebene und freigegebene Produktattribute erstellt werden, gelten sie für alle Produkte.

![Katalog-Produktattributwertgruppen](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Überschreiben Sie die Attributwerte eines Einzelprodukts in einem Kanal

1. Melden Sie sich beim Backoffice Client als Einzelverkaufsmanager an.
2. Wählen Sie **Einzelhandel und Handel** &gt; **Kanaleinstellung** &gt; **Kanalkategorien und Produktattribute**.
3. Wählen Sie den **Houston** Kanal aus.
4. Auf dem Inforegister **Produkte** aktivieren Sie das erforderliche Produkt aus, und wählen Sie anschließend **Attribute** über dem Produktraster aus.

    > [!NOTE]
    > Wenn keine Produkte vorrätig sind, fügen Sie Produkte hinzu, indem Sie auf dem Inforegister **Hinzufügen** **Produkte** auswählen und dann die erforderlichen Produkte im Dialogfeld **Produkte hinzufügen** auswählen.

5. Auf den folgenden Inforegistern aktualisieren Sie die Werte die erforderlichen Attribute:

    - Gemeinsam genutzte Produktmedien
    - Gemeinsam genutzte Produktattribute
    - Kanalmedien
    - Kanalspezifische Produktattribute

    > [!NOTE]
    > Wenn Produktmedien freigegebene und freigegebene Produktattribute erstellt werden, gelten sie für alle Produkte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]