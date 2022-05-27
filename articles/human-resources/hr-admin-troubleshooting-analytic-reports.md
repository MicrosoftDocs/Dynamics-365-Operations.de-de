---
title: Problembehandlung bei analytischen Berichten
description: Dieses Thema erklärt, wie Sie Probleme beheben und diagnostizieren, wenn die Datenänderungen eines Debitors in keinem seiner Arbeitsbereiche angezeigt werden.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e81bae4d9cb0bb0b77bb57bac16cc67bbbcf9ea
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694059"
---
# <a name="troubleshoot-analytic-reports"></a>Problembehandlung bei analytischen Berichten


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Abgang**

Die Datenänderungen eines Kunden werden nicht in der Registerkarte **Analyse** von irgendeinem der Arbeitsbereiche des Kunden angezeigt.

**Ursache**

Standardmäßig werden die Microsoft Power BI-Berichte alle vier Stunden aktualisiert, entsprechend dem Zeitplan des Batch-Jobs „Messung bereitstellen“.

**Auflösung**

Dieses Problem ist möglicherweise nur eine Frage der Zeitmessung. Gehen Sie folgendermaßen vor, um den Batchauftrag zu starten und die Analysearbeitsbereiche zu aktualisieren.

1. Öffnen Sie die Seite **Batchaufträge** unter **Systemverwaltung \> Links \> Batchaufträge \> Batchaufträge**. Alternativ verwenden Sie „Suche” und geben Sie **Batchaufträge** ein.
1. Suchen Sie den Einzelvorgang **Messung bereitstellen** in der Liste.
1. Wählen Sie **Bearbeiten** am oberen Seitenrand aus, und legen Sie das geplante Startdatum/Uhrzeit auf einen Wert fest, durch den die Analyse näher an der aktuellen Uhrzeit aktualisiert wird.

![Batchaufträge.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
