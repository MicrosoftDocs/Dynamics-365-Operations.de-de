---
title: Grundeinrichtung eines veröffentlichten Produktmasters abschließen
description: In diesem Thema wird gezeigt, wie Sie die Mindesteinstellungen abschließen, die erforderlich sind, bevor der Produktmaster in den Stücklistenversionen verwendet werden kann.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428714"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Grundeinrichtung eines veröffentlichten Produktmasters abschließen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird gezeigt, wie Sie die Mindesteinstellungen abschließen, die erforderlich sind, bevor der Produktmaster in den Stücklistenversionen verwendet werden kann.

Dies ist die dritte von acht Prozeduren, die beschreibt, wie Kombinationen für eine dimensionsbasierte Konfiguration erstellt werden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.

1. Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie den Produktmaster aus, der in der zweiten Verfahren freigegeben haben. Dieser Produktmaster wird mit der Technologie der dimensionsbasierten Konfiguration erstellt.  
3. Klicken Sie im Aktivitätsbereich auf **Produkt**.
4. Klicken Sie auf **Dimensionsgruppen**, um das Dropdown-Dialogfeld zu öffnen.
5. Wählen Sie im Feld **Lagerdimensionsgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Die Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen für Produktbuchung verwendet werden. Wählen Sie **Standort** für diese Prozedur aus.  
7. Wählen Sie im Feld **Rückverfolgungsgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Die Nachverfolgung der Lagerdimensionsgruppe bestimmt, welche Lagerdimensionen für Produktbuchung verwendet werden. Wählen Sie **Keine** für diese Prozedur aus.  
9. Klicken Sie auf **OK**.
10. Klicken Sie auf **Bearbeiten**.
11. Wählen Sie im Feld **Artikelmodellgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
12. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Lagersteuerungsgruppen enthalten Einstellungen, die bestimmen, wie Artikel beim Artikelzugang und -abgang gesteuert und gehandhabt werden. Sie bestimmen auch, wie der Artikelverbrauch ermittelt wird. Wählen Sie **FIFO** für diese Prozedur aus.  
13. Erweitern Sie den Abschnitt **Kosten verwalten**.
14. Wählen Sie im Feld **Artikelgruppe** die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Artikelgruppen werden verwendet, um Lagerartikel in Gruppen zu unterteilen. Wählen Sie **CarAudio** für diese Prozedur aus.  
16. Wählen Sie im Aktivitätsbereich **Plan** aus.
17. Wählen Sie **Standardauftragseinstellungen**.
18. Wählen Sie im Feld **Standardauftragstyp** eine Option aus. Wählen Sie **Produktion** aus, um anzugeben, dass die standardmäßige Lieferoption für diesen Produktmaster ist, ihn zu erzeugen.  
19. Wählen Sie **Speichern**.
20. Schließen Sie die Seite.
21. Schließen Sie das Formular **Details für freigegebene Produkte**.

