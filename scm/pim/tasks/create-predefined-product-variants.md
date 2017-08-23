--- 
title: Vordefinierte Produktvarianten erstellen
description: "Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen."
author: BibiSp
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: fd6e6844b5920ba1364fa0fd5865d89d83789973
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="create-predefined-product-variants"></a>Vordefinierte Produktvarianten erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch das Erstellen von Produktvarianten für einen Produktmaster mithilfe der Kombinationen von Produktdimensionen. Das Demounternehmen für diese Prozedur ist USMF.


## <a name="create-a-product-master"></a>Produktmaster erstellen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Produktmaster".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Produktnummer" einen Wert ein.
    * Eine Produktnummer manuell einzugeben ist nur erforderlich, wenn kein Nummernkreis für das Produktnummernfeld eingerichtet wurde. In anderen Worten, überspringen Sie den Schritt, wenn ein Nummernkreis für das Feld festgelegt wurde.  
4. Geben Sie im Feld "Produktname" einen Wert ein.
5. Geben Sie im Feld "Produktdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie die Produktdimensionsgruppe "SizeCol" (Größe und Farbe) aus.  
6. Klicken Sie auf "OK".

## <a name="add-product-dimensions"></a>Klicken Sie auf "Produktdimensionen hinzufügen".
1. Klicken Sie auf "Produktdimensionen".
    * Dieses Beispiel zeigt, wie Produktdimensionenen manuell eingegeben werden. Sie können auch wählen, eine Größe, Farbe oder Stilgruppe auszuwählen, die die Produktdimensionswerte umfasst, die Sie verwenden möchten.  
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Größe" einen Wert ein, oder wählen Sie einen Wert aus.
5. Geben Sie im Feld "Name" einen Wert ein.
6. Klicken Sie auf Neu.
7. Markieren Sie in der Liste die ausgewählte Zeile.
8. Geben Sie im Feld "Größe" einen Wert ein, oder wählen Sie einen Wert aus.
9. Geben Sie im Feld "Name" einen Wert ein.
10. Klicken Sie auf die Registerkarte "Farben".
11. Klicken Sie auf "Neu".
12. Markieren Sie in der Liste die ausgewählte Zeile.
13. Geben Sie im Feld "Farbe" einen Wert ein, oder wählen Sie einen Wert aus.
14. Geben Sie im Feld "Name" einen Wert ein.
15. Klicken Sie auf Neu.
16. Markieren Sie in der Liste die ausgewählte Zeile.
17. Geben Sie im Feld "Farbe" einen Wert ein, oder wählen Sie einen Wert aus.
18. Geben Sie im Feld "Name" einen Wert ein.
19. Klicken Sie auf "Speichern".
20. Schließen Sie die Seite.

## <a name="generate-product-variants"></a>Generieren Sie Produktvarianten
1. Klicken Sie auf "Produktvarianten".
2. Klicken Sie auf "Variantenvorschläge".
3. Klicken Sie auf "Alles auswählen".
    * In diesem Beispiel werden alle möglichen Varianten ausgewählt. Wenn nur eine Teilmenge der möglichen Produktdimensionskombinationen verwendet wird, um Varianten zu erstellen, können Sie die einzelnen Einträge auswählen.  
4. Klicken Sie auf "Erstellen".
    * Sie können Beschreibungen für alle Ihre Varianten anhand der Kombination von Produktdimensionswerten generieren. Die Beschreibungen sind optional.  
5. Klicken Sie auf "Speichern".


