--- 
title: Kostenelemente erstellen
description: "Es gibt mehrere Möglichkeiten, Kostenfaktoren in der Kostenrechnung zu erstellen."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e665fc53455e457a2488f4ec28ebb5b715d90eb
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-elements"></a>Kostenelemente erstellen 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Es gibt mehrere Möglichkeiten, Kostenfaktoren in der Kostenrechnung zu erstellen. Dieses Verfahren zeigt, wie Kostenfaktoren erstellt werden, indem Hauptkonten über einen Datenkonnektor importiert werden. Das USMF-Demodatenunternehmen wurde verwendet, um diese Prozedur zu erstellen. Diese Prozedur ist für eine Kostenbuchhaltungs-Funktion, die in Microsoft Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


## <a name="create-new-cost-elements"></a>Klicken Sie auf "Neue Kostenelemente erstellen".
1. Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenelementdimensionen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Datenkonnektor für Dimensionsmitglieder" einen Wert ein oder wählen Sie einen Wert aus.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Klicken Sie auf "Speichern".

## <a name="configure-the-data-connector"></a>Den Datenkonnektor konfigurieren
1. Klicken Sie auf "Dimensionselementanbieter konfigurieren".
2. Geben Sie im Feld "Kontenplan" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie "Gemeinsam", um den freigegebenen Kontenplan zu nutzen.  
3. Klicken Sie auf "Neu".
4. Markieren Sie in der Liste die ausgewählte Zeile.
    * Sie können Filter auf Konten anwenden, um die Kriterien zu erfüllen.  
5. Geben Sie im Feld "Aus Hauptkonto" einen Wert ein, oder wählen Sie einen Wert aus.
6. Geben Sie im Feld 'An Hauptkonto' einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf "OK".

## <a name="import-main-accounts"></a>Hauptkonten importieren
1. Klicken Sie auf "Dimensionsmitglieder importieren".
    * Hauptkonten werden in die Kostenrechnung importiert und als Kostenfaktoren verwendet.  
2. Klicken Sie auf "OK".

## <a name="view-the-imported-accounts-as-cost-elements"></a>Anzeigen der importierten Konten als an Kostenfaktoren
1. Klicken Sie auf "Dimensionsmitglieder anzeigen".
    * Zeigen Sie die importierten Sachkonten als Kostenfaktoren in Ihrem Unternehmen an, in dass Kosten fließen können.  


