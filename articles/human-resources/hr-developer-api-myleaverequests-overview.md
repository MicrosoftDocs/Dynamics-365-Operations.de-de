---
title: MyLeaveRequests-Überblick
description: Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418607"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests-Überblick

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