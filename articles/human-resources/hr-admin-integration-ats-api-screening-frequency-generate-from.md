---
title: Screening-Häufigkeit erzeugen aus
description: In diesem Artikel wird der Optionssatz „Screening-Häufigkeit erzeugen aus“ für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 846a35a2e8ca39ed9479601d99c8c515328d8ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879307"
---
# <a name="screening-frequency-generate-from"></a>Screening-Häufigkeit erzeugen aus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird der Optionssatz „Screening-Häufigkeit erzeugen aus“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmfrequencygeneratefrom

Diese Aufzählung bietet den Optionssatz von Werten zum Bestimmen des Startdatums der Berechnung für das Nächste erforderliche Screening.

| Wert | Etikett | Beschreibung |
| --- | --- | --- |
| 200000000 Nicht ausgewählt | Es wurde kein Wert ausgewählt. |
| 200000001 Abschlussdatum | Die Berechnung erfolgt ab dem letzten abgeschlossenen Screening-Datum. |
| 200000002 Datum erforderlich | Die Berechnung erfolgt ab dem letzten erforderlichen Screening-Datum. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
