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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125568"
---
# <a name="job-exempt-status"></a>Stellenbefreiungsstatus

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
