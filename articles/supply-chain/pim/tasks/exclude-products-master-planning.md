---
title: Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen
description: In dieser Prozedur wird gezeigt, wie ein neuer Produktlebenszyklus-Status erstellt wird, bei dem Produkte vom Produktprogrammplan und der Stücklistenberechnung ausgeschlossen werden.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc24aad05499adf9bfb2db3613c7f134c3a70770
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264697"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen

[!include [banner](../../includes/banner.md)]

In dieser Prozedur wird gezeigt, wie ein neuer Produktlebenszyklus-Status erstellt wird, bei dem Produkte vom Produktprogrammplan und der Stücklistenberechnung ausgeschlossen werden.


## <a name="create-an-obsolete-state"></a>Einen veralteten Status erstellen
1. Wechseln Sie zu Produktinformationsverwaltung > Einstellungen > Produktlebenszyklus-Status.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld „Status” einen Wert ein.
4. Wählen Sie „Nein” im Feld „Ist aktiv für Planung” aus.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Den veralteten Status einem freigegebenen Produkt zuordnen
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
3. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld „Name suchen” mit einem Wert von „M00”.
4. Klicken Sie auf "Bearbeiten".
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]