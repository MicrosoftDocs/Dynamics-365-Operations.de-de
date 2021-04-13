---
title: Nach Zuordnung einer neuen Website werden Produkte und Kategorien nicht im Commerce-Website-Generator angezeigt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Zuordnen einer neuen Website nicht im Commerce-Website-Generator angezeigt werden.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 46ad73256e5acf6d42772fc4af154a8d74206bbb
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585344"
---
# <a name="products-and-categories-dont-appear-in-commerce-site-builder-after-a-new-site-is-mapped"></a>Nach Zuordnung einer neuen Website werden Produkte und Kategorien nicht im Commerce-Website-Generator angezeigt

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Zuordnen einer neuen Website nicht im Commerce-Website-Generator angezeigt werden.

## <a name="description"></a>Beschreibung

Produkte und Kategorien werden nicht im Commerce-Website-Generator angezeigt, nachdem eine neue Website zugeordnet wurde.

## <a name="resolution"></a>Lösung

### <a name="add-products-to-channel-categories-in-commerce-headquarters"></a>Kanalkategorien Produkte in der Commerce-Zentralverwaltung hinzufügen

Befolgen Sie diese Schritte, um Kanalkategorien Produkte in der Commerce-Zentralverwaltung hinzuzufügen.

1. Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.
1. Wählen Sie in der linken Navigation die Kategorie aus, die auf der E-Commerce-Website angezeigt werden soll.
1. Wählen Sie im Inforegister **Produkte** die Option **Hinzufügen** aus.
1. Wählen Sie im Abschnitt **Verfügbare Produkte** die Produkte aus, die angezeigt werden sollen. Wählen Sie dann **Hinzufügen** aus.
1. Wählen Sie **OK**.
1. Wählen Sie im Aktionsbereich die Option **Kanalupdates veröffentlichen** aus, sobald die Produkte im Inforegister **Produkte** angezeigt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einen Kanal zur Verwendung einer Kanalnavigationshierarchie konfigurieren](../configure-channel-hierarchy.md)