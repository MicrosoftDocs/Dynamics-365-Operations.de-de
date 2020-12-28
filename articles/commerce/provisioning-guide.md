---
title: Eine Dynamics 365 Commerce-Evaluierungsumgebung bereitstellen
description: In diesem Thema wird erläutert, wie eine Evaluierungsumgebung in Microsoft Dynamics 365 Commerce bereitgestellt wird.
author: psimolin
manager: annbe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4412720"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="51cea-103">Eine Dynamics 365 Commerce-Evaluierungsumgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="51cea-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51cea-104">In diesem Thema wird erläutert, wie eine Evaluierungsumgebung in Microsoft Dynamics 365 Commerce bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="51cea-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="51cea-105">Bevor Sie beginnen, empfehlen wir, dass Sie einen kurzen Blick in dieses Thema werfen, um eine Vorstellung davon zu bekommen, was der Prozess erfordert.</span><span class="sxs-lookup"><span data-stu-id="51cea-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="51cea-106">Commerce-Auswertungsumgebungen sind nicht allgemein verfügbar und sie werden Partner und Kunden auf Anfrage gewährt.</span><span class="sxs-lookup"><span data-stu-id="51cea-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="51cea-107">Für weitere Informationen wenden Sie sich an den Ansprechpartner Ihres Microsoft-Partners.</span><span class="sxs-lookup"><span data-stu-id="51cea-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="51cea-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="51cea-108">Overview</span></span>

<span data-ttu-id="51cea-109">Um eine Commerce-Evaluierungsumgebung erfolgreich bereitzustellen, müssen Sie ein Projekt mit einem bestimmten Produktnamen und -Typ erstellen.</span><span class="sxs-lookup"><span data-stu-id="51cea-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="51cea-110">Bei der Umgebung und der Commerce Scale Unit (CSU) gibt es auch einige spezifische Parameter, die Sie verwenden müssen, um später E-Commerce bereitstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="51cea-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="51cea-111">In den Anweisungen in diesem Thema werden alle Schritte, die zum Ausführen der Bereitstellung erforderlich sind, sowie die Parameter, die Sie verwenden müssen, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="51cea-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="51cea-112">Nach der erfolgreichen Bereitstellung Ihrer Commerce-Evaluierungsumgebung müssen Sie einige Schritte nach der Bereitstellung ausführen, um Ihre Vorschauumgebung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="51cea-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="51cea-113">Einige Schritte sind optional, je nachdem, welche Aspekte des Systems Sie bewerten möchten.</span><span class="sxs-lookup"><span data-stu-id="51cea-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="51cea-114">Sie können die optionalen Schritte später jederzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="51cea-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="51cea-115">Informationen zum Konfigurieren Ihrer Commerce-Evaluierungsumgebung nach deren Bereitstellung finden Sie unter [Konfigurieren Sie eine Commerce-Evaluierungsumgebung](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="51cea-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="51cea-116">Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Evaluierungsumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Evaluierungsumgebung konfigurieren](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="51cea-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="51cea-117">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="51cea-117">Prerequisites</span></span>

<span data-ttu-id="51cea-118">Die folgenden Voraussetzungen müssen erfüllt sein, damit Sie Ihre Commerce-Evaluierungsumgebung bereitstellen können:</span><span class="sxs-lookup"><span data-stu-id="51cea-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="51cea-119">Sie wurden in das Auswertungsprogramm aufgenommen und Ihnen wurde die Kapazität für eine Auswertungsumgebung gewährt.</span><span class="sxs-lookup"><span data-stu-id="51cea-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="51cea-120">Sie haben Zugriff auf das Microsoft Dynamics Lifecycle Services-Portal (LCS).</span><span class="sxs-lookup"><span data-stu-id="51cea-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="51cea-121">Sie sind ein bestehender Partner oder Kunde von Microsoft Dynamics 365 und können ein Dynamics 365 Commerce-Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="51cea-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="51cea-122">Sie haben Administratorzugriff auf Ihr Microsoft Azure-Abonnement, oder Sie stehen in Kontakt mit einem Abonnementadministrator, der Sie bei Bedarf unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="51cea-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="51cea-123">Ihnen liegt Ihre Azure Active Directory-Mandanten-ID (Azure AD) vor.</span><span class="sxs-lookup"><span data-stu-id="51cea-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="51cea-124">Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als E-Commerce-Systemadministrator-Gruppe verwendet wird, und Ihnen liegt deren ID vor.</span><span class="sxs-lookup"><span data-stu-id="51cea-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="51cea-125">Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als Bewertungs- und Prüfungsmoderatorgruppe verwendet wird, und Ihnen liegt deren ID vor.</span><span class="sxs-lookup"><span data-stu-id="51cea-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="51cea-126">(Diese Sicherheitsgruppe kann mit der Administratorgruppe des E-Commerce-Systems identisch sein.)</span><span class="sxs-lookup"><span data-stu-id="51cea-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="51cea-127">Beachten Sie, dass diese Liste nicht vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="51cea-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="51cea-128">Sollten Probleme auftreten, wenden Sie sich an Ihren Microsoft-Partner, um Unterstützung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="51cea-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="51cea-129">Bereitstellen Ihrer Commerce-Evaluierungsumgebung</span><span class="sxs-lookup"><span data-stu-id="51cea-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="51cea-130">In diesen Verfahren wird erläutert, wie eine Commerce-Evaluierungsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="51cea-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="51cea-131">Nachdem Sie sie erfolgreich abgeschlossen haben, kann die Commerce-Evaluierungsumgebung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="51cea-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="51cea-132">Alle hier beschriebenen Aktivitäten finden im LCS-Portal statt.</span><span class="sxs-lookup"><span data-stu-id="51cea-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="51cea-133">Neues Projekt erstellen</span><span class="sxs-lookup"><span data-stu-id="51cea-133">Create a new project</span></span>

<span data-ttu-id="51cea-134">Gehen Sie folgendermaßen vor, um ein neues Projekt in LCS zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="51cea-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="51cea-135">Wählen Sie auf der LCS-Startseite das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="51cea-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="51cea-136">Führen Sie im rechten Bereich einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="51cea-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="51cea-137">Wenn Sie ein Partner sind, wählen Sie **Migrieren, Erstellen von Lösungen und Kennenlernen von** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="51cea-138">Wenn Sie ein Debitor sind, wählen Sie **Künftige Presales** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="51cea-139">Geben Sie einen Namen, eine Beschreibung und die Branche ein.</span><span class="sxs-lookup"><span data-stu-id="51cea-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="51cea-140">Wählen Sie im Feld **Produktname** die Option **Dynamics 365 Commerce** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="51cea-141">Wählen Sie im Feld **Produktversion** die Option **Dynamics 365 Commerce** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="51cea-142">Wählen Sie im Feld **Methode** **Dynamics Retail-Implementierungsmethode** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="51cea-143">Optional: Sie können Rollen und Benutzer aus einem vorhandenen Projekt importieren.</span><span class="sxs-lookup"><span data-stu-id="51cea-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="51cea-144">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-144">Select **Create**.</span></span> <span data-ttu-id="51cea-145">Die Projektansicht wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51cea-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="51cea-146">Azure-Connector hinzufügen</span><span class="sxs-lookup"><span data-stu-id="51cea-146">Add the Azure Connector</span></span>

<span data-ttu-id="51cea-147">Führen Sie die folgenden Schritte aus, um den Azure Connector zu Ihrem LCS-Projekt hinzuzufügen [Schließen Sie den Onboarding-Prozess für Azure Resource Manager (ARM) ab](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="51cea-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="51cea-148">Bereitstellen der Umgebung</span><span class="sxs-lookup"><span data-stu-id="51cea-148">Deploy the environment</span></span>

<span data-ttu-id="51cea-149">Gehen Sie folgendermaßen vor, um die Umgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="51cea-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="51cea-150">Möglicherweise müssen Sie die Schritte 6, 7 und/oder 8 nicht ausführen, da Seiten mit einer einzelnen Option übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="51cea-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="51cea-151">Wenn Sie sich in der Ansicht **Umgebungsparameter** befinden, bestätigen Sie, dass der Text **Dynamics 365 Commerce – Demo (10.0.* x* mit Plattform-Update *xx*)\*\* direkt über dem Feld **Umgebungsname** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="51cea-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="51cea-152">Weitere Details finden Sie in der Abbildung, die nach Schritt 8 angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="51cea-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="51cea-153">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="51cea-154">Wählen Sie **Hinzufügen** aus, um eine Umgebung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="51cea-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="51cea-155">Wählen Sie im Feld **Anwendungsversion** die aktuellste Version aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="51cea-156">Wenn Sie aus einem bestimmten Grund eine andere Anwendungsversion als die aktuellste auswählen müssen, wählen Sie keine Version vor **10.0.14** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="51cea-157">Verwenden Sie im Feld **Plattformversion** die Plattformversion, die automatisch für die von Ihnen ausgewählte Anwendungsversion ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="51cea-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Auswählen von Anwendungs- und Plattformversionen](./media/project1.png)

1. <span data-ttu-id="51cea-159">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="51cea-159">Select **Next**.</span></span>
1. <span data-ttu-id="51cea-160">Wählen Sie **Demo** als Umgebungstopologie aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-160">Select **Demo** as the environment topology.</span></span>

    ![Auswählen der Umgebungstopologie 1](./media/project2.png)

1. <span data-ttu-id="51cea-162">Geben Sie auf der Seite **Umgebung bereitstellen** einen Umgebungsnamen ein.</span><span class="sxs-lookup"><span data-stu-id="51cea-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="51cea-163">Lassen Sie die erweiterten Einstellungen unverändert.</span><span class="sxs-lookup"><span data-stu-id="51cea-163">Leave the advanced settings as they are.</span></span>

    ![Bereitstellen der Umgebungsseite](./media/project4.png)

1. <span data-ttu-id="51cea-165">Passen Sie die VM-Größe nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="51cea-165">Adjust the VM size as required.</span></span> <span data-ttu-id="51cea-166">(Wir empfehlen die VM-Lagermengeneinheit \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="51cea-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="51cea-167">Überprüfen Sie die Preis- und Lizenzbedingungen und aktivieren Sie das Kontrollkästchen, um anzuzeigen, dass Sie diesen zustimmen.</span><span class="sxs-lookup"><span data-stu-id="51cea-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="51cea-168">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="51cea-168">Select **Next**.</span></span>
1. <span data-ttu-id="51cea-169">Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Bereitstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="51cea-170">Sie werden zur Ansicht **In der Cloud gehostete Umgebungen** weitergeleitet, und Ihre Umgebung sollte in der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="51cea-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="51cea-171">Ihre angeforderte Umgebung wird so angezeigt, dass sie in die Warteschlange gestellt und anschließend bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="51cea-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="51cea-172">Es wird einige Zeit dauern, bis die Arbeitsabläufe in der Umgebung abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="51cea-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="51cea-173">Versuchen Sie es daher nach ungefähr sechs bis neun Stunden erneut.</span><span class="sxs-lookup"><span data-stu-id="51cea-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="51cea-174">Stellen Sie vor dem Fortfahren sicher, dass der Status Ihrer Umgebung **Bereitgestellt** lautet.</span><span class="sxs-lookup"><span data-stu-id="51cea-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="51cea-175">Initialisieren der Commerce Scale Unit (Cloud)</span><span class="sxs-lookup"><span data-stu-id="51cea-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="51cea-176">Führen Sie folgende Schritte aus, um eine CSU zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="51cea-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="51cea-177">Wählen Sie in der Ansicht **In der Cloud gehostete Umgebungen** Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="51cea-178">Wählen Sie in der Umgebungsansicht rechts die Option **Vollständige Details** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="51cea-179">Die Ansicht zu Umgebungsdetails wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51cea-179">The environment details view appears.</span></span>
1. <span data-ttu-id="51cea-180">Wählen Sie unter **Umgebungsfunktionen** die Option **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="51cea-181">Wählen Sie auf der Registerkarte **Commerce** die Option **Initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="51cea-182">Die Ansicht zu CSU-Initialisierungsparametern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51cea-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="51cea-183">Wählen Sie im Feld **Region** die Region aus, die mit der Region identisch ist, in der Sie die Umgebung bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="51cea-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="51cea-184">Lassen Sie das Feld **Version** wie es ist.</span><span class="sxs-lookup"><span data-stu-id="51cea-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="51cea-185">Wählen Sie **Initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="51cea-186">Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="51cea-187">In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **Commerce** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="51cea-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="51cea-188">Ihre CSU wurde für die Bereitstellung in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="51cea-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="51cea-189">Stellen Sie vor dem Fortfahren sicher, dass Ihr CSU-Status **Erfolgreich** lautet.</span><span class="sxs-lookup"><span data-stu-id="51cea-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="51cea-190">Die Initialisierung dauert ungefähr zwei bis fünf Stunden.</span><span class="sxs-lookup"><span data-stu-id="51cea-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="51cea-191">Wenn Sie den Link **Verwalten** in der Ansicht „Umgebungsdetails“ nicht finden können, wenden Sie sich an Ihren Microsoft-Kontakt, um Unterstützung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="51cea-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="51cea-192">E-Commerce initialisieren</span><span class="sxs-lookup"><span data-stu-id="51cea-192">Initialize e-Commerce</span></span>

<span data-ttu-id="51cea-193">Führen Sie folgende Schritte aus, um e-Commerce zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="51cea-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="51cea-194">Prüfen Sie auf der Registerkarte **E-Commerce** die Evaluierungseinwilligung und wählen Sie dann **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="51cea-195">Geben Sie im Feld **E-Commerce-Evaluierungsname** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="51cea-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="51cea-196">Beachten Sie, dass dieser Name in einigen URLs sichtbar ist, die auf Ihre E-Commerce-Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="51cea-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="51cea-197">Wählen Sie im Feld **Commerce Scale Unit Name** Ihre CSU in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="51cea-198">(Die Liste sollte nur eine Option haben.)</span><span class="sxs-lookup"><span data-stu-id="51cea-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="51cea-199">Das Feld **E-Commerce-Geografie** wird automatisch eingestellt.</span><span class="sxs-lookup"><span data-stu-id="51cea-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="51cea-200">Wählen Sie **Weiter** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="51cea-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="51cea-201">Geben Sie im Feld **Unterstützte Hostnamen** eine gültige Domäne, wie `www.fabrikam.com`, ein.</span><span class="sxs-lookup"><span data-stu-id="51cea-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="51cea-202">Geben Sie in das Feld **AAD-Sicherheitsgruppe für Systemadministrator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51cea-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="51cea-203">Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="51cea-204">Geben Sie in das Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51cea-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="51cea-205">Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="51cea-206">Lassen Sie die Option **Bewertungs- und Prüfungsdienst aktivieren** auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51cea-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="51cea-207">Wählen Sie **Initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="51cea-207">Select **Initialize**.</span></span> <span data-ttu-id="51cea-208">In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **E-Commerce** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="51cea-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="51cea-209">Die E-Commerce-Initialisierung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="51cea-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="51cea-210">Warten Sie, bevor Sie fortfahren, bis Ihr E-Commerce-Initialisierungsstatus **Initialisierung erfolgreich** lautet.</span><span class="sxs-lookup"><span data-stu-id="51cea-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="51cea-211">Notieren Sie sich unten rechts im Bereich **Links** die URLs für die folgenden Links:</span><span class="sxs-lookup"><span data-stu-id="51cea-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="51cea-212">**E-Commerce-Website** – Der Link zum Stammverzeichnis Ihrer E-Commerce-Website.</span><span class="sxs-lookup"><span data-stu-id="51cea-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="51cea-213">**Commerce-Site-Builder** – Der Link zum Site-Management-Tool.</span><span class="sxs-lookup"><span data-stu-id="51cea-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="51cea-214">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="51cea-214">Next steps</span></span>

<span data-ttu-id="51cea-215">Um den Prozess zum Bereitstellen und Konfigurieren Ihrer Commerce-Evaluierungsumgebung fortzusetzen, schauen Sie sich [Konfigurieren Sie eine Commerce-Evaluierungsumgebung](cpe-post-provisioning.md) an.</span><span class="sxs-lookup"><span data-stu-id="51cea-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51cea-216">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51cea-216">Additional resources</span></span>

[<span data-ttu-id="51cea-217">Dynamics 365 Commerce-Evaluierungsumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="51cea-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="51cea-218">Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="51cea-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="51cea-219">BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="51cea-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="51cea-220">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="51cea-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="51cea-221">Dynamics 365 Commerce-Evaluierungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="51cea-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="51cea-222">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="51cea-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="51cea-223">Commerce Scale Unit (Cloud)</span><span class="sxs-lookup"><span data-stu-id="51cea-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="51cea-224">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="51cea-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="51cea-225">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="51cea-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
