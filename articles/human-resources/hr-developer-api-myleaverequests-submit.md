---
title: Urlaubsanforderung an Workflow übermitteln
description: ''
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009194"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="d33d9-102">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="d33d9-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="d33d9-103">In Microsoft Dynamics 365 Human Resources können Sie die Anwendungsprogrammierschnittstelle (API) MyLeaveRequests submit () verwenden, um eine Urlaubsanfrage an den Workflow zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d33d9-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="d33d9-104">Diese API wird als Aktion für die OData-Entität MyLeaveRequests verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="d33d9-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d33d9-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d33d9-105">Prerequisites</span></span>

<span data-ttu-id="d33d9-106">Die Urlaubsanforderung muss in der Datenbank gespeichert und über die MyLeaveRequests-Entität abrufbar sein.</span><span class="sxs-lookup"><span data-stu-id="d33d9-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="d33d9-107">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d33d9-107">Permissions</span></span>

<span data-ttu-id="d33d9-108">Zum Aufrufen dieser API ist eine der folgenden Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d33d9-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d33d9-109">Weitere Informationen zu Berechtigungen und zu ihrer Auswahl finden Sie unter [Authentifizierung](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="d33d9-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="d33d9-110">Berechtigungstyp</span><span class="sxs-lookup"><span data-stu-id="d33d9-110">Permission type</span></span>                    | <span data-ttu-id="d33d9-111">Berechtigungen (von den mit den wenigsten bis zu den meisten Rechten)</span><span class="sxs-lookup"><span data-stu-id="d33d9-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="d33d9-112">Delegiert (Geschäfts- oder Schulkonto)</span><span class="sxs-lookup"><span data-stu-id="d33d9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d33d9-113">benutzer\_identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="d33d9-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="d33d9-114">HTTPS-Anforderung</span><span class="sxs-lookup"><span data-stu-id="d33d9-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="d33d9-115">Die Anforderung entspricht den OData-Standards.</span><span class="sxs-lookup"><span data-stu-id="d33d9-115">The request conforms to OData standards.</span></span> <span data-ttu-id="d33d9-116">Die Parameter {requestId}, {leaveType}, {leaveDate} und {dataArea} beziehen sich auf die Felder, die den zusammengesetzten natürlichen Schlüssel für die MyLeaveRequests-Entität bilden.</span><span class="sxs-lookup"><span data-stu-id="d33d9-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="d33d9-117">Während sich die Felder für die MyLeaveRequests-Entität auf eine einzelne Zeile in der Urlaubsanforderung beziehen, wird beim Aufrufen der Übermittlungs-API die gesamte Urlaubsanforderung (alle Zeilen) an den Workflow übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d33d9-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="d33d9-118">Anforderungskopfzeile</span><span class="sxs-lookup"><span data-stu-id="d33d9-118">Request headers</span></span>

| <span data-ttu-id="d33d9-119">Header</span><span class="sxs-lookup"><span data-stu-id="d33d9-119">Header</span></span>         | <span data-ttu-id="d33d9-120">Value</span><span class="sxs-lookup"><span data-stu-id="d33d9-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="d33d9-121">Autorisierung</span><span class="sxs-lookup"><span data-stu-id="d33d9-121">Authorization</span></span>  | <span data-ttu-id="d33d9-122">Bearer-{token} (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="d33d9-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="d33d9-123">Inhaltstyp</span><span class="sxs-lookup"><span data-stu-id="d33d9-123">Content-Type</span></span>   | <span data-ttu-id="d33d9-124">Anwendung/JSON</span><span class="sxs-lookup"><span data-stu-id="d33d9-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="d33d9-125">Anforderungstext</span><span class="sxs-lookup"><span data-stu-id="d33d9-125">Request body</span></span>

<span data-ttu-id="d33d9-126">Geben Sie für diese Methode keinen Anforderungstext an.</span><span class="sxs-lookup"><span data-stu-id="d33d9-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="d33d9-127">Antwort</span><span class="sxs-lookup"><span data-stu-id="d33d9-127">Response</span></span>

<span data-ttu-id="d33d9-128">Eine erfolgreiche Antwort ist immer eine Antwort der Form **204 Kein Inhalt**.</span><span class="sxs-lookup"><span data-stu-id="d33d9-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="d33d9-129">Nicht autorisierte Aufrufer erhalten eine Antwort der Form **401 Nicht Autorisiert** oder **403 Verboten**.</span><span class="sxs-lookup"><span data-stu-id="d33d9-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="d33d9-130">Wenn die Übermittlung fehlschlägt (z. B. aufgrund einer Validierung), hat die Antwort die Form **500 Serverfehler** und der Antworttext enthält ein JSON-Objekt mit weiteren Details.</span><span class="sxs-lookup"><span data-stu-id="d33d9-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="d33d9-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d33d9-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="d33d9-132">Validierungs- und Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="d33d9-132">Validation and error messages</span></span>

<span data-ttu-id="d33d9-133">Im Rahmen des Aufrufs der Übermittlungs-API führt die Personalverwaltung vor der Übermittlung eine Geschäftslogikvalidierung durch, um sicherzustellen, dass die Urlaubsanforderungen für die Übermittlung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d33d9-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="d33d9-134">Die möglichen Fehlermeldungen für die Antwort, wenn die Validierung fehlschlägt, sind:</span><span class="sxs-lookup"><span data-stu-id="d33d9-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="d33d9-135">Die Anforderung würde den Saldo "{LeaveTypeId}" unterhalb des zulässigen Mindestguthabens {date} ansetzen.</span><span class="sxs-lookup"><span data-stu-id="d33d9-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="d33d9-136">Urlaubsantrag mit Status „Abgeschlossen“ kann nicht übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d33d9-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="d33d9-137">Anforderung kann nicht übermittelt oder gespeichert werden, da keine Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="d33d9-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="d33d9-138">Ergänzen oder aktualisieren Sie den Betrag oder den Urlaubstyp und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="d33d9-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="d33d9-139">Der eingegebene Urlaubsantrag enthält einen oder mehrere Tage mit demselben Datum und demselben Urlaubstyp wie eine vorhandene ausstehende Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d33d9-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="d33d9-140">Rufen Sie die vorhandene Anforderung zurück, um Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="d33d9-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="d33d9-141">Der Ursachencode '{ReasonCodeId}' gilt für keinen der Urlaubstypen in dem Antrag.</span><span class="sxs-lookup"><span data-stu-id="d33d9-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="d33d9-142">Der Urlaubstyp '{LeaveTypeId}' erfordert einen Ursachencode.</span><span class="sxs-lookup"><span data-stu-id="d33d9-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="d33d9-143">Wählen Sie den entsprechenden Typ und den Ursachencode aus.</span><span class="sxs-lookup"><span data-stu-id="d33d9-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="d33d9-144">Der Urlaubsantrag wurde nicht erfolgreich übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d33d9-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="d33d9-145">Der Urlaubsantrag wurde als Anforderungsentwurf gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d33d9-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="d33d9-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d33d9-146">See also</span></span>

- [<span data-ttu-id="d33d9-147">MyLeaveRequests-Überblick</span><span class="sxs-lookup"><span data-stu-id="d33d9-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="d33d9-148">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d33d9-148">Authentication</span></span>](hr-developer-api-authentication.md)