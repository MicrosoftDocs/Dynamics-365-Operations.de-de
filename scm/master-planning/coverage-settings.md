---
title: Dispositionseinstellungen
description: Diese Deckungseinstellungen werden beim Produktprogrammplanungslauf zum Berechnen des Artikelbedarfs verwendet.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>Dispositionseinstellungen

Diese Deckungseinstellungen werden beim Produktprogrammplanungslauf zum Berechnen des Artikelbedarfs verwendet. 

Sie können Deckungseinstellungen auf verschiedene Arten angeben:

-   Angeben von Dispositionseinstellungen für eine Dispositionsgruppe. Sie haben die Möglichkeit zum Erstellen einer Deckungsgruppe mit Einstellungen für alle Produkte, die mit der Deckungsgruppe verknüpft sind. ** Auf Produktprogrammplanung &gt; richten Sie &gt; Dispositions-Dispositionssteuerungsgruppen &gt; ** um eine Dispositionssteuerungsgruppe erstellen. Sie können eine Deckungsgruppe mit einem Produkt verknüpfen. Wenn der Link für einen bestimmten Standort, Lagerort oder eine Produktdimension bestimmt ist, verwenden Sie auf der Seite **Artikeldeckung** das Feld **Dispositionssteuerungsgruppe**. Wenn es ein generischer Link ist, verwenden Sie unabhängig von den Produktdimensionen die **Dispositionssteuerungsgruppe** auf dem Inforegister **Plan** der Seite **Produktdetails**. Wenn Sie eine Dispositionssteuerungsgruppe nicht mit einem Produkt verknüpfen, verwendet der Produktprogrammplan nicht die **Allgemeine Dispositionssteuerungsgruppe**, die auf der Seite **Produktprogrammplanungsparameter** als Standard angegeben ist.

-   Angeben der Dispositionseinstellungen für ein Produkt. Sie haben die Möglichkeit zum Erstellen von Deckungseinstellungen für ein bestimmtes Produkt. ** Produktinformationsverwaltung auf Produkt-freigegebeneProdukte &gt; ** &gt;. Wählen Sie die Produkt-, auf ** Aktivitätsbereich **, auf der Registerkarte, ** ** Plan in ** Dispositionssteuerungsgruppe **, auf ** Artikeldeckung aus ** um die Artikeldeckung ** ** Seite zu öffnen. Ist das Produkt bereits mit einer Dispositionsgruppe verknüpft, können die Einstellungen der Deckungsgruppe mithilfe des Felds **Überschreiben** überschrieben werden. Die Dispositionseinstellungen auf der Seite **Artikeldeckung** haben Vorrang vor den Einstellungen auf der Seite **Dispositionssteuerungsgruppe**.

<!-- -->

-   Angeben der Deckungseinstellungen für ein Produkt mithilfe eines Assistenten. Bei dem Assistenten handelt es sich um eine schrittweise Anleitung zum Einrichten der primären Artikeldeckungsparameter. Klicken Sie auf der Seite **Artikeldeckung** auf **Assistent**, um den **Artikeldeckungs-Assistent** zu öffnen.

<!-- -->

-   Angeben von Deckungseinstellungen für eine Dimensionsgruppe. ** Produktinformationsverwaltung auf allgemeine &gt; freigegebene Produkte &gt; **. Auf der freigegebenen ** Details des Produkts ** Seite auf der Registerkarte Allgemein ** **, in der Verwaltung ** ** Gruppe, Lagerdimensionsgruppe ** ** auf den Link. Wählen Sie auf der Seite **Lagerdimensionsgruppe** das Feld **Disposition nach Dimensionen** aus, um die Deckungseinstellungen für eine Dimension in der Lagerdimensionsgruppe zu erstellen. Alle Produktdimensionen, beispielsweise Konfiguration, Größe, Farbe, Stil, müssen das ** Dispositionsplan nach Dimension ** ausgewählte Feld haben.



<a name="see-also"></a>Siehe auch
--------

[Master plans](master-plans.md)


