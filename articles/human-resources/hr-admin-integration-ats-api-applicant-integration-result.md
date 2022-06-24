---
title: Bewerberintegrationsergebnis
description: In diesem Artikel wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 84f0ba9b197866935535a68006cfdb8c18fa3ad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902313"
---
# <a name="applicant-integration-result"></a>Bewerberintegrationsergebnis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird der Optionssatz zum Ergebnis der Bewerberintegration für Dynamics 365 Human Resources beschrieben.

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
