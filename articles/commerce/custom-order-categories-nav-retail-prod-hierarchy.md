---
title: Sortierreihenfolge bei Verkaufsentitäten ändern
description: In diesem Artikel werden die Konzepte erläutert, die zum Steuern der Anzeigereihenfolge für verschiedene verkaufsbezogene Entitäten in Dynamics 365 Commerce zugeordnet werden.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265835"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Ändern Sie die Sortierreihenfolge für Verkaufsentitäten


[!Include [banner](includes/banner.md)]

Einzelhändler erachten die Produkterfassung als ein primäres Tool für Debitoreninteraktionen über alle Kanäle hinweg. Es gibt mehrere Funktionen, die Kunden dabei helfen können, Produkte einfach zu entdecken. So können Kunden zum Beispiel Kategorien, Suchen und Filter durchsuchen.

In diesem Artikel werden die Konzepte erläutert, die zum Steuern der Anzeigereihenfolge für verschiedene verkaufsbezogene Entitäten zugeordnet werden. Es wird auch erklärt, wie Sie die Sortierreihenfolge ändern.

## <a name="overview"></a>Übersicht

In Commerce ist das Sortieren verschiedener auf die merchandisingbezogener Instanzen an bestehenden Kundenszenarien ausgerichtet und erfordert keine Erweiterungen von Implementierungspartnern mehr.

In den Commerce-Versionen bis 10.0.5 war die Sortierreihenfolge für Kategorien in der Navigationshierarchie alphabetisch. Mit den aktuellen benutzerdefinierten Sortierreihenfolgenfunktionen können Verkaufsmanager die Sortierreihenfolge für verschiedene verkaufsbezogene Entitäten für alle Endbenutzerkunden konfigurieren. Diese Kunden umfassen Headquarters (HQ) und Callcenter.

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

![Produkthierarchie: Benutzerdefinierte Sortierung mit negativen Werten.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Freigegebene Produkte nach Kategorie: Benutzerdefinierte Sortierung auf Basis der Produkthierarchie.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

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

![Kanalnavigationshierarchie: Benutzerdefinierte Sortierung.](./media/ChannelNavCustomSorted.png)

![Katalognavigationshierarchie: Benutzerdefinierte Sortierung auf Basis der Kanalnavigationshierarchie.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS mit benutzerdefiniert sortierten Kategorien.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Standardmäßig ist die Funktion **Anzeigereihenfolge für Merchandisinginstanzen aktivieren** ausgeschaltet. Sie können Sie mit der [Funktionsverwaltung](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) einzuschalten. Nachdem Sie die Funktion eingeschaltet haben, führen Sie den CDX-Auftrag **Globale Konfiguration -1110** aus dem Vertriebsplan aus.
> Wenn Ihre Kategorienreihenfolge in POS nicht aktualisiert wird, reaktivieren Sie das Gerät. Kategorieinformationen werden abgerufen, wenn das Gerät aktiviert wird, sodass das Gerät die Kategorieinformationen möglicherweise mit aktualisierten Anzeigereihenfolgen erneut abrufen muss. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
