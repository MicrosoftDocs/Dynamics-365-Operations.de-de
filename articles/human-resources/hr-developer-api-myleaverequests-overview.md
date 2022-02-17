---
title: MyLeaveRequests-Überblick
description: Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41ef8c6fc0e896e7f2cefd94801abab610083b81
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070854"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests-Überblick


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
