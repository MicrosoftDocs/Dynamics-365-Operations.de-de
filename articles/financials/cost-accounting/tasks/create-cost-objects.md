--- 
title: Kostenobjekte erstellen
description: "Diese Prozedur zeigt an, wie Kostenobjekte erstellt werden, indem die Kostenstellen-Finanzdimension von Dynamics 365 for Finance and Operations nach Kostenrechnung über einen Datenkonnektor importiert wird."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 21fa90557b665e0777935cc6bae8cd9f1c29cb60
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---
# <a name="create-cost-objects"></a>Kostenobjekte erstellen 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt an, wie Kostenobjekte erstellt werden, indem die Kostenstellen-Finanzdimension von Dynamics 365 for Finance and Operations nach Kostenrechnung über einen Datenkonnektor importiert wird. Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen. Diese Prozedur ist für eine Kostenbuchhaltungs-Funktion, die in Microsoft Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


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


