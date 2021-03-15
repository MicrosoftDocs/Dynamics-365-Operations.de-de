---
title: Problembehandlung bei analytischen Berichten
description: In diesem Artikel wird erläutert, was zu tun ist, wenn die Datenänderungen eines Kunden in keinem der Arbeitsbereiche des Kunden angezeigt werden.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112672"
---
# <a name="troubleshoot-analytic-reports"></a>Problembehandlung bei analytischen Berichten

**Abgang**

Die Datenänderungen eines Kunden werden nicht in der Registerkarte **Analyse** von irgendeinem der Arbeitsbereiche des Kunden angezeigt.

**Ursache**

Standardmäßig werden Microsoft Power BI-Berichte alle vier Stunden aktualisiert, entsprechend des Zeitplans des Batchauftrags „Messung bereitstellen”.

**Auflösung**

Dieses Problem ist möglicherweise nur eine Frage der Zeitmessung. Gehen Sie folgendermaßen vor, um den Batchauftrag zu starten und die Analysearbeitsbereiche zu aktualisieren.

1. Öffnen Sie die Seite **Batchaufträge** unter **Systemverwaltung \> Links \> Batchaufträge \> Batchaufträge**. Alternativ verwenden Sie „Suche” und geben Sie **Batchaufträge** ein.
1. Suchen Sie den Einzelvorgang **Messung bereitstellen** in der Liste.
1. Wählen Sie **Bearbeiten** am oberen Seitenrand aus, und legen Sie das geplante Startdatum/Uhrzeit auf einen Wert fest, durch den die Analyse näher an der aktuellen Uhrzeit aktualisiert wird.

![Batchaufträge](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]