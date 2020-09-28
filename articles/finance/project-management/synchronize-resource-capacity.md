---
title: Ressourcenkapazität synchronisieren
description: Dieses Thema enthält Informationen zum Synchronisieren der Kapazität einer Ressource über Kalender und Projekte hinweg.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760552"
---
# <a name="synchronize-resource-capacity"></a>Ressourcenkapazität synchronisieren

[!include [banner](../includes/banner.md)]

Die Prozesse für die Ressourcensynchronisierung stellen sicher, dass die Kalender- und Basiskalenderinformationen zur Projekteinsatzplanung passen. Wenn der Kalender geändert wird, nehmen die Prozesse die erforderlichen Aktualisierungen der Planung von Projektbetriebsmitteln vor. Die Verfahren helfen außerdem, die Leistung zu verbessern, da die Ressourceninformationen des Kalenders vorab synchronisiert werden. Deshalb werden Aktualisierungen der Einsatzplanungsinformationen schneller durchgeführt. Es wird empfohlen, die Prozesse als Stapelverarbeitung und nicht einzeln zu planen. Andernfalls besteht das Risiko, das jemand die inklusiven Datumsangaben bei der letzten Synchronisierung der Information vergisst. Wenn keine inklusiven Datumsangaben verwendet werden, können Lücken während der Datumssynchronisierung auftreten.

![Kalendersynchronisierung](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Ressourcenkapazitätszusammenfassungen synchronisieren

Der Synchronisierungsprozess wurde entworfen, um alle Ressourcenkalenderinformationen zu synchronisieren. Dazu gehören Basiskalenderinformationen zu Änderungen an der Ressourcenkalenderkapazitätstabelle des Projekts. Wenn neue Ressourcen zum Projekt hinzugefügt werden, stellen die Synchronisierungshilfen sicher, dass die aktualisierten Kalenderdaten verfügbar sind. Es Synchronisierung kann jederzeit durchgeführt werden.

Es wird empfohlen, eine Stapelverarbeitung zu verwenden. Die Optionen sind verfügbar, wenn Sie Kapazitätsreservierungen synchronisieren.

1. Wählen Sie **Projektverwaltung und -buchhaltung** &gt; **Periodisch** &gt; **Kapazitätssynchronisierung** &gt; **Ressourcenkapazitätszusammenfassungen synchronisieren** aus.
2. Legen Sie die Optionen in der folgenden Tabelle fest.

    | Option      | Beschreibung |
    |-------------|-------------|
    | Periodencode | Wählen Sie optional den Hauptbuch-Datumsintervallcode aus, um das Start-und Enddatum für den Synchronisierungsprozess für die Ressourcenkapazitätszusammenfassungen festzulegen. |
    | Eintrittstermin  | Geben Sie das Startdatum für die Synchronisierung der Ressourcenkapazitätszusammenfassungen ein. |
    | Enddatum    | Geben Sie das Enddatum für die Synchronisierung der Ressourcenkapazitätszusammenfassungen ein. |

[![Synchronisierungsprozess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
