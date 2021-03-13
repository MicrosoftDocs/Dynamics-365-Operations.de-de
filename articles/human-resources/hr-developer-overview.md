---
title: Entwicklungsüberblick
description: Dieses Entwicklerhandbuch enthält eine API- und eine Referenz für benutzerdefinierte Felder. Es enthält außerdem Informationen zur Integration in andere Apps.
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
ms.openlocfilehash: 517febd7967350956a28dfd9d11e4042456c7da0
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115389"
---
# <a name="development-overview"></a><span data-ttu-id="14704-104">Entwicklungsüberblick</span><span class="sxs-lookup"><span data-stu-id="14704-104">Development overview</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="14704-105">Dieses Entwicklerhandbuch enthält eine API- und eine Referenz für benutzerdefinierte Felder.</span><span class="sxs-lookup"><span data-stu-id="14704-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="14704-106">Es enthält außerdem Informationen zur Integration in andere Apps.</span><span class="sxs-lookup"><span data-stu-id="14704-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="14704-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="14704-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="14704-108">Mit Power Apps und Power Automate erweitern</span><span class="sxs-lookup"><span data-stu-id="14704-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="14704-109">Datenentitäten: Personalverwaltung in Dataverse</span><span class="sxs-lookup"><span data-stu-id="14704-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="14704-110">Benutzerdefinierte Felder</span><span class="sxs-lookup"><span data-stu-id="14704-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="14704-111">Datenintegration einrichten</span><span class="sxs-lookup"><span data-stu-id="14704-111">Set up data integration</span></span>
  - [<span data-ttu-id="14704-112">Datenintegrationstechnologie auswählen</span><span class="sxs-lookup"><span data-stu-id="14704-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="14704-113">Dataverse-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="14704-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="14704-114">Integration mit Finance konfigurieren</span><span class="sxs-lookup"><span data-stu-id="14704-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="14704-115">Integration mit Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="14704-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="14704-116">Eine wiederkehrende Datenexport-App erstellen</span><span class="sxs-lookup"><span data-stu-id="14704-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="14704-117">In Office integrieren</span><span class="sxs-lookup"><span data-stu-id="14704-117">Integrate with Office</span></span>
    - [<span data-ttu-id="14704-118">Lernprogramm zur Office-Integration</span><span class="sxs-lookup"><span data-stu-id="14704-118">Office integration tutorial</span></span>](../dev-itpro/office-integration/office-integration-tutorial.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="14704-119">Entitätsdaten in Excel aktualisieren</span><span class="sxs-lookup"><span data-stu-id="14704-119">Update entity data in Excel</span></span>](../dev-itpro/office-integration/use-excel-add-in.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="14704-120">Möglichkeit „In Excel öffnen“ schaffen</span><span class="sxs-lookup"><span data-stu-id="14704-120">Create Open in Excel experiences</span></span>](../dev-itpro/office-integration/office-integration-edit-excel.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="14704-121">Problembehandlung bei der Office-Integration</span><span class="sxs-lookup"><span data-stu-id="14704-121">Troubleshoot Office integration</span></span>](../dev-itpro/office-integration/office-integration-troubleshooting.md?toc=/dynamics365/unified-operations/talent/toc.json)

- <span data-ttu-id="14704-122">Referenz zur Entitäts-API</span><span class="sxs-lookup"><span data-stu-id="14704-122">Entity API reference</span></span>
  - [<span data-ttu-id="14704-123">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="14704-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="14704-124">Entitäten</span><span class="sxs-lookup"><span data-stu-id="14704-124">Entities</span></span>
    - [<span data-ttu-id="14704-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="14704-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="14704-126">Urlaubsanforderung an Workflow übermitteln</span><span class="sxs-lookup"><span data-stu-id="14704-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="14704-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14704-127">See also</span></span>

- [<span data-ttu-id="14704-128">Neuerungen oder Änderungen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="14704-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="14704-129">Administratorhandbuch</span><span class="sxs-lookup"><span data-stu-id="14704-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="14704-130">Benutzerhandbuch</span><span class="sxs-lookup"><span data-stu-id="14704-130">User Guide</span></span>](hr-hrpro-overview.md)
