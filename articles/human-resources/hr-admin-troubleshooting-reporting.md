---
title: Sonstige Berichtsoptionen
description: In diesem Artikel wird erläutert, wie das Problem behoben wird, bei dem ein Kunde die Microsoft Dynamics 365 Human Resources-Berichte anpassen möchte oder neue Berichte erstellen möchte.
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
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112640"
---
# <a name="reporting-options"></a>Sonstige Berichtsoptionen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Umgebungsdetails**

Dieses Problem gilt für alle Umgebungen.

**Symptom**

Der Kunde möchte Microsoft Dynamics 365 Human Resources-Berichte anpassen oder neue Berichte erstellen.

**Abgang**

Der Benutzer kann die eingebetteten Microsoft Power BI-Berichte nicht anpassen.

**Lösung**

- Über die Human Resources-Daten, die zu Dataverse fließen, kann über den Power Apps Dataverse-Connector zu Power BI Desktop berichtet werden. Beachten Sie, dass Dataverse eine Untergruppe von Human Resources-Daten enthält. Weitere Informationen zu Power BI und Dashboards finden Sie unter [Erstellen von Power BI-Berichten mit Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronische Berichterstellung (EB) ist für manche Berichte in Human Resources verfügbar. Kundengesteuerte Anpassungen können über die EB-Konfigurationsoptionen erfolgen.
- Daten können nach Microsoft Excel oder Microsoft Word exportiert werden, indem die verschiedenen Datenentitäten verwendet werden, die Human Resources durch die Microsoft Office-Integration bereitstellt.

**Langfristige Lösung**

Zusätzliche Power BI-Optionen werden verfügbar sein und mehr Daten und Entitäten werden Teil von Dataverse  sein.
