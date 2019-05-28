---
title: Deckungseinstellungen
description: Dieses Thema enthält Informationen zur Behandlung von Deckungseinstellungen, die beim Produktprogrammplanungslauf verwendet wird, um den Artikelbedarf zu berechnen.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538893"
---
# <a name="coverage-settings"></a>Deckungseinstellungen

[!include [banner](../includes/banner.md)]

Diese Deckungseinstellungen werden beim Produktprogrammplanungslauf zum Berechnen des Artikelbedarfs verwendet.

Sie können Deckungseinstellungen auf verschiedene Arten angeben:

- Angeben von Dispositionseinstellungen für eine Dispositionsgruppe.

    Sie haben die Möglichkeit zum Erstellen einer Deckungsgruppe mit Einstellungen für alle Produkte, die mit der Deckungsgruppe verknüpft sind. Um eine Abdeckungsgruppe zu erstellen, gehen Sie zu **Masterplan &gt; Einrichten &gt; Abdeckung &gt; Abdeckungsgruppen**. Sie können eine Deckungsgruppe mit einem Produkt verknüpfen. Wenn der Link für einen bestimmten Standort, Lagerort oder eine Produktdimension bestimmt ist, verwenden Sie auf der Seite **Artikeldeckung** das Feld **Dispositionssteuerungsgruppe**. Wenn es ein generischer Link ist, verwenden Sie unabhängig von den Produktdimensionen das Feld **Dispositionssteuerungsgruppe** auf dem Inforegister **Plan** der Seite **Produktdetails**. Entsprechend dem Standard und wenn Sie keine Dispositionssteuerungsgruppe mit einem Produktplan verküpfen, indem Sie die allgemeine Dispositionssteuerungsgruppe der Seite **Produktprogrammplanungsparameter** als Standard angegeben ist.

- Angeben der Dispositionseinstellungen für ein Produkt.

    Sie haben die Möglichkeit zum Erstellen von Deckungseinstellungen für ein bestimmtes Produkt. Wechseln Sie zu **Produktinformationsverwaltung &gt; Produkte &gt;Freigegebene Produkte**. Wählen Sie das Produkt und dann im Aktivitätenbereich in der Registerkarte **Plan** in der Gruppe**Abdeckung** und wählen Sie **Artikelabdeckung**, um die Seite **Artikelabdeckung** zu öffnen. Ist das Produkt bereits mit einer Dispositionsgruppe verknüpft, können die Einstellungen der Deckungsgruppe mithilfe des Felds **Überschreiben** überschrieben werden. Die Dispositionseinstellungen auf der Seite **Artikeldeckung** haben Vorrang vor den Einstellungen auf der Seite **Dispositionssteuerungsgruppe**.

- Angeben der Deckungseinstellungen für ein Produkt mithilfe eines Assistenten.

    Der Assistent führt Sie schrittweise durch den Prozess zum Einrichten der zentralen Artikeldeckungsparameter. Klicken Sie auf der Seite **Artikeldeckung** unter Aktivitätsbereich auf **Assistent**, um den **Artikelabdeckungs-Assistent** zu öffnen.

- Angeben von Deckungseinstellungen für eine Dimensionsgruppe.

    Wechseln Sie zu **Produktinformationsverwaltung &gt; Produkte &gt;Freigegebene Produkte**. Klicken Sie auf der Seite **Details für freigegebene Produkte** auf der Registerkarte **Allgemein** in der Gruppe **Administration** auf den Link **Lagerdimensionsgruppe**. Wählen Sie auf der Seite **Lagerdimensionsgruppen** das Kontrollkästchen **Abdeckungsplan nach Dimensionen** aus, um die Deckungseinstellungen für eine Dimension in der Lagerdimensionsgruppe zu erstellen. Das Feld **Abdeckungsplan nach Dimensionn**  muss ausgewählt sein für alle Produktdimensionen wie Konfiguration, Farbe, Größe und Stil .

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Produktprogrammpläne](master-plans.md)
