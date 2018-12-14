---
title: Analyseberichte werden nicht aktualisiert
description: "In diesem Thema wird erläutert, was zu tun ist, wenn die Datenänderungen eines Kunden in keinem der Arbeitsbereiche des Kunden angezeigt werden."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a>Analyseberichte werden nicht aktualisiert

[!include [banner](includes/banner.md)]

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

