--- 
title: Kostenobjekte erstellen
description: "Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die  Dynamics 365 for Finance and Operations Enterprise Edition Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importieren."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d43274aed2edbb91fd4e399cb8d45e91646b055
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-objects"></a>Kostenobjekte erstellen 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die  Dynamics 365 for Finance and Operations Enterprise Edition Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importieren. Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen. Diese Prozedur ist für eine Kostenbuchhaltungs-Funktion, die in Microsoft Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


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


