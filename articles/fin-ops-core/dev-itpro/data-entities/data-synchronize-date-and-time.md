---
title: Synchronisieren von Datum und Uhrzeit in Importaufträgen
description: Verwenden Sie UTC-Zeitzonen in Importaufträgen, um Probleme mit Zeitzonenkonvertierungen zu vermeiden.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798718"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Synchronisieren von Datum und Uhrzeit in Importaufträgen

[!include [banner](../includes/banner.md)]

Es ist wichtig, die Zeitzone für Ihren Importauftrag auf die koordinierte Weltzeit (UTC) einzustellen. Wenn Sie eine andere Einstellung verwenden, werden möglicherweise unerwartete Daten und Zeiten in Ihren importierten Daten angezeigt. Ohne die richtige Einstellung konvertiert der Importvorgang das UTC-Datum in das lokale Format, und die Systemeinstellungen konvertieren es erneut.

Diese doppelte Konvertierung führt dazu, dass sich die Datumsangaben zwischen den Anwendungen ändern. Beispielsweise kann die doppelte Konvertierung dazu führen, dass das Startdatum eines Mitarbeiters sich in Dynamics 365 Human Resources und Dynamics 365 Finance aufgrund von Unterschieden in den lokalen Zeitzonen unterscheidet. Durch Setzen des Importauftrags auf UTC wird dieses Problem behoben.

1. In Dynamics 365 Finance and Operations wählen Sie **Datenverwaltung**.

2. Wählen Sie **Importprojekte**, und wählen Sie dann das Projekt aus.

3. Unter **Quelldatumsformat** wählen Sie **CSV-Unicode** aus.

   [![Ändern des Quelldatumsformats in UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Ändern Sie die **Zeitzone** in **Koordinierte Weltzeit**, und ändern Sie **Sprache** in **En-US**.

