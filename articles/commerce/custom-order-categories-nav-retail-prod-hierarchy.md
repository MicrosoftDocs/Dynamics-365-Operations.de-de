---
title: Ändern Sie die Sortierreihenfolge für Verkaufsentitäten
description: In diesem Thema werden die Konzepte erläutert, die zum Steuern der Anzeigereihenfolge für verschiedene verkaufsbezogene Entitäten in Dynamics 365 Commerce zugeordnet werden.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54929f924bd9c2b59dec453cf580e0b2bc149d38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799468"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Ändern Sie die Sortierreihenfolge für Verkaufsentitäten


[!include [banner](includes/banner.md)]

Einzelhändler erachten die Produkterfassung als ein primäres Tool für Debitoreninteraktionen über alle Kanäle hinweg. Verschiedene Funktionen können Debitoren helfen, Produkte einfacher zu ermitteln. So können sie Kategorien, Suchen und Filter durchsuchen.

In diesem Thema werden die Konzepte erläutert, die zum Steuern der Anzeigereihenfolge für verschiedene verkaufsbezogene Entitäten zugeordnet werden. Es wird auch erklärt, wie Sie die Sortierreihenfolge ändern.

## <a name="overview"></a>Übersicht

Die Unterstützung zur Sortierung von verschiedenen verkaufsbezogenen Entitäten wurde verbessert. Diese Unterstützung ist nun besser auf Szenarien mit Bestandskunden ausgerichtet, die zuvor Erweiterungen von Implementierungspartnern erforderlich machten.

In Retail-Versionen vor Version 10.0.5 war die Sortierreihenfolge für Kategorien in der Navigationshierarchie alphabetisch. Mit den neuen benutzerdefinierten Sortierreihenfolgenfunktionen können Verkaufsmanager die Sortierreihenfolge für verschiedene verkaufsbezogene Entitäten für alle Endbenutzerkunden konfigurieren. Diese Kunden umfassen Headquarters (HQ) und Callcenter.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Konfigurieren der Anzeigereihenfolge für Kategorien in der Produkthierarchie

Bevor Sie dieses Verfahren ausführen können, müssen Demodaten in Ihrer Umgebung installiert werden.

1. Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Commerce-Produkthierarchie**.
2. Klicken Sie auf **Kategoriehierarchie bearbeiten**.
3. Klicken Sie auf **Bearbeiten**.
4. Erweitern Sie in der Struktur **ALLE \> Aktivität Sport**.
5. Erweitern Sie in der Struktur **ALLE \> Team-Sport**.
6. Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein. (Die Zahl kann negativ sein.)
7. Wiederholen Sie die Schritte 4 bis 6 für zusätzliche Kategorien, für die Sie die Reihenfolge ändern möchten.

Der Anzeigereihenfolge für die Kanalnavigationshierarchie wird in HQ für die Produkthierarchie und freigegebene Produkte nach Kategorie angezeigt.

![Produkthierarchie: Benutzerdefinierte Sortierung mit negativen Werten](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Freigegebene Produkte nach Kategorie: Benutzerdefinierte Sortierung auf Basis der Produkthierarchie](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Konfigurieren der Anzeigereihenfolge für Kategorien in der Kanalnavigationshierarchie

Bevor Sie dieses Verfahren ausführen können, müssen Demodaten in Ihrer Umgebung installiert werden.

1. Gehen Sie zu **Retail and Commerce \> Produkte und Kategorien \> Kanalnavigationskategorien**.
2. Wählen Sie in der Liste die **Modenavigation**-Hierarchie aus.
3. Klicken Sie auf **Kategoriehierarchie bearbeiten**.
4. Klicken Sie auf **Bearbeiten**.
5. In der Struktur wählen Sie **Mode \> Damenmode \> Damenschuhe** aus.
6. Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein.
7. In der Struktur wählen Sie **Mode \> Damenmode \> Oberteile** aus.

    Ebenso können Sie die Sortierreihenfolge für die Unterkategorien definieren.

8. In der Struktur wählen Sie **Mode \> Herrenmode \> Freizeithemden** aus.
9. Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein.
10. In der Struktur wählen Sie **Mode \> Herrenmode \> Mäntel & Jacken** aus.
11. Geben Sie im Feld **Anzeigereihenfolge** eine Zahl ein.
12. Wiederholen Sie dies für alle weiteren Kategorien, für die Sie die Reihenfolge ändern möchten.

Der Anzeigereihenfolge für die Kanalnavigationshierarchie wird in HQ, im Katalog und in Kanälen angezeigt.

![Kanalnavigationshierarchie: Benutzerdefinierte Sortierung](./media/ChannelNavCustomSorted.png)

![Katalognavigationshierarchie: Benutzerdefinierte Sortierung auf Basis der Kanalnavigationshierarchie](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS mit benutzerdefiniert sortierten Kategorien](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Standardmäßig ist die Funktion für die benutzerdefinierte Sortierreihenfolge deaktiviert. Um zu erfahren, wie Sie diese Funktion und andere Funktionen aktivieren können, siehe [Funktionsverwaltung](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]