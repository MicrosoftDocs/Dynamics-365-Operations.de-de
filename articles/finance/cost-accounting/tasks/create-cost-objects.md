---
title: Kostenobjekte erstellen
description: Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importiert wird.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734129"
---
# <a name="create-cost-objects"></a>Kostenobjekte erstellen 

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie Kostenobjekte erstellt werden, indem die Kostenstellenfinanzdimension in die Kostenrechnung über einen Datenkonnektor importiert wird. Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen. 


## <a name="create-new-cost-objects"></a>Neue Kostenobjekte erstellen
1. Wechseln Sie zu den **Kostenrechnung > Dimensionen > Kostenträgerdimensionen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Name** einen Wert ein.
4. Geben Sie im Feld **Datenkonnektor für Dimensionsmitglieder** einen Wert ein oder wählen Sie einen Wert aus.
5. Geben Sie im Feld **Beschreibung** einen Wert ein.
6. Klicken Sie auf **Speichern**.

## <a name="configure-the-data-connector"></a>Den Datenkonnektor konfigurieren
1. Klicken Sie auf **Dimensionselementanbieter konfigurieren**.
    * Wählen Sie CostCenter aus, um CostCenter-Dimension in die Kostenrechnung zu importieren.  
2. Wählen Sie im **Dimensionsname**-Feld Sie die Kostenstelle aus.
3. Klicken Sie auf **OK**.

## <a name="import-cost-centers"></a>Kostenstellen importieren
1. Klicken Sie auf **Dimensionsmitglieder importieren**.
2. Klicken Sie auf **OK**.

## <a name="view-the-imported-cost-centers"></a>Importierte Kostenstellen anzeigen
1. Klicken Sie auf **Dimensionsmitglieder anzeigen**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
