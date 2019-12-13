---
title: Bestandsfälligkeitsbericht
description: In diesem Thema wird die Funktionalität beschrieben, mit der Sie einen Bericht zur Bestandsalterung ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen können.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810250"
---
# <a name="inventory-aging-report"></a>Bestandsfälligkeitsbericht


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 Supply Chain Management können Sie einen Bericht **Inventuralterung** ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen. Im Formular werden Spalten- und Summensalden je nach konfiguriertem Layout dynamisch angepasst. Das Diagramm bietet einen visuellen Überblick, der die Filterung unterstützt und es Ihnen ermöglicht, bis in die Details zu verzweigen. Zusätzlich können Sie mit einer Datenentität mit dem Namen **Bestandsalterungsbericht** die Ergebnisse eines **Bestandsalterungsberichts** in ein Format wie eine Microsoft Excel-Datei oder eine PDF-Datei exportieren.

Diese Methode zur Ausführung eines Berichts **Bestandsalterung** ist hilfreich, wenn die Ausgabe viele Zeilen enthält. Beispielsweise enthält die Ausgabe viele Zeilen, wenn Sie 50.000 Artikel und 300 Filialen haben, die als Lager angelegt sind, und Sie die Bestandsalterung nach Artikel, Standort und Lager anfordern.

## <a name="run-an-inventory-aging-report"></a>Ausführen eines Berichts zur Bestandsalterung

1. Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Bestandsalterung**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Prozesskennung - Name** einen eindeutigen Namen für den Bericht ein.
1. Wählen Sie den Bericht **Identifikation - ID** aus und filtern Sie ihn nach Ihren Wünschen.

    Die Berichtsausführung erfolgt immer in einem Batch-Job.

1. Nach Abschluss des Batch-Jobs wird die Ausgabe auf der Seite **Bestandsalterung Berichtsspeicher** angezeigt.
1. Um die Ausgabe als ein Formular mit einem traditionellen Rasterlayout anzuzeigen, wählen Sie **Details anzeigen**. Um die Ausgabe als aggregiertes Diagramm anzuzeigen, wählen Sie **Diagramm anzeigen**.

    > [!NOTE]
    > Das Formular enthält keine Zwischensummen, die im Berichtslayout definiert sind.

Mit dem Bericht **Bestandsalterung** Dateneinheit können Sie die Ausgabe eines Berichts **Bestandsalterung** exportieren, indem Sie einen Filter für das Feld **Prozessidentifikator - Name** auf jedes Format anwenden, das von der Datenverwaltung unterstützt wird.
