---
title: Stellenbefreiungsstatus
description: In diesem Thema wird der Optionssatz Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798296"
---
# <a name="job-exempt-status"></a>Stellenbefreiungsstatus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird der Optionssatz Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.

Physischer Name: cdm_jobexemptstatus

Diese Aufzählung gibt den Optionssatz für FLSA-Stellenbefreiungsstatuswerte an. Dies wird im vorhandenen Optionssatz cdm_jobexemptstatus bereitstellt.

| Wert | Etikett | Beschreibung |
| --- | --- | --- |
| 200000000 | Befreit | Die Stelle hat einen Ausnahmestatus basierend auf den FLSA-Richtlinien. |
| 200000001 | NonExempt | Die Stelle hat einen Nicht-Ausnahmestatus basierend auf den FLSA-Richtlinien. |
| 200000002 | Trifft nicht zu | Die FLSA-Statusrichtlinien gelten nicht für die Stelle. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]