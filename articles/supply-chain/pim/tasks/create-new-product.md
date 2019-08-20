---
title: Neues Produkt erstellen
description: In diesem Thema wird beschrieben, wie Sie ein neues freigegebenes Produkt erstellen.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844800"
---
# <a name="create-a-new-product"></a>Neues Produkt erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird beschrieben, wie Sie ein neues freigegebenes Produkt erstellen. Es wird in der Regel von einem Produktdesigner ausgeführt. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.


## <a name="create-a-product"></a>Ein Produkt erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Produktinformationsverwaltung > Produkte > Produkte**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Produktnummer** einen Wert ein. Wenn kein Nummernkreis für die Produktnummer eingerichtet wurde, muss er manuell eingegeben werden.  
4. Geben Sie im Feld **Produktname** einen Wert ein. Der Produktname wird standardmäßig zum Suchbegriff. Diesen Wert können Sie bei Bedarf ändern.  
5. Wählen Sie **OK**.

## <a name="set-up-dimension-groups"></a>Richten Sie Dimensionsgruppen ein
1. Klicken Sie auf **Dimensionsgruppen**, um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld **Lagerdimensionsgruppe** einen Wert ein, oder wählen Sie einen Wert aus. Die Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen Sie zu jeder Transaktion für das Produkt eingeben müssen und wie es im Bestand nachverfolgt wird.  
3. Geben Sie im Feld **Rückverfolgungsgruppe** einen Wert ein, oder wählen Sie einen Wert aus. Die Rückverfolgungsangabengruppe bestimmt, welche Rückverfolgungsangaben Sie für jede Transaktion für das Produkt eingeben müssen und wie es im Bestand behandelt wird.  
4. Wählen Sie **OK**.

