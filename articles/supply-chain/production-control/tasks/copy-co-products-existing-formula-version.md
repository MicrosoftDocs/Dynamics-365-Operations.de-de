---
title: Kuppelprodukte aus einer vorhandenen Formel kopieren
description: Diese Prozedur zeigt Ihnen an, wie Sie Co-Produkte aus einer vorhandenen Formelversion zu einer anderen Formelversion für ein freigegebenes Produkt kopieren.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 182cc79a3aaacd8a3af97310bd63a37de5338157
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212364"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>Kuppelprodukte aus einer vorhandenen Formel kopieren

[!include [banner](../../includes/banner.md)]

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

