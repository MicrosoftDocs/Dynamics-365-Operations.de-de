---
title: Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen
description: Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für vordefinierte Produktvarianten eingerichtet wird und sie der passenden Produktdimensionsgruppe zugeordnet werden kann.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550582"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für vordefinierte Produktvarianten eingerichtet wird und sie der passenden Produktdimensionsgruppe zugeordnet werden kann. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Die neue Produktnummernnomenklatur wird der Produktdimensionsgruppe Farbe und Größe zuweisen. Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Erstellen eine Produktnummerbezeichnung
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktbezeichnung".
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld Name einen Nomenklaturnamen ein, der die Zielproduktdimensionsgruppe identifiziert (beispielsweise ColorSize).
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Klicken Sie auf Hinzufügen.
7. Klicken Sie auf "Produktmasternummer".
8. Klicken Sie auf Hinzufügen.
9. Klicken Sie auf Textkonstante.
10. Geben Sie im Feld "Text" einen Wert ein.
11. Klicken Sie auf Hinzufügen.
12. Klicken Sie auf "Farbe".
13. Klicken Sie auf Hinzufügen.
14. Klicken Sie auf Textkonstante.
15. Geben Sie im Feld "Text" einen Wert ein.
16. Klicken Sie auf Hinzufügen.
17. Klicken Sie auf Größe.
18. Schließen Sie die Seite.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Zuweisen der Nomenklatur zu einem Produktmaster
1. Klicken Sie auf "Produktdimensionsgruppen".
2. Wählen Sie die Dimensionsgruppe "SizeCol".
3. Klicken Sie auf Bearbeiten.
4. Wählen Sie "Ja" im Feld "Bezeichnungen verwenden".
5. Geben Sie im Feld "Produktvariantennummerbezeichnung" eine Bezeichnung ein oder wählen Sie eine aus.
6. Schließen Sie die Seite.

