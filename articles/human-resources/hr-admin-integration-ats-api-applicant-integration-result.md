---
title: Bewerberintegrationsergebnis
description: In diesem Thema wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467552"
---
# <a name="applicant-integration-result"></a>Bewerberintegrationsergebnis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmapplicantintegrationresult

Diese Aufzählung liefert den Status für einen Kandidatendatensatz.

| Wert | Etikett | Beschreibung |
| --- | --- | --- |
| 200000000 | Nicht verarbeitet | Der Kandidat wird noch geprüft. |
| 200000001 | Eingestellt | Der Kandidat wurde eingestellt. |
| 200000002 | Nicht eingestellt | Es wurde beschlossen, den Kandidaten nicht einzustellen. |
| 200000003 | Abgeschlossen | Der Kandidat wurde von der Prüfung ausgeschlossen. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]