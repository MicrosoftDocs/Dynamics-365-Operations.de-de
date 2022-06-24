---
title: Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen
description: Dieser Artikel erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77c8eabe1657f7fbfef71747627207dccff3b60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887311"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen

[!include [banner](../../includes/banner.md)]

Dieser Artikel erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Die neue Produktnummernnomenklatur wird der Produktdimensionsgruppe Farbe und Größe zuweisen. Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Erstellen eine Produktnummerbezeichnung

1. Wechseln Sie zu **Produktinformationsmanagement \> Einrichten \> Produktbezeichnung**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Name** einen Bezeichnungsnamen ein, der die Zielproduktdimensionsgruppe identifiziert (beispielsweise `ColorSize`).
1. Geben Sie im Feld **Beschreibung** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Produktmaster**-Nummer aus.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Textkonstante** aus.
1. Geben Sie im Feld **Text** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Farbe** aus.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Textkonstante** aus.
1. Geben Sie im Feld **Text** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Größe** aus.
1. Schließen Sie die Seite.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Zuweisen der Nomenklatur zu einem Produktmaster

1. Wählen Sie **Produktdimensionsgruppen** aus.
2. Wählen Sie die Gruppe **SizeCol-Produktdimension** aus.
3. Wählen Sie **Bearbeiten** aus.
4. Wählen Sie **Ja** im Feld **Bezeichnungen verwenden** aus.
5. Geben Sie im Feld **Produktvariantennummerbezeichnung** einen Wert ein oder wählen Sie einen Wert aus.
6. Schließen Sie die Seite.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]