---
title: Anlagenhersteller und -modelle
description: In diesem Artikel wird erläutert, wie Anlagenhersteller und zugehörige Modelle in Anlagenverwaltung eingerichtet werden.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95d0998bbacef7a4350d0fd0a58259ec35759d28
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868100"
---
# <a name="asset-manufacturers-and-models"></a>Anlagenhersteller und -modelle

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel wird erläutert, wie Anlagenhersteller und zugehörige Modelle in Anlagenverwaltung eingerichtet werden. Modelle können Anlagentypen zugeordnet sein.

## <a name="set-up-product-model-relations"></a>Produktmodellbeziehungen einrichten

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Hersteller und Modell** aus.
2. Wählen Sie **Neu** aus, um ein neues Produkt zu erstellen.
3. Geben Sie im Feld **Hersteller** den Namen des Anlagenherstellers ein.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie auf dem Inforegister **Modelle** die Option **Hinzufügen** aus, um ein Anlagenmodell zu erstellen, das dem Anlagenhersteller zugeordnet werden soll.
6. Geben Sie im Feld **Modell** einen Namen für das Anlagenmodell ein.
7. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
8. Wählen Sie im Feld **Anlagentyp** den Anlagentyp aus, dem das Herstellermodell zugeordnet werden soll.

    > [!NOTE]
    > Sie können Zuordnungen für Anlagentypen, -hersteller und -modelle auch in der Suche **Anlagentypen** einrichten. Weitere Informationen finden Sie unter [Anlagentypen](../setup-for-objects/object-types.md).

    Auf dem Inforegister **Details** wird im Feld **Modelle** die Anzahl der Anlagenmodelle angezeigt, die für den ausgewählten Anlagenhersteller eingerichtet sind. Das Feld **Anlagen** zeigt die Anzahl der Anlagen, die den ausgewählten Hersteller verwenden.
    
    Das Feld **Anlagen** zeigt die Anzahl der Objekte, die das Herstellermodell verwenden.

> [!NOTE]
> Für einen Anlagentyp können keine Anlagenherstellermodell-Zuordnungen vorliegen, er kann einem Anlagenherstellermodell zugeordnet sein, oder er kann mehreren Anlagenherstellermodellen zugeordnet sein. Wenn ein Anlagentyp mindestens einem Herstellermodell zugeordnet ist, können nur die Kombinationen, die in der Suche **Herstellermodell** eingerichtet sind, auf den Asset Management-Seiten ausgewählt werden, für die eine Kombination aus Anlagentyp, -hersteller und -modell eingerichtet werden kann. Zu diesen Seiten gehören **Alle Anlagen**, **Anlagenservicelevel**, **Einzelvorgangstypstandards** und **Wartungsbudgetpositionen**. Wenn einige Anlagentypen keinem Herstellermodell zugeordnet sind, werden auf den Seiten nur diese Anlagentypen und Herstellermodelle angezeigt, die ebenfalls keinen Anlagentypen zugeordnet sind.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Wählen Sie einen Hersteller und ein Modell für ein Objekt aus.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**.
2. Wählen Sie in der Spalte **Anlage** den Link für die Anlage aus. Die Seite **Details** wird angezeigt.
3. Wählen Sie **Bearbeiten** aus.
4. Wählen Sie auf dem Inforegister **Allgemein** Werte in den Feldern **Hersteller** und **Modell** aus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]