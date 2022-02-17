---
title: Stellenbefreiungsstatus
description: In diesem Thema wird der Optionssatz Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 29d3c4fd37a219b520172c6866c5fec488c698f7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064990"
---
# <a name="job-exempt-status"></a>Stellenbefreiungsstatus


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
