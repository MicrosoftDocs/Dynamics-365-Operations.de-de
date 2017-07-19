---
title: Dispositionseinstellungen
description: Diese Deckungseinstellungen werden beim Produktprogrammplanungslauf zum Berechnen des Artikelbedarfs verwendet.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b42f0515823bd42ec260aa1d175855a923162b62
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="coverage-settings"></a>Dispositionseinstellungen

[!include[banner](../includes/banner.md)]


Diese Deckungseinstellungen werden beim Produktprogrammplanungslauf zum Berechnen des Artikelbedarfs verwendet. 

Sie können Deckungseinstellungen auf verschiedene Arten angeben:

-   Angeben von Dispositionseinstellungen für eine Dispositionsgruppe. Sie haben die Möglichkeit zum Erstellen einer Deckungsgruppe mit Einstellungen für alle Produkte, die mit der Deckungsgruppe verknüpft sind. Klicken Sie auf **Masterplan&gt; Einrichten &gt; Abdeckung &gt; Abdeckungsgruppen**, um eine Abdeckungsgruppe zu erstellen. Sie können eine Deckungsgruppe mit einem Produkt verknüpfen. Wenn der Link für einen bestimmten Standort, Lagerort oder eine Produktdimension bestimmt ist, verwenden Sie auf der Seite **Artikeldeckung** das Feld **Dispositionssteuerungsgruppe**. Wenn es ein generischer Link ist, verwenden Sie unabhängig von den Produktdimensionen die **Dispositionssteuerungsgruppe** auf dem Inforegister **Plan** der Seite **Produktdetails**. Wenn Sie eine Dispositionssteuerungsgruppe nicht mit einem Produkt verknüpfen, verwendet der Produktprogrammplan nicht die **Allgemeine Dispositionssteuerungsgruppe**, die auf der Seite **Produktprogrammplanungsparameter** als Standard angegeben ist.

-   Angeben der Dispositionseinstellungen für ein Produkt. Sie haben die Möglichkeit zum Erstellen von Deckungseinstellungen für ein bestimmtes Produkt. Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**. Wählen Sie das Produkt im **Aktivitätenbereich**, in der Registerkarte **Plan** in der **Abdeckungsgruppe**, klicken Sie auf **Artikelabdeckung**, um die Seite **Artikelabdeckung** zu öffnen. Ist das Produkt bereits mit einer Dispositionsgruppe verknüpft, können die Einstellungen der Deckungsgruppe mithilfe des Felds **Überschreiben** überschrieben werden. Die Dispositionseinstellungen auf der Seite **Artikeldeckung** haben Vorrang vor den Einstellungen auf der Seite **Dispositionssteuerungsgruppe**.

<!-- -->

-   Angeben der Deckungseinstellungen für ein Produkt mithilfe eines Assistenten. Bei dem Assistenten handelt es sich um eine schrittweise Anleitung zum Einrichten der primären Artikeldeckungsparameter. Klicken Sie auf der Seite **Artikeldeckung** auf **Assistent**, um den **Artikeldeckungs-Assistent** zu öffnen.

<!-- -->

-   Angeben von Deckungseinstellungen für eine Dimensionsgruppe. Klicken Sie auf **Produktinformationsverwaltung &gt;Allgemein &gt; Freigegebene Produkte**. Auf der Seite **freigegebene Produktedetails** auf der Registerkarte **Allgemein**in der Gruppe **Administration** klicken Sie auf den Link **Lagerdimensionsgruppe**. Wählen Sie auf der Seite **Lagerdimensionsgruppe** das Feld **Disposition nach Dimensionen** aus, um die Deckungseinstellungen für eine Dimension in der Lagerdimensionsgruppe zu erstellen. Für jede Produktdimension, wie Konfiguration, Farbe, Größe, Stil, muss das Feld **Abdeckungsplan nach Dimensionn**  ausgewählt sein.



<a name="see-also"></a>Siehe auch
--------

[Masterpläne](master-plans.md)




