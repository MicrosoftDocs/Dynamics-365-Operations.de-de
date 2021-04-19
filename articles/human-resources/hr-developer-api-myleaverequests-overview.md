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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803632"
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