---
title: Berichterstellungsoptionen in Talent
description: "In diesem Thema wird erläutert, wie das Problem behoben wird, bei dem ein Kunde die Microsoft Dynamics 365 for Talent-Berichte anpassen möchte oder neue Berichte erstellen möchte."
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
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a>Berichterstellungsoptionen in Talent

[!include [banner](includes/banner.md)]

**Umgebungsdetails**

Dieses Problem gilt für alle Umgebungen.

**Symptom**

Der Kunde möchte Microsoft Dynamics 365 for Talent-Berichte anpassen oder neue Berichte erstellen.

**Abgang**

Der Benutzer kann die eingebetteten Microsoft Power BI-Berichte nicht anpassen.

**Lösung**

- Über die Core HR-Daten, die zum Common Data Service for Apps fließen, kann über den PowerApps CDS mit Power BI Desktop berichtet werden. Beachten Sie, dass Common Data Service for Apps eine Untergruppe von Core HR-Daten enthält. Weitere Informationen zu Power BI und Dashboards finden Sie unter [Power BI-Berichte und Dashboards mit PowerApps Common Data Service erstellen](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Elektronische Berichterstellung (EB) ist für manche Berichte in Talent verfügbar. Kundengesteuerte Anpassungen können über die EB-Konfigurationsoptionen erfolgen.
- Daten können nach Microsoft Excel oder Microsoft Word exportiert werden, indem die verschiedenen Datenentitäten verwendet werden, die Talent durch die Microsoft Office-Integration bereitstellt.

**Langfristige Lösung**

Zusätzliche Power BI-Optionen werden verfügbar sein und mehr Daten und Entitäten werden Teil von Common Data Service for Apps sein.

