---
title: Positionsstatus ders Personalbeschaffungsantrags
description: In diesem Artikel wird der Optionssatz zum Status der Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846411"
---
# <a name="recruiting-request-position-status"></a>Positionsstatus ders Personalbeschaffungsantrags


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird der Optionssatz zum Status der Personalbeschaffungsantragsposition für Dynamics 365 Human Resources beschrieben.

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
