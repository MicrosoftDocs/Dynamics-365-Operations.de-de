---
title: Einrichten der vorzeitigen Abschreibung
description: Die folgende Prozedur zeigt, wie ein Sonderabschreibungsbetrag erstellt wird und es einem Anlagenbuch zuordnet wird.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad1b7f584d2b2a63dba5f8519ada9d89d6265e7b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815619"
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