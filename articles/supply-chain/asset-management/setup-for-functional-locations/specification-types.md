---
title: Wartungsattributtypen
description: In diesem Thema wird erläutert, wie Sie in Attributtypen in Asset Management erstellen.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783286"
---
# <a name="maintenance-attribute-types"></a>Wartungsattributtypen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie in Attributtypen in Asset Management erstellen. Attribute werden verwendet, um die Eigenschaften verschiedener Elemente zu beschreiben. Sie können Attribute für die folgenden Elemente einrichten:

- [Funktionale Standorttypen](../setup-for-functional-locations/functional-location-types.md)
- [Funktionale Standorte](../functional-locations/create-functional-locations.md)
- [Anlagentypen](../setup-for-objects/object-types.md)
- Anlagen

Die Attribute, die Sie einrichten können, variieren, je nach spezifischem Element. Für einen funktionalen Standort können Sie beispielsweise Attribute für die Konfiguration und physische Größe des Standorts einrichten. Für einen Anlagentyp oder eine Anlage können Sie Attribute für Modulvolumen, Stromverbrauch und die maximale Ladungskapazität unter verschiedene Bedingungen einrichten.

## <a name="create-attribute-types"></a>Erstellen von Attributtypen

Sie können eigene Attributtypen erstellen. Darüber hinaus können Sie Produktdimensionen aus Microsoft Dynamics 365 for Finance and Operations auf die Seite **Attributtypen** übertragen.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Attributtypen** aus.
2. Beim der erstmaligen Einrichtung von Attributtypen wählen Sie **Produktdimensionen erstellen** aus, um Standardproduktdimensionen von Finance and Operations automatisch zu übertragen.
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