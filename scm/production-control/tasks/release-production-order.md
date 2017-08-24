--- 
title: Produktionsauftrag freigeben
description: Diese Prozedur zeigt an, wie ein Produktionsauftrag freigegeben wird.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6497921db5632fe69ae596bddd6889c6d3125c38
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="release-a-production-order"></a>Produktionsauftrag freigeben

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt an, wie ein Produktionsauftrag freigegeben wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist die vierte Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.

1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
    * Wählen Sie im Raster einen Produktionsauftrag aus, der den Status "Eingeplant" hat.  
2. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
3. Klicken Sie auf "Freigabe".
    * Auf dieser Seite können Sie die Freigabe des ausgewählten Bereichs von Produktionsaufträgen bestätigen. Klicken Sie auf "Auswählen", wenn Sie Aufträge hinzufügen möchten.  
    * Der "Freigabeschritt" zeigt an, wann der Produktionsauftrag für die Produktionszeiterfassung freigegeben wird, sodass die Zeiterfassungsoperatoren den Status zu Produktionseinzelvorgängen melden können. Produktionsunterlagen, die relevante Informationen zum Verarbeiten der Einzelvorgänge enthalten, können ausgestellt werden. Die Lagerortarbeit für die Rohmaterialentnahme wird für die Artikel generiert, die für den Lagerortprozess eingerichtet werden.  
4. Klicken Sie auf die Registerkarte "Allgemein".
    * Wählen Sie aus, welche Produktionsberichte gedruckt werden sollen. Der Bericht "Einzelvorgangsliste" druckt eine Seite für jeden geplanten Einzelvorgang aus und erfordert, dass der Produktionsauftrag auf der Einzelvorgangebene eingeplant wird. Der Bericht enthält Informationen über die geplante Start- und Endzeit, die zu produzierende Menge und welche Ressource den Einzelvorgang verarbeitet. Der Bericht "Arbeitsplan" sammelt die gleichen Informationen auf der gleichen Seite, aber druckt keine Seite für jeden Einzelvorgang aus. Der Bericht "Arbeitsplanliste" zeigt nur die Arbeitsgänge aber nicht die Einzelvorgänge an. Daher ist für diesen Bericht keine Feinterminierung erforderlich, aber sie kann verwendet werden, wenn Produktionsaufträge auf der Arbeitsgangsebene geplant werden.  
5. Klicken Sie auf das Kontrollkästchen "Arbeitsplanliste drucken".
6. Klicken Sie auf "OK".
7. Schließen Sie die Seite.


