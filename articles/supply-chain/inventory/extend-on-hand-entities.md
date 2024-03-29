---
title: Erweitern vorhandener Dateneinheiten
description: In diesem Artikel finden Sie ein Beispiel, das zeigt, wie Sie den Ansichten INVENTORSITEONHANDENTITY und INVENTWAREHOUSEONHANDENTITY erweiterte Felder hinzufügen, damit die Funktionen der Inventardateneinheiten mit den Erweiterungen arbeiten können.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 352b466a185bcd0778ea17e598129864c1547987
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906036"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Erweitern vorhandener Dateneinheiten

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management bietet die Funktionen von [Erweiterbarkeit](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md), mit denen Sie [Felder durch Erweiterung in Tabellen einfügen](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md) können. In diesem Artikel finden Sie ein Beispiel, das zeigt, wie Sie den Ansichten `INVENTORSITEONHANDENTITY` und `INVENTWAREHOUSEONHANDENTITY` erweiterte Felder hinzufügen, damit die Funktionen der Inventardateneinheiten mit den Erweiterungen arbeiten können. Ausführliche Informationen zu Dateneinheiten finden Sie unter [Datenverwaltungsübersicht](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Hier ist eine Liste einiger verfügbarer Inventardateneinheiten:
>
> - Verfügbarer Lagerbestand nach Standort
> - Verfügbarer Lagerbestand nach Standort V2
> - Lagerbestand nach Lagerort
> - Verfügbarer Lagerbestand nach Lagerort v2

Nachdem Sie Tabellen Felder hinzugefügt haben, die von der Ansicht `inventSiteOnHandView` verwendet werden, muss der Engine synchronisiert werden, damit die Erweiterungen korrekt erkannt werden.

1. Erweitern Sie die Ansicht `InventSiteOnHandView`, indem Sie das Erweiterungsfeld hinzufügen.
1. Erweitern Sie die Ansicht `InventSiteOnHandAggregatedView` mit den Erweiterungsfeldern.
1. Erweitern Sie die `InventSiteOnHandAggregatedViewBuilder`viewBuilder-Klasse durch Ändern der `getExtensionFields()`-Methode. Auf diese Weise ordnen Sie alte Ansichtsfelder neuen Ansichtsfeldern zu, wenn die viewBuilder-Synchronisierung ausgeführt wird.

Beispielsweise haben Sie die folgenden vier Felder durch Erweiterung in die Tabelle `InventTable` eingefügt:

- Benutzerdefiniertes Feld 1
- Benutzerdefiniertes Feld 2
- Benutzerdefiniertes Feld 3
- Benutzerdefiniertes Feld 4

In diesem Fall müssen Sie die Methode `getExtensionFields()` auf folgende Weise ändern.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Nachdem Sie diese Schritte ausgeführt haben, können Sie den Lagerbestand nach Standort und den Lagerbestand nach Lagerdateneinheiten erweitern, indem Sie die neuen Felder hinzufügen. Auf diese Weise stellen Sie sicher, dass die erweiterten Felder während der Datenmigration, die diese Datenentitäten verwendet, erkannt und eingeschlossen werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]