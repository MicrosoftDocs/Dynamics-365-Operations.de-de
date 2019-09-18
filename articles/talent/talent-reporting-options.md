---
title: Berichterstellungsoptionen in Talent
description: In diesem Thema wird erläutert, wie das Problem behoben wird, bei dem ein Kunde die Microsoft Dynamics 365 for Talent-Berichte anpassen möchte oder neue Berichte erstellen möchte.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e7348a515b08523c15aa8f74d5616a3daf645b7
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741797"
---
# <a name="reporting-options-in-talent"></a>Berichtsoptionen in Talent

[!include [banner](includes/banner.md)]

**Umgebungsdetails**

Dieses Problem gilt für alle Umgebungen.

**Symptom**

Der Kunde möchte Microsoft Dynamics 365 for Talent-Berichte anpassen oder neue Berichte erstellen.

**Abgang**

Der Benutzer kann die eingebetteten Microsoft Power BI-Berichte nicht anpassen.

**Lösung**

- Über die Core HR-Daten, die zu Common Data Service  fließt, kann über den PowerApps Common Data Service Konnektor zu Power BI Desktop berichtet werden. Beachten Sie, dass Common Data Service eine Untergruppe von Core HR-Daten enthält. Weitere Informationen zu Power BI und Dashboards, finden [Erstellen Power BI Berichte und PowerApps Dashboards mit Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) Sie unter.
- Elektronische Berichterstellung (EB) ist für manche Berichte in Talent verfügbar. Kundengesteuerte Anpassungen können über die EB-Konfigurationsoptionen erfolgen.
- Daten können nach Microsoft Excel oder Microsoft Word exportiert werden, indem die verschiedenen Datenentitäten verwendet werden, die Talent durch die Microsoft Office-Integration bereitstellt.

**Langfristige Lösung**

Zusätzliche Power BI-Optionen werden verfügbar sein und mehr Daten und Entitäten werden Teil von Common Data Service  sein.
