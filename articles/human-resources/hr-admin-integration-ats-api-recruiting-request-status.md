---
title: Status des Personalbeschaffungsantrags
description: In diesem Thema wird der Optionssatz zum Status des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059183"
---
# <a name="recruiting-request-status"></a>Status des Personalbeschaffungsantrags

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird der Optionssatz zum Status des Personalbeschaffungsantrags für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmrecruitingrequeststatus

Diese Aufzählung bietet den Optionssatz für die Statuswerte eines RecruitingRequest.

| Wert | Etikett | Beschreibung |
| --- | --- | --- |
| 200000000 | Übersicht | Die Anfrage befindet sich im Entwurf und ist nicht für die aktive Rekrutierung bereit. |
| 200000001 | In Überprüfung | Die Anforderung wurde gesendet und wird zur Genehmigung durch den Workflow weitergeleitet. Nur verfügbar, wenn der Workflow aktiviert ist. |
| 200000002 | Ausstehend | Die Anfrage wartet auf die Workflow-Aktion. Nur verfügbar, wenn der Workflow aktiviert ist. |
| 200000003 | Storniert | Die Anforderung wurde storniert. Nur verfügbar, wenn der Workflow aktiviert ist. |
| 200000004 | Verweigert | Die Anforderung wurde abgelehnt. Nur verfügbar, wenn der Workflow aktiviert ist. |
| 200000005 | Aktiv | Jeder Workflow wird abgeschlossen und genehmigt, und die Anfrage ist für die aktive Rekrutierung bereit. |
| 200000006 | Abgeschlossen | Der Personalbeschaffungsantrage wird geschlossen. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]