---
title: Urlaubsanforderung an Workflow übermitteln
description: In Microsoft Dynamics 365 Human Resources können Sie die Anwendungsprogrammierschnittstelle (API) MyLeaveRequests submit () verwenden, um eine Urlaubsanfrage an den Workflow zu übermitteln.
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
ms.openlocfilehash: 7552a4c921dc4a88034b5d2c87d5a9b47d699ae3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418606"
---
# <a name="submit-a-leave-request-to-workflow"></a>Urlaubsanforderung an Workflow übermitteln

In Microsoft Dynamics 365 Human Resources können Sie die Anwendungsprogrammierschnittstelle (API) MyLeaveRequests submit () verwenden, um eine Urlaubsanfrage an den Workflow zu übermitteln. Diese API wird als Aktion für die OData-Entität MyLeaveRequests verfügbar gemacht.

## <a name="prerequisites"></a>Voraussetzungen

Die Urlaubsanforderung muss in der Datenbank gespeichert und über die MyLeaveRequests-Entität abrufbar sein.

## <a name="permissions"></a>Berechtigungen

Zum Aufrufen dieser API ist eine der folgenden Berechtigungen erforderlich. Weitere Informationen zu Berechtigungen und zu ihrer Auswahl finden Sie unter [Authentifizierung](hr-developer-api-authentication.md).

| Berechtigungstyp                    | Berechtigungen (von den mit den wenigsten bis zu den meisten Rechten) |
|------------------------------------|--------------------------------------------------------|
| Delegiert (Geschäfts- oder Schulkonto) | benutzer\_identitätswechsel                                    |

## <a name="https-request"></a>HTTPS-Anforderung

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Die Anforderung entspricht den OData-Standards. Die Parameter {requestId}, {leaveType}, {leaveDate} und {dataArea} beziehen sich auf die Felder, die den zusammengesetzten natürlichen Schlüssel für die MyLeaveRequests-Entität bilden.

> [!NOTE]
> Während sich die Felder für die MyLeaveRequests-Entität auf eine einzelne Zeile in der Urlaubsanforderung beziehen, wird beim Aufrufen der Übermittlungs-API die gesamte Urlaubsanforderung (alle Zeilen) an den Workflow übermittelt.

### <a name="request-headers"></a>Anforderungskopfzeile

| Header         | Value                     |
|----------------|---------------------------|
| Autorisierung  | Bearer-{token} (erforderlich) |
| Inhaltstyp   | Anwendung/JSON          |

### <a name="request-body"></a>Anforderungstext

Geben Sie für diese Methode keinen Anforderungstext an.

### <a name="response"></a>Antwort

Eine erfolgreiche Antwort ist immer eine Antwort der Form **204 Kein Inhalt**.

Nicht autorisierte Aufrufer erhalten eine Antwort der Form **401 Nicht Autorisiert** oder **403 Verboten**.

Wenn die Übermittlung fehlschlägt (z. B. aufgrund einer Validierung), hat die Antwort die Form **500 Serverfehler** und der Antworttext enthält ein JSON-Objekt mit weiteren Details.

## <a name="example"></a>Beispiel

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>Validierungs- und Fehlermeldungen

Im Rahmen des Aufrufs der Übermittlungs-API führt die Personalverwaltung vor der Übermittlung eine Geschäftslogikvalidierung durch, um sicherzustellen, dass die Urlaubsanforderungen für die Übermittlung gültig ist. Die möglichen Fehlermeldungen für die Antwort, wenn die Validierung fehlschlägt, sind:

 - Die Anforderung würde den Saldo "{LeaveTypeId}" unterhalb des zulässigen Mindestguthabens {date} ansetzen.
 - Urlaubsantrag mit Status „Abgeschlossen“ kann nicht übermittelt werden.
 - Anforderung kann nicht übermittelt oder gespeichert werden, da keine Änderungen vorgenommen wurden. Ergänzen oder aktualisieren Sie den Betrag oder den Urlaubstyp und versuchen Sie es erneut.
 - Der eingegebene Urlaubsantrag enthält einen oder mehrere Tage mit demselben Datum und demselben Urlaubstyp wie eine vorhandene ausstehende Anforderung. Rufen Sie die vorhandene Anforderung zurück, um Änderungen vorzunehmen.
 - Der Ursachencode '{ReasonCodeId}' gilt für keinen der Urlaubstypen in dem Antrag.
 - Der Urlaubstyp '{LeaveTypeId}' erfordert einen Ursachencode. Wählen Sie den entsprechenden Typ und den Ursachencode aus.
 - Der Urlaubsantrag wurde nicht erfolgreich übermittelt. Der Urlaubsantrag wurde als Anforderungsentwurf gespeichert.

## <a name="see-also"></a>Siehe auch

- [MyLeaveRequests-Überblick](hr-developer-api-myleaverequests-overview.md)
- [Authentifizierung](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]