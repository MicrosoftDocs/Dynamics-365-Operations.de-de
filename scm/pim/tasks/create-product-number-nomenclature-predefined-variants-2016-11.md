--- 
title: "Produktnummer für vordefinierte Produktvarianten erstellen"
description: "Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für vordefinierte Produktvarianten eingerichtet wird und sie der passenden Produktdimensionsgruppe zugeordnet werden kann."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f14ee57564ad70bb7f28cd9274fc97d07974ec32
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Produktnummer für vordefinierte Produktvarianten erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

