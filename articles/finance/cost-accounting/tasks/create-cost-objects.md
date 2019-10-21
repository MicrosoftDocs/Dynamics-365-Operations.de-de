---
title: Kostenobjekte erstellen
description: Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importiert wird.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2616e5275f9f59b962d4e456684073aea2c654ea
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249677"
---
# <a name="create-cost-objects"></a>Kostenobjekte erstellen 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importiert wird. Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen. 


## <a name="create-new-cost-objects"></a>Neue Kostenobjekte erstellen
1. Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenobjektdimensionen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Datenkonnektor für Dimensionsmitglieder" einen Wert ein oder wählen Sie einen Wert aus.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Klicken Sie auf "Speichern".

## <a name="configure-the-data-connector"></a>Den Datenkonnektor konfigurieren
1. Klicken Sie auf "Dimensionselementanbieter konfigurieren".
    * Wählen Sie CostCenter aus, um CostCenter-Dimension in die Kostenrechnung zu importieren.  
2. Wählen Sie im Dimensionsnamen-Feld Sie die Kostenstelle aus.
3. Klicken Sie auf "OK".

## <a name="import-cost-centers"></a>Kostenstellen importieren
1. Klicken Sie auf "Dimensionsmitglieder importieren".
2. Klicken Sie auf "OK".

## <a name="view-the-imported-cost-centers"></a>Importierte Kostenstellen anzeigen
1. Klicken Sie auf "Dimensionsmitglieder anzeigen".

