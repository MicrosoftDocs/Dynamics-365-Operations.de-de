---
title: Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen
description: Dieses Thema erklärt, wie eine Produktnummernbezeichnung für vordefinierte Produktvarianten eingerichtet wird und der passenden Produktdimensionsgruppe zugeordnet werden kann.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cf0efeac2851e6ead6fc5e15a016370dfa620bc
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914906"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Produktnummernbezeichnung für vordefinierte Produktvarianten erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

