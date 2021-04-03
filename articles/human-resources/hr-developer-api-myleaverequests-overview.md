---
title: MyLeaveRequests-Überblick
description: Die MyLeaveRequests-Entität in Microsoft Dynamics 365 Human Resources stellt die Liste der Urlaubsanforderungen im System bereit, die auf diejenigen Anforderungen beschränkt sind, auf die der aktuelle Benutzer, der die Entität abfragt, zugreifen kann.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465509"
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