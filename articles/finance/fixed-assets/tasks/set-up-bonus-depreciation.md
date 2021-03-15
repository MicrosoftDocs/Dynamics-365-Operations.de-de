---
title: Einrichten der vorzeitigen Abschreibung
description: Die folgende Prozedur zeigt, wie ein Sonderabschreibungsbetrag erstellt wird und es einem Anlagenbuch zuordnet wird.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968928"
---
# <a name="set-up-bonus-depreciation"></a>Einrichten der vorzeitigen Abschreibung

[!include [banner](../../includes/banner.md)]

Die folgende Prozedur zeigt, wie ein Sonderabschreibungsbetrag erstellt wird und es einem Anlagenbuch zuordnet wird. Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.


## <a name="create-a-special-depreciation-allowance"></a>Eine Sonderabschreibung erstellen
1. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Sonderabschreibung".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Sonderabschreibung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Prozentsatz" eine Zahl ein.
    * Wen ein Betrag nicht festgelegt ist, legen Sie einen Betrag fest.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>Eine Sonderabschreibung einem Anlagengruppenbuch zuordnen
1. Wechseln Sie zu Anlagen > Einstellungen > Anlagengruppen.
2. Wählen Sie in der Liste die Anlagengruppe aus, die der Sonderabschreibung zugeordnet ist.
3. Klicken Sie auf Bücher.
4. Wählen Sie in der Liste das Buch aus, die der Sonderabschreibung zugeordnet ist.
5. Klicken Sie auf "Sonderabschreibung".
6. Klicken Sie auf "Neu".
7. Geben Sie im Feld "Sonderabschreibung" einen Wert ein oder wählen Sie einen aus.
    * Der Prozentsatz oder Betrag wird standardmäßig aus der Sonderabschreibungseinstellung übernommen.  
8. Geben Sie im Feld "Priorität" eine Zahl ein.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]