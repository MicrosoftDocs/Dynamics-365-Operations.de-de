---
title: Eine Variantengruppe erstellen
description: In diesem Thema wird beschrieben, wie Sie eine Größen-, Stil- oder Farbvariantengruppe für ein Produkt in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4c34aca043f10fef38f186800c429cac36c41ce7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207846"
---
# <a name="create-a-variant-group"></a>Eine Variantengruppe erstellen


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine Größen-, Stil- oder Farbvariantengruppe für ein Produkt in Microsoft Dynamics 365 Commerce erstellen.

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce unterstützt mehrere Varianten für Produkte. Es ist ideal, Variantengruppen für verschiedene Produktkategorien einzurichten. Beispielsweise kann eine Größengruppe für T-Shirts mit besonders kleinen, mittleren, großen und besonders großen Größen erstellt werden, oder es kann eine Farbgruppe erstellt werden, die alle verfügbaren Farben eines Produkts enthält. Variantengruppen sollten hinzugefügt werden, bevor Produkte hinzugefügt werden.

In diesem Thema wird eine Größengruppe erstellt und konfiguriert. Ähnliche Verfahren können zum Hinzufügen und Konfigurieren von Stilgruppen und Farbgruppen verwendet werden.

## <a name="create-a-size-group"></a>Eine Größengruppe erstellen

Gehen Sie folgendermaßen vor, um eine Größengruppe zu erstellen.
 
1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Variantengruppen \>. Größengruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Größengruppe** einen Namen für die Größengruppe ein.
1. Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.
1. Wählen Sie im Aktivitätsbereich **Speichern** aus.

## <a name="add-attributes-to-the-size-group"></a>Der Größengruppe Attribute hinzufügen

Um Attribute zu einer Größengruppe hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Variantengruppen \> Größengruppen**.
1. Wählen Sie im Navigationsbereich eine Größengruppe aus.
1. Wählen Sie unter **Größengruppenlinien** die Option **Hinzufügen**.
1. Geben Sie im Feld **Größe** eine Zeichenfolge für die Größe ein (zum Beispiel „XL”).
1. Geben Sie in das Feld **Größenbezeichnung** einen Namen für die Größe ein (z. B. „Extra groß”).
1. Geben Sie im Feld **Auffüllungsgewicht** eine Zahl ein, die das Auffüllungsgewicht darstellt.
1. Geben Sie in das Feld **Nummer in Strichcode** eine Zahl ein, die den Strichcode darstellt.
1. Geben Sie im Feld **Anzeigereihenfolge** eine Nummer ein, die die Anzeigereihenfolge darstellt.
1. Wenn Sie mit dem Hinzufügen von Größen fertig sind, wählen Sie **Speichern** im Aktivitätsbereich.

Die folgende Abbildung zeigt ein Beispiel für die Größengruppe für „lässige Shirtgrößen”

![Größengruppe erstellen](media/create-variant-group.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Produktinformationsübersicht](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Einzelhandelsprodukte einrichten](set-up-retail-products.md)

[Produktdimensionen](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]