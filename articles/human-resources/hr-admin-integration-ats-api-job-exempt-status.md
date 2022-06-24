---
title: Stellenbefreiungsstatus
description: In diesem Artikel wird der Optionssatz für Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894671"
---
# <a name="job-exempt-status"></a>Stellenbefreiungsstatus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird der Optionssatz für Stellenbefreiungsstatus für Dynamics 365 Human Resources beschrieben.

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
