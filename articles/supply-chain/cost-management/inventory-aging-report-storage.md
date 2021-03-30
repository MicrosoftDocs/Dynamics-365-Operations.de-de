---
title: Bestandsfälligkeitsbericht
description: In diesem Thema wird die Funktionalität beschrieben, mit der Sie einen Bericht zur Bestandsalterung ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen können.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 40b15448677f319c650c667cd7c4981c343f7a02
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205345"
---
# <a name="inventory-aging-report-storage"></a>Bestandsfälligkeitsbericht

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management können Sie einen Bericht **Bestandsfälligkeitsbericht** ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen. Im Formular werden Spalten- und Summensalden je nach konfiguriertem Layout dynamisch angepasst. Das Diagramm bietet einen visuellen Überblick, der die Filterung unterstützt und es Ihnen ermöglicht, bis in die Details zu verzweigen. Zusätzlich können Sie mit einer Datenentität mit dem Namen **Bestandsfälligkeitsbericht** die Ergebnisse eines **Bestandsfälligkeitsbericht** in ein Format wie eine Microsoft Excel-Datei oder eine PDF-Datei exportieren.

Diese Methode zur Ausführung eines Berichts **Bestandsfälligkeitsbericht** ist hilfreich, wenn die Ausgabe viele Zeilen enthält. Beispielsweise enthält die Ausgabe viele Zeilen, wenn Sie 50.000 Artikel und 300 Filialen haben, die als Lager angelegt sind, und Sie die Bestandsalterung nach Artikel, Standort und Lager anfordern.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Aktivieren Sie die Funktion „Lagerbericht zum Bestandswert“

Bevor Sie diese Funktion nutzen können, müssen Sie sie auf Ihrem System aktivieren. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie bei Bedarf aktivieren. Hier wird die Funktion als aufgeführt:

- **Modul** - Kostenmanagement
- **Funktionsname** – Bestandsfälligkeitsbericht

## <a name="run-an-inventory-aging-report-storage"></a>Bestandsfälligkeitsbericht ausführen

1. Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Bestandsalterung**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Prozesskennung - Name** einen eindeutigen Namen für den Bericht ein.
1. Wählen Sie den Bericht **Identifikation - ID** aus und filtern Sie ihn nach Ihren Wünschen.

    Die Berichtsausführung erfolgt immer in einem Batch-Job.

1. Nach Abschluss des Batch-Jobs wird die Ausgabe auf der Seite **Bestandsalterung Berichtsspeicher** angezeigt.
1. Um die Ausgabe als ein Formular mit einem traditionellen Rasterlayout anzuzeigen, wählen Sie **Details anzeigen**. Um die Ausgabe als aggregiertes Diagramm anzuzeigen, wählen Sie **Diagramm anzeigen**.

    > [!NOTE]
    > Das Formular enthält keine Zwischensummen, die im Berichtslayout definiert sind.

Mit der **Bestandsfälligkeitsbericht**-Dateneinheit können Sie die Ausgabe eines Berichts **Bestandsfälligkeitsbericht** exportieren, indem Sie einen Filter für das Feld **Prozessidentifikator - Name** auf jedes Format anwenden, das von der Datenverwaltung unterstützt wird.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]