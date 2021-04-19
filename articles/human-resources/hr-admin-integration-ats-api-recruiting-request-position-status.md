---
title: Positionsstatus ders Personalbeschaffungsantrags
description: In diesem Thema wird der Optionssatz zum Status der Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789731"
---
# <a name="recruiting-request-position-status"></a>Positionsstatus ders Personalbeschaffungsantrags

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird der Optionssatz zum Status der Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmrecruitingrequestpositionstatus

Diese Aufzählung bietet den Optionssatz für die Statuswerte jeder Position eines Personalbeschaffungsantrags in der Entität RecruitingRequestPosition.

| Wert | Etikett | Beschreibung |
| --- | --- | --- |
| 200000000 | Öffentlich | Die Position im Personalbeschaffungsantrag ist offen für die Rekrutierung. Dies bedeutet nicht, dass für die Position derzeit keine Positionszuweisung aktiv ist. Zum Zeitpunkt der Einstellung befindet sich möglicherweise ein Mitarbeiter in der Position. Es wird nur angezeigt, dass die Position im Rahmen des Personalbeschaffungsantrags für die Rekrutierung verfügbar ist. |
| 200000001 | Besetzt | Eine Arbeitskraft wurde für die Zuordnung zur Position ausgewählt. |
| 200000002 | Storniert | Der Antrag auf Einstellung für diese Position wurde storniert. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]