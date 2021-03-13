---
title: Probleme bei der anfänglichen Einrichtung behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Einrichtung der Integration vom dualen Schreiben zusammenhängen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: cfbc1ab3ef6d47f6ec2d8ca4ca4b8940784e6e49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129980"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="bbd32-103">Probleme bei der anfänglichen Einrichtung behandeln</span><span class="sxs-lookup"><span data-stu-id="bbd32-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="bbd32-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="bbd32-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="bbd32-105">Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der initialen Einrichtung der Integration vom dualen Schreiben zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="bbd32-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbd32-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="bbd32-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="bbd32-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bbd32-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="bbd32-108">Sie können eine Finance and Operations App nicht mit Dataverse verknüpfen</span><span class="sxs-lookup"><span data-stu-id="bbd32-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="bbd32-109">**Erforderliche Rolle zur Einrichtung von dualem Schreiben:** Systemadministrator in Finance and Operations-Apps und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="bbd32-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="bbd32-110">Fehler auf der Seite **Einrichtungs-Link für Dataverse** werden normalerweise durch unvollständige Setup- oder Berechtigungsprobleme verursacht.</span><span class="sxs-lookup"><span data-stu-id="bbd32-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="bbd32-111">Stellen Sie sicher, dass die gesamte Integritätsprüfung die Seite **Einrichtungs-Link zu Dataverse** wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bbd32-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="bbd32-112">Sie können Duales Schreiben nur verknüpfen, wenn die gesamte Integritätsprüfung bestanden wurde.</span><span class="sxs-lookup"><span data-stu-id="bbd32-112">You can't link dual-write unless the whole health check passes.</span></span>

![Erfolgreiche Integritätsprüfung](media/health_check.png)

<span data-ttu-id="bbd32-114">Sie müssen Azure AD Mandantenadministrator-Anmeldeinformationen haben, um Finance and Operations und Dataverse Umgebungen zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="bbd32-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="bbd32-115">Nachdem Sie die Umgebungen verknüpft haben, können sich Benutzer mit ihren Kontoanmeldeinformationen anmelden und eine vorhandene Tabellenzuordnung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bbd32-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="bbd32-116">Fehler beim Öffnen des Links zur Seite Dataverse</span><span class="sxs-lookup"><span data-stu-id="bbd32-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="bbd32-117">**Erforderliche Anmeldeinformationen zum Lösen des Problems:** Azure AD Mandant Admin</span><span class="sxs-lookup"><span data-stu-id="bbd32-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="bbd32-118">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie den **Link zur Dataverse** Seite in einer Finance and Operations App öfnen:</span><span class="sxs-lookup"><span data-stu-id="bbd32-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="bbd32-119">*Der Antwortstatuscode zeigt keinen Erfolg an: 404 (Nicht gefunden).*</span><span class="sxs-lookup"><span data-stu-id="bbd32-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="bbd32-120">Dieser Fehler tritt auf, wenn der Zustimmungsschritt nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bbd32-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="bbd32-121">Melden Sie sich bei Portal.Azure.com an, um zu überprüfen, ob der Zustimmungsschritt abgeschlossen wurde mithilfe dem Azure AD Mandantenadministratorkonto, und prüfen Sie, ob die Drittanbieter-App die über die ID verfügt **33976c19-1db5-4c02-810e-c243db79efde** in der Azure AD **Unternehmensanwendungen** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bbd32-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="bbd32-122">Wenn dies nicht der Fall ist, müssen Sie die Zustimmung der App geben.</span><span class="sxs-lookup"><span data-stu-id="bbd32-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="bbd32-123">Führen Sie die folgenden Schritte aus, um die App-Zustimmung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="bbd32-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="bbd32-124">Öffnen Sie die folgende URL mithilfe Ihrer Administratoranmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="bbd32-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="bbd32-125">Sie sollten zur Zustimmung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="bbd32-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="bbd32-126">Wählen **Akzeptieren**, um anzugeben, dass Sie Ihre Zustimmung zur Installation der App mit der ID **33976c19-1db5-4c02-810e-c243db79efde** in Ihrem Mandant geben.</span><span class="sxs-lookup"><span data-stu-id="bbd32-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="bbd32-127">Diese App muss verlinkt werden mit Dataverse und Finance and Operations Apps.</span><span class="sxs-lookup"><span data-stu-id="bbd32-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="bbd32-128">Wenn Sie Probleme mit diesem Schritt haben, öffnen Sie Ihren Browser im Inkognito-Modus (in Google Chrome) oder im InPrivate-Modus (in Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="bbd32-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="bbd32-129">Stellen Sie sicher, dass Unternehmensdaten und Teams Duales Schreiben während der Verknüpfung korrekt eingerichtet sind</span><span class="sxs-lookup"><span data-stu-id="bbd32-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="bbd32-130">Um sicherzustellen, dass Duales Schreiben ordnungsgemäß funktioniert, werden die Unternehmen, die Sie während der Konfiguration auswählen, in der Liste Dataverse Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="bbd32-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="bbd32-131">Standardmäßig sind diese Unternehmen schreibgeschützt und die **IsDualWriteEnable** Eigenschaft ist auf **Wahr** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bbd32-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="bbd32-132">Darüber hinaus werden der Eigentümer und das Team der Geschäftseinheit mit Standardbesitz erstellt und enthalten den Firmennamen.</span><span class="sxs-lookup"><span data-stu-id="bbd32-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="bbd32-133">Stellen Sie vor dem Aktivieren der Karten sicher, dass der Standardteambesitzer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bbd32-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="bbd32-134">Um die Tabelle **Unternehmen (CDM\_Unternehmen)** zu finden, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="bbd32-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="bbd32-135">Wählen Sie in der modellgesteuerten App in Dynamics 365 den Filter in der oberen rechten Ecke aus.</span><span class="sxs-lookup"><span data-stu-id="bbd32-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="bbd32-136">Wählen Sie in der Dropdownliste **Unternehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="bbd32-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="bbd32-137">Wählen **Ausführen**, um die Ergebnisse zu sehen.</span><span class="sxs-lookup"><span data-stu-id="bbd32-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="bbd32-138">Wählen Sie die Firma aus, die bei der Konfiguration von Dualem Schreiben verknüpft war.</span><span class="sxs-lookup"><span data-stu-id="bbd32-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="bbd32-139">Stellen Sie sicher, dass die Spalte **Standardbesitzerteam** einen Wert hat.</span><span class="sxs-lookup"><span data-stu-id="bbd32-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="bbd32-140">In der folgenden Abbildung ist die Spalte **Standardbesitzerteam** auf **USMF – Duales Schreiben** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bbd32-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![Überprüfen des Standardbesitzerteams](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="bbd32-142">Finden Sie das Limit für die Anzahl der juristischen Tabellen oder Unternehmen, die für duales Schreiben verknüpft werden können</span><span class="sxs-lookup"><span data-stu-id="bbd32-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="bbd32-143">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Zuordnung zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="bbd32-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="bbd32-144">*Dualer Schreibfehler – Plugin-Registrierung fehlgeschlagen: \[(Partitionszuordnung für Projekt DWM kann nicht abgerufen werden-1ae35e60-4bc2-4905-88ea-69efd3b29260–7f12cb89-1550-42e2-858e-4761fc1443ea . Fehler überschreitet die maximal zulässigen Partitionen für die Zuordnung von DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260–7f12cb89-1550-42e2-858e-4761fc1443ea)\]Ein oder mehrere Fehler sind aufgetreten.*</span><span class="sxs-lookup"><span data-stu-id="bbd32-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="bbd32-145">Die aktuelle Limite beim Verknüpfen der Umgebungen beträgt ungefähr 40 juristische Tabellen.</span><span class="sxs-lookup"><span data-stu-id="bbd32-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="bbd32-146">Dieser Fehler tritt auf, wenn Sie versuchen, Karten zu aktivieren, und mehr als 40 juristische Tabellen zwischen den Umgebungen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="bbd32-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>
