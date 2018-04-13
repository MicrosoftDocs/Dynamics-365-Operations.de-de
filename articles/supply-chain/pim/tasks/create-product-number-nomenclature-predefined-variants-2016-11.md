--- 
title: "Produktnummer für vordefinierte Produktvarianten erstellen"
description: "Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für vordefinierte Produktvarianten eingerichtet wird und sie der passenden Produktdimensionsgruppe zugeordnet werden kann."
author: BibiSp
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c423aab341ddad9383c4c95b9dbb63c9875c99ef
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Produktnummer für vordefinierte Produktvarianten erstellen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für vordefinierte Produktvarianten eingerichtet wird und sie der passenden Produktdimensionsgruppe zugeordnet werden kann. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Die neue Produktnummernnomenklatur wird der Produktdimensionsgruppe Farbe und Größe zuweisen. Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Erstellen eine Produktnummerbezeichnung
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktbezeichnung".
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Name" einen Bezeichnungsnamen ein, der die Zielproduktdimensionsgruppe identifiziert, beispielsweise ColorSize.
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


