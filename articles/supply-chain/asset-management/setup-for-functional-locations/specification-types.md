---
title: Wartungsattributtypen
description: In diesem Artikel wird erläutert, wie Sie in Attributtypen in Anlagenverwaltung erstellen.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a0aca3ccf24505c064ad59f0adafb771056ba95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887659"
---
# <a name="maintenance-attribute-types"></a>Wartungsattributtypen

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel wird erläutert, wie Sie in Attributtypen in Anlagenverwaltung erstellen. Attribute werden verwendet, um die Eigenschaften verschiedener Elemente zu beschreiben. Sie können Attribute für die folgenden Elemente einrichten:

- [Funktionale Standorttypen](../setup-for-functional-locations/functional-location-types.md)
- [Funktionale Standorte erstellen](../functional-locations/create-functional-locations.md)
- [Anlagentypen](../setup-for-objects/object-types.md)
- Anlagen

Die Attribute, die Sie einrichten können, variieren, je nach spezifischem Element. Für einen funktionalen Standort können Sie beispielsweise Attribute für die Konfiguration und physische Größe des Standorts einrichten. Für einen Anlagentyp oder eine Anlage können Sie Attribute für Modulvolumen, Stromverbrauch und die maximale Ladungskapazität unter verschiedene Bedingungen einrichten.

## <a name="create-attribute-types"></a>Erstellen von Attributtypen

Sie können eigene Attributtypen erstellen. Darüber hinaus können Sie Produktdimensionen auf die Seite **Attributtypen** übertragen.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Attributtypen** aus.
2. Beim der erstmaligen Einrichtung von Attributtypen wählen Sie **Produktdimensionen erstellen** aus, um Standardproduktdimensionen automatisch zu übertragen.
3. Wählen Sie **Neu** aus, um einen neuen Attributtyp zu erstellen.
4. Geben Sie im Feld **Attributtyp** einen Namen für den Attributtyp ein.
5. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
6. Wählen Sie im Feld **Einheit** die benötigte Attributeinheit aus.
7. Wählen Sie im Feld **Datentyp** einen Datentyp für die Einheit aus.
8. Wenn Sie **Zeichenfolge** als Datentyp ausgewählt haben, gehen Sie folgendermaßen vor, um Werte für den Attributtyp zu erstellen:

    1. Wählen Sie den Attributtyp und dann **Werte** aus.
    2. Wählen Sie im Feld **Attributwerte** die Option **Neu** aus.
    3. Wählen Sie im Feld **Attributtyp** einen Attributtyp (Dimension) aus.
    4. Geben Sie im Feld **Wert** einen zugehörigen Wert ein.
    5. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
    6. Speichern Sie den Datensatz.
    7. Kehren Sie zur Seite **Attributtypen** zurück.

9. Speichern Sie den Datensatz.

    Das Feld **Funktionale Standorttypen** zeigt die Anzahl der funktionalen Standorte an, die den Attributtyp verwenden. Das Feld **Anlagentypen** zeigt die Anzahl von Anlagentypen an, die ihn verwenden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]