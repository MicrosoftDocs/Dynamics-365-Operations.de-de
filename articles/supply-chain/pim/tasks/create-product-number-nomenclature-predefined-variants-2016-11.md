---
title: Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen
description: Dieses Thema erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a15d1f4ecbf85e22bfadc1dd680d24bc56d807f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007540"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen

[!include [banner](../../includes/banner.md)]

Dieses Thema erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Die neue Produktnummernnomenklatur wird der Produktdimensionsgruppe Farbe und Größe zuweisen. Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Erstellen eine Produktnummerbezeichnung
1. Wählen Sie **Produktvariantenmodell-Definition** aus.
2. Wählen Sie **Produktbezeichnung** aus.
3. Wählen Sie **Neu** aus.
4. Geben Sie im Feld **Name** einen Bezeichnungsnamen ein, der die Zielproduktdimensionsgruppe identifiziert (beispielsweise `ColorSize`).
5. Geben Sie im Feld **Beschreibung** einen Wert ein.
6. Wählen Sie **Hinzufügen** aus.
7. Wählen Sie **Produktmaster**-Nummer aus.
8. Wählen Sie **Hinzufügen** aus.
9. Wählen Sie **Textkonstante** aus.
10. Geben Sie im Feld **Text** einen Wert ein.
11. Wählen Sie **Hinzufügen** aus.
12. Wählen Sie **Farbe** aus.
13. Wählen Sie **Hinzufügen** aus.
14. Wählen Sie **Textkonstante** aus.
15. Geben Sie im Feld **Text** einen Wert ein.
16. Wählen Sie **Hinzufügen** aus.
17. Wählen Sie **Größe** aus.
18. Schließen Sie die Seite.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Zuweisen der Nomenklatur zu einem Produktmaster
1. Wählen Sie **Produktdimensionsgruppen** aus.
2. Wählen Sie die Gruppe **SizeCol-Produktdimension** aus.
3. Wählen Sie **Bearbeiten** aus.
4. Wählen Sie **Ja** im Feld **Bezeichnungen verwenden** aus.
5. Geben Sie im Feld **Produktvariantennummerbezeichnung** einen Wert ein oder wählen Sie einen Wert aus.
6. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]