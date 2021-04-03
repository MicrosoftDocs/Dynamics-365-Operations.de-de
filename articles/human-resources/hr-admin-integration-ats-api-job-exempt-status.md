---
title: Stellenbefreiungsstatus
description: In diesem Thema wird der Optionssatz Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464451"
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