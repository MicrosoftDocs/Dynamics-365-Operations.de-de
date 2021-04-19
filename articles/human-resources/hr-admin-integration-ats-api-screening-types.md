---
title: Prüfungstypen
description: In diesem Thema wird die Screening-Typen-Entität für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805129"
---
# <a name="screening-types"></a>Prüfungstypen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Screening-Typen-Entität für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmscreeningtypeentity

## <a name="description"></a>Beschreibung

Diese Einheit beschreibt die vom Unternehmen eingerichteten Screening-Typen vor der Einstellung und laufende Mitarbeiter-Screening-Prozesse.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Screening-Typ-Entitätskennung**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Eindeutiger primärer Bezeichner für den Screening-Typ-Datensatz. |
| **Screening-Typ-Kennung**<br>mshr_screeningtypeid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Benutzerdefinierter eindeutiger Bezeichner für den Screening-Typ. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Beschreibung des Screening-Typs. |
| **Einheit der Häufigkeit**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Beschreibt die Häufigkeit, mit der das Screening für die zugewiesene Person durchgeführt werden muss. |
| **Formular erstellen**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom-Optionssatz* | Lesen/Schreiben<br>Erforderlich | Wenn der Häufigkeitswert ein anderer Wert als „Nur einmalig“ ist, bestimmt der GenerateFrom-Wert das Datum, ab dem das nächste Screening-Ereignis berechnet werden soll. |
| **Häufigkeitsintervall**<br>mshr_frequencyinterval<br>*Ganzzahl* | Lesen/Schreiben<br>Erforderlich | Wenn der Häufigkeitswert ein anderer Wert als „Nur einmalig“ ist, müssen Sie ein Intervall für die Zeiteinheiten zwischen den einzelnen Screening-Ereignissen definieren. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]