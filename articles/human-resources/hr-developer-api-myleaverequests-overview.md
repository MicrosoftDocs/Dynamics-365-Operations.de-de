---
title: MyLeaveRequests-Überblick
description: Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054955"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests-Überblick

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.

## <a name="key"></a>Schlüssel

  | Eigenschaftenname | Datentyp |
  |---------------|-----------|
  | dataAreaId    | Zeichenfolge    |
  | RequestId     | Zeichenfolge    |
  | LeaveType     | Zeichenfolge    |
  | LeaveDate     | Datum      |
  
## <a name="properties"></a>Eigenschaften

  | Eigenschaftenname     | Datentyp | Erforderlich |
  |-------------------|-----------|----------|
  | dataAreaId        | Zeichenfolge    | X        |
  | RequestId         | Zeichenfolge    | X        |
  | LeaveType         | Zeichenfolge    | X        |
  | LeaveDate         | Datum      | X        |
  | ReasonCodeId      | Zeichenfolge    |          |
  | PersonnelNumber   | Zeichenfolge    | X        |
  | RequestDate       | Datum      | X        |
  | Kommentar           | Zeichenfolge    |          |
  | Status            | Option      | X        |
  | Dauer            | Gleitkommazahl      |          |
  | HalfDayDefinition | Option      |          |

## <a name="actions"></a>Aktionen

 | Aktivitätsname                               | Beschreibung                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [Übermitteln](hr-developer-api-myleaverequests-submit.md)   | Übermitteln Sie die Anforderung, die vom Workflow verarbeitet werden soll. |

## <a name="see-also"></a>Siehe auch

- [Urlaubsanforderung an Workflow übermitteln](hr-developer-api-myleaverequests-submit.md)
- [Authentifizierung](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]