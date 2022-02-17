---
title: Bewertungsebene
description: In diesem Thema wird die Entität „Bewertungsstufe“ für Dynamics 365 Human Resources beschrieben.
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
ms.openlocfilehash: a821e3cd90e85571da4a09f5dd564beb2de35989
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068633"
---
# <a name="rating-level"></a>Bewertungsebene


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema wird die Entität „Bewertungsstufe“ für Dynamics 365 Human Resources beschrieben.

Physischer Name: mshr_hcmratinglevelentity

## <a name="description"></a>Beschreibung

Diese Entität stellt die verfügbaren Bewertungsstufen für Qualifikationen bereit. Die Bewertungsstufen gelten für alle juristischen Personen.

## <a name="json-representation"></a>JSON-Darstellung

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschaften

| Eigenschaft<br>**Physikalischer Name**<br>**_Typ_** | Verwenden | Beschreibung |
| --- | --- | --- |
| **Bewertungsstufenentitätskennung**<br>mshr_hcmratinglevelentityid<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Vom System generiert | Der vom System generierte eindeutige Bezeichner der Stufe. |
| **Bewertungsstufenkennung**<br>mshr_ratinglevelid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Vom Benutzer lesbarer eindeutiger Bezeichner der Stufe. |
| **Bewertungsmodellkennung**<br>mshr_ratingmodelid<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Das Bewertungsmodell, zu dem die Bewertungsstufe gehört. |
| **Bewertungsmodellentitätskennung**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Schreibgeschützt<br>Erforderlich<br>Fremdschlüssel: mshr_hcmratingmodelentityid von mshr_hcmratingmodelentity | Der vom System generierte Bezeichner für das Bewertungsmodell, zu dem die Bewertungsstufe gehört. |
| **Beschreibung**<br>mshr_description<br>*Zeichenfolge* | Lesen/Schreiben<br>Erforderlich | Die Beschreibung der Bewertungsstufe. |
| **Faktor**<br>mshr_factor<br>*Ganzzahl* | Lesen/Schreiben<br>Erforderlich | Der Faktor für die Bewertungsstufe. Hier wird ein Faktor eingegeben, durch den die Ergebnisse normalisiert werden, wenn Elemente mit einer unterschiedlichen Anzahl von Ebenen verglichen werden. Der Wert muss eine Ganzzahl zwischen 0 und 9 sein. |
| **Hinweis**<br>mshr_note<br>*Zeichenfolge* | Lesen/Schreiben<br>Optional | Alle mit der Bewertungsstufe verbundenen Notizen. |
| **Primärfeld**<br>mshr_primaryfield<br>*Zeichenfolge* | Schreibgeschützt<br>Erforderlich | Feld, das als ein weitere Bezeichner des Entitätsdatensatzes verwendet werden kann. Kombination aus Bewertungsstufenkennung und Bewertungsmodellkennung. |

## <a name="see-also"></a>Siehe auch

[Einführung der API zur Integration des Bewerber-Tracking-Systems](hr-admin-integration-ats-api-introduction.md)<br>
[Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
