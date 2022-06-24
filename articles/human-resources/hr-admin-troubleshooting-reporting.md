---
title: Berichtsoptionen
description: In diesem Artikel wird erklärt, wie Sie Microsoft Dynamics 365 Human Resources-Berichte anpassen oder neue Berichte erstellen.
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
ms.openlocfilehash: 421883d314fb27b4592e9be0455946ab3730fb1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856337"
---
# <a name="reporting-options"></a>Berichtsoptionen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
