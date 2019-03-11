---
title: Kuppelprodukte aus einer vorhandenen Formel kopieren
description: Diese Prozedur zeigt Ihnen an, wie Sie Co-Produkte aus einer vorhandenen Formelversion zu einer anderen Formelversion für ein freigegebenes Produkt kopieren.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179c12da0c2ddc7b5e2f2fdddd21168eac121811
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "319246"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>Kuppelprodukte aus einer vorhandenen Formel kopieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen an, wie Sie Co-Produkte aus einer vorhandenen Formelversion zu einer anderen Formelversion für ein freigegebenes Produkt kopieren. Es ist eine Voraussetzung, dass es mindestens eine Formelversion gibt, die Co-Produkten zugeordnet ist. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USP2.


## <a name="find-a-released-product"></a>Suchen eines freigegebenen Produktes
1. Wechseln Sie zu "Freigegebene Produkte".
2. Klicken Sie auf "Filter anzeigen".
    * Sie sind im Begriff, das Feld "Produktionstyp" im Filterdialogfeld hinzuzufügen.  
3. Klicken Sie auf "Einen Filter hinzufügen", um das Feld "Produktionstyp" hinzuzufügen.
    * Im nächsten Schritt müssen Sie manuell "Formel" im Feld "Produktionstyp" eingeben, bevor Sie "Anwenden" auswählen. Dies legt den Filter auf der Liste der freigegebenen Produkte fest.  
4. Geben Sie manuell "Formel" im Feld "Produktionstyp" ein.
5. Klicken Sie auf Übernehmen.

## <a name="select-a-released-product"></a>Wählen eines freigegebenen Produktes
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
2. Klicken Sie auf "Formelversionen".
    * Klicken Sie im Aktivitätsbereich "Konstruktion" auf "Formelversionen".  

## <a name="copy-co-products"></a>Kopieren von Kuppelprodukten
1. Klicken Sie im Aktivitätsbereich auf "Formelversionen".
2. Klicken Sie auf Kuppelprodukte.
3. Klicken Sie auf Kopieren.
4. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
5. Geben Sie im Feld "Formelversion" einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie auf "OK".
7. Schließen Sie die Seite.

