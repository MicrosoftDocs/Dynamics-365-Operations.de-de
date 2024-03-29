---
title: Kostenelemente erstellen
description: Es gibt mehrere Möglichkeiten, Kostenfaktoren in der Kostenrechnung zu erstellen.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779688"
---
# <a name="create-cost-elements"></a>Kostenelemente erstellen 

[!include [banner](../../includes/banner.md)]

Es gibt mehrere Möglichkeiten, Kostenfaktoren in der Kostenrechnung zu erstellen. Dieses Verfahren zeigt, wie Kostenfaktoren erstellt werden, indem Hauptkonten über einen Datenkonnektor importiert werden. Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen. Diese Prozedur ist eine Funktion, für die Kostenrechnung-Funktion, die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="create-new-cost-elements"></a>Klicken Sie auf "Neue Kostenelemente erstellen".
1. Wechseln Sie zu **Kostenrechnung > Dimensionen > Kostenelementdimensionen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Name** einen Wert ein.
4. Geben Sie im Feld **Datenkonnektor für Dimensionsmitglieder** einen Wert ein oder wählen Sie einen Wert aus.
5. Geben Sie im Feld **Beschreibung** einen Wert ein.
6. Klicken Sie auf **Speichern**.

## <a name="configure-the-data-connector"></a>Den Datenkonnektor konfigurieren
1. Klicken Sie auf **Dimensionselementanbieter konfigurieren**.
2. Geben Sie im Feld **Kontenplan** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie **Gemeinsam**, um den freigegebenen Kontenplan zu nutzen.  
3. Klicken Sie auf **Neu**.
4. Markieren Sie in der Liste die ausgewählte Zeile.
    * Sie können Filter auf Konten anwenden, um die Kriterien zu erfüllen.  
5. Geben Sie im Feld **Aus Hauptkonto** einen Wert ein, oder wählen Sie einen Wert aus.
6. Geben Sie im Feld **An Hauptkonto** einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf **OK**.

## <a name="import-main-accounts"></a>Hauptkonten importieren
1. Klicken Sie auf **Dimensionsmitglieder importieren**.
    * Hauptkonten werden in die Kostenrechnung importiert und als Kostenfaktoren verwendet.  
2. Klicken Sie auf **OK**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Anzeigen der importierten Konten als an Kostenfaktoren
1. Klicken Sie auf **Dimensionsmitglieder anzeigen**.
    * Zeigen Sie die importierten Sachkonten als Kostenfaktoren in Ihrem Unternehmen an, in dass Kosten fließen können.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
