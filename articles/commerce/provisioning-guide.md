---
title: Eine Dynamics 365 Commerce-Evaluierungsumgebung bereitstellen
description: In diesem Thema wird erläutert, wie eine Evaluierungsumgebung in Microsoft Dynamics 365 Commerce bereitgestellt wird.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a57cc02c6d62f288f14b65191c2f4927a019963c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478163"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="9d640-103">Eine Dynamics 365 Commerce-Evaluierungsumgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="9d640-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d640-104">In diesem Thema wird erläutert, wie eine Evaluierungsumgebung in Microsoft Dynamics 365 Commerce bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9d640-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="9d640-105">Bevor Sie beginnen, empfehlen wir, dass Sie einen kurzen Blick in dieses Thema werfen, um eine Vorstellung davon zu bekommen, was der Prozess erfordert.</span><span class="sxs-lookup"><span data-stu-id="9d640-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="9d640-106">Commerce-Auswertungsumgebungen sind nicht allgemein verfügbar und sie werden Partner und Kunden auf Anfrage gewährt.</span><span class="sxs-lookup"><span data-stu-id="9d640-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="9d640-107">Für weitere Informationen wenden Sie sich an den Ansprechpartner Ihres Microsoft-Partners.</span><span class="sxs-lookup"><span data-stu-id="9d640-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="9d640-108">Um eine Commerce-Evaluierungsumgebung erfolgreich bereitzustellen, müssen Sie ein Projekt mit einem bestimmten Produktnamen und -Typ erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d640-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="9d640-109">Bei der Umgebung und der Commerce Scale Unit (CSU) gibt es auch einige spezifische Parameter, die Sie verwenden müssen, um später E-Commerce bereitstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="9d640-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="9d640-110">In den Anweisungen in diesem Thema werden alle Schritte, die zum Ausführen der Bereitstellung erforderlich sind, sowie die Parameter, die Sie verwenden müssen, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d640-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="9d640-111">Nach der erfolgreichen Bereitstellung Ihrer Commerce-Evaluierungsumgebung müssen Sie einige Schritte nach der Bereitstellung ausführen, um Ihre Vorschauumgebung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="9d640-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="9d640-112">Einige Schritte sind optional, je nachdem, welche Aspekte des Systems Sie bewerten möchten.</span><span class="sxs-lookup"><span data-stu-id="9d640-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="9d640-113">Sie können die optionalen Schritte später jederzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d640-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="9d640-114">Informationen zum Konfigurieren Ihrer Commerce-Evaluierungsumgebung nach deren Bereitstellung finden Sie unter [Konfigurieren Sie eine Commerce-Evaluierungsumgebung](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="9d640-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="9d640-115">Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Evaluierungsumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Evaluierungsumgebung konfigurieren](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="9d640-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9d640-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9d640-116">Prerequisites</span></span>

<span data-ttu-id="9d640-117">Die folgenden Voraussetzungen müssen erfüllt sein, damit Sie Ihre Commerce-Evaluierungsumgebung bereitstellen können:</span><span class="sxs-lookup"><span data-stu-id="9d640-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="9d640-118">Sie wurden in das Auswertungsprogramm aufgenommen und Ihnen wurde die Kapazität für eine Auswertungsumgebung gewährt.</span><span class="sxs-lookup"><span data-stu-id="9d640-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="9d640-119">Sie haben Zugriff auf das Microsoft Dynamics Lifecycle Services-Portal (LCS).</span><span class="sxs-lookup"><span data-stu-id="9d640-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="9d640-120">Sie sind ein bestehender Partner oder Kunde von Microsoft Dynamics 365 und können ein Dynamics 365 Commerce-Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d640-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="9d640-121">Sie haben Administratorzugriff auf Ihr Microsoft Azure-Abonnement, oder Sie stehen in Kontakt mit einem Abonnementadministrator, der Sie bei Bedarf unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="9d640-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="9d640-122">Ihnen liegt Ihre Azure Active Directory-Mandanten-ID (Azure AD) vor.</span><span class="sxs-lookup"><span data-stu-id="9d640-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="9d640-123">Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als E-Commerce-Systemadministrator-Gruppe verwendet wird, und Ihnen liegt deren ID vor.</span><span class="sxs-lookup"><span data-stu-id="9d640-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="9d640-124">Sie haben eine Azure AD-Sicherheitsgruppe erstellt, die als Bewertungs- und Prüfungsmoderatorgruppe verwendet wird, und Ihnen liegt deren ID vor.</span><span class="sxs-lookup"><span data-stu-id="9d640-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="9d640-125">(Diese Sicherheitsgruppe kann mit der Administratorgruppe des E-Commerce-Systems identisch sein.)</span><span class="sxs-lookup"><span data-stu-id="9d640-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="9d640-126">Beachten Sie, dass diese Liste nicht vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="9d640-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="9d640-127">Sollten Probleme auftreten, wenden Sie sich an Ihren Microsoft-Partner, um Unterstützung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d640-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="9d640-128">Bereitstellen Ihrer Commerce-Evaluierungsumgebung</span><span class="sxs-lookup"><span data-stu-id="9d640-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="9d640-129">In diesen Verfahren wird erläutert, wie eine Commerce-Evaluierungsumgebung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9d640-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="9d640-130">Nachdem Sie sie erfolgreich abgeschlossen haben, kann die Commerce-Evaluierungsumgebung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9d640-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="9d640-131">Alle hier beschriebenen Aktivitäten finden im LCS-Portal statt.</span><span class="sxs-lookup"><span data-stu-id="9d640-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="9d640-132">Neues Projekt erstellen</span><span class="sxs-lookup"><span data-stu-id="9d640-132">Create a new project</span></span>

<span data-ttu-id="9d640-133">Gehen Sie folgendermaßen vor, um ein neues Projekt in LCS zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d640-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="9d640-134">Wählen Sie auf der LCS-Startseite das Pluszeichen (**+**) aus, um ein Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d640-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="9d640-135">Führen Sie im rechten Bereich einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="9d640-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="9d640-136">Wenn Sie ein Partner sind, wählen Sie **Migrieren, Erstellen von Lösungen und Kennenlernen von** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="9d640-137">Wenn Sie ein Debitor sind, wählen Sie **Künftige Presales** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="9d640-138">Geben Sie einen Namen, eine Beschreibung und die Branche ein.</span><span class="sxs-lookup"><span data-stu-id="9d640-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="9d640-139">Wählen Sie im Feld **Produktname** die Option **Dynamics 365 Commerce** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="9d640-140">Wählen Sie im Feld **Produktversion** die Option **Dynamics 365 Commerce** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="9d640-141">Wählen Sie im Feld **Methode** **Dynamics Retail-Implementierungsmethode** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="9d640-142">Optional: Sie können Rollen und Benutzer aus einem vorhandenen Projekt importieren.</span><span class="sxs-lookup"><span data-stu-id="9d640-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="9d640-143">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-143">Select **Create**.</span></span> <span data-ttu-id="9d640-144">Die Projektansicht wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d640-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="9d640-145">Azure-Connector hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9d640-145">Add the Azure Connector</span></span>

<span data-ttu-id="9d640-146">Führen Sie die folgenden Schritte aus, um den Azure Connector zu Ihrem LCS-Projekt hinzuzufügen [Schließen Sie den Onboarding-Prozess für Azure Resource Manager (ARM) ab](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="9d640-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="9d640-147">Bereitstellen der Umgebung</span><span class="sxs-lookup"><span data-stu-id="9d640-147">Deploy the environment</span></span>

<span data-ttu-id="9d640-148">Gehen Sie folgendermaßen vor, um die Umgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d640-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="9d640-149">Möglicherweise müssen Sie die Schritte 6, 7 und/oder 8 nicht ausführen, da Seiten mit einer einzelnen Option übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="9d640-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="9d640-150">Wenn Sie sich in der Ansicht **Umgebungsparameter** befinden, bestätigen Sie, dass der Text **Dynamics 365 Commerce – Demo (10.0.* x* mit Plattform-Update *xx*)\*\* direkt über dem Feld **Umgebungsname** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9d640-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="9d640-151">Weitere Details finden Sie in der Abbildung, die nach Schritt 8 angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9d640-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="9d640-152">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="9d640-153">Wählen Sie **Hinzufügen** aus, um eine Umgebung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9d640-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="9d640-154">Wählen Sie im Feld **Anwendungsversion** die aktuellste Version aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="9d640-155">Wenn Sie aus einem bestimmten Grund eine andere Anwendungsversion als die aktuellste auswählen müssen, wählen Sie keine Version vor **10.0.14** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="9d640-156">Verwenden Sie im Feld **Plattformversion** die Plattformversion, die automatisch für die von Ihnen ausgewählte Anwendungsversion ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="9d640-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Auswählen von Anwendungs- und Plattformversionen](./media/project1.png)

1. <span data-ttu-id="9d640-158">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9d640-158">Select **Next**.</span></span>
1. <span data-ttu-id="9d640-159">Wählen Sie **Demo** als Umgebungstopologie aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-159">Select **Demo** as the environment topology.</span></span>

    ![Auswählen der Umgebungstopologie 1](./media/project2.png)

1. <span data-ttu-id="9d640-161">Geben Sie auf der Seite **Umgebung bereitstellen** einen Umgebungsnamen ein.</span><span class="sxs-lookup"><span data-stu-id="9d640-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="9d640-162">Lassen Sie die erweiterten Einstellungen unverändert.</span><span class="sxs-lookup"><span data-stu-id="9d640-162">Leave the advanced settings as they are.</span></span>

    ![Bereitstellen der Umgebungsseite](./media/project4.png)

1. <span data-ttu-id="9d640-164">Passen Sie die VM-Größe nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="9d640-164">Adjust the VM size as required.</span></span> <span data-ttu-id="9d640-165">(Wir empfehlen die VM-Lagermengeneinheit \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="9d640-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="9d640-166">Überprüfen Sie die Preis- und Lizenzbedingungen und aktivieren Sie das Kontrollkästchen, um anzuzeigen, dass Sie diesen zustimmen.</span><span class="sxs-lookup"><span data-stu-id="9d640-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="9d640-167">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="9d640-167">Select **Next**.</span></span>
1. <span data-ttu-id="9d640-168">Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Bereitstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="9d640-169">Sie werden zur Ansicht **In der Cloud gehostete Umgebungen** weitergeleitet, und Ihre Umgebung sollte in der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9d640-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="9d640-170">Ihre angeforderte Umgebung wird so angezeigt, dass sie in die Warteschlange gestellt und anschließend bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9d640-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="9d640-171">Es wird einige Zeit dauern, bis die Arbeitsabläufe in der Umgebung abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="9d640-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="9d640-172">Versuchen Sie es daher nach ungefähr sechs bis neun Stunden erneut.</span><span class="sxs-lookup"><span data-stu-id="9d640-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="9d640-173">Stellen Sie vor dem Fortfahren sicher, dass der Status Ihrer Umgebung **Bereitgestellt** lautet.</span><span class="sxs-lookup"><span data-stu-id="9d640-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="9d640-174">Initialisieren der Commerce Scale Unit (Cloud)</span><span class="sxs-lookup"><span data-stu-id="9d640-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="9d640-175">Führen Sie folgende Schritte aus, um die CSU zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="9d640-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="9d640-176">Wählen Sie in der Ansicht **In der Cloud gehostete Umgebungen** Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="9d640-177">Wählen Sie in der Umgebungsansicht rechts die Option **Vollständige Details** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="9d640-178">Die Ansicht zu Umgebungsdetails wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d640-178">The environment details view appears.</span></span>
1. <span data-ttu-id="9d640-179">Wählen Sie unter **Umgebungsfunktionen** die Option **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="9d640-180">Wählen Sie auf der Registerkarte **Commerce** die Option **Initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="9d640-181">Die Ansicht zu CSU-Initialisierungsparametern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d640-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="9d640-182">Wählen Sie im Feld **Region** die Region aus, die mit der Region identisch ist, in der Sie die Umgebung bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="9d640-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="9d640-183">Lassen Sie das Feld **Version** wie es ist.</span><span class="sxs-lookup"><span data-stu-id="9d640-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="9d640-184">Wählen Sie **Initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="9d640-185">Prüfen Sie auf der Bestätigungsseite für die Bereitstellung, ob die Details korrekt sind, und wählen Sie dann **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="9d640-186">In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **Commerce** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="9d640-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="9d640-187">Ihre CSU wurde für die Bereitstellung in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="9d640-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="9d640-188">Stellen Sie vor dem Fortfahren sicher, dass Ihr CSU-Status **Erfolgreich** lautet.</span><span class="sxs-lookup"><span data-stu-id="9d640-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="9d640-189">Die Initialisierung dauert ungefähr zwei bis fünf Stunden.</span><span class="sxs-lookup"><span data-stu-id="9d640-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="9d640-190">Wenn Sie den Link **Verwalten** in der Ansicht „Umgebungsdetails“ nicht finden können, wenden Sie sich an Ihren Microsoft-Kontakt, um Unterstützung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d640-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="9d640-191">Während des Bereitstellungsprozesses wird möglicherweise die folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="9d640-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="9d640-192">Auswertungsumgebungen (Demo/Test) müssen die Anwendung \<application ID\> für den Konnektor der Skalierungseinheit in der Zentralverwaltung registrieren.</span><span class="sxs-lookup"><span data-stu-id="9d640-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="9d640-193">Wenn die CSU-Initialisierung fehlschlägt und Sie diese Fehlermeldung erhalten, notieren Sie sich die Anwendungs-ID, bei der es sich um einen global eindeutigen Bezeichner (GUID) handelt, und befolgen Sie die Schritte im nächsten Abschnitt, um die CSU-Bereitstellungsanwendung in der Commerce-Zentralverwaltung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="9d640-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="9d640-194">Registrieren Sie die CSU-Bereitstellungsanwendung in der Commerce-Zentrale (falls erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d640-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="9d640-195">Führen Sie folgende Schritte aus, um die CSU-Bereitstellungsanwendung in der Commerce-Zentralverwaltung zu registrieren (falls erforderlich).</span><span class="sxs-lookup"><span data-stu-id="9d640-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9d640-196">Wechseln Sie in Commerce-Zentralverwaltung zu **Systemverwaltung \> Einrichtung \> Azure Active Directory-Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="9d640-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="9d640-197">Geben Sie in der Spalte **Kunden-ID** die Anwendungs-ID aus der CSU-Initialisierungsfehlermeldung ein, die Sie erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="9d640-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="9d640-198">Geben Sie in der Spalte **Name** einen beliebigen beschreibenden Text ein (z. B. **CSU Eval**).</span><span class="sxs-lookup"><span data-stu-id="9d640-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="9d640-199">Geben Sie in der Spalte **Benutzer-UD** **RetailServiceAccount** ein.</span><span class="sxs-lookup"><span data-stu-id="9d640-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="9d640-200">Wiederholen Sie die CSU-Initialisierung und -Bereitstellung über LCS.</span><span class="sxs-lookup"><span data-stu-id="9d640-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="9d640-201">E-Commerce initialisieren</span><span class="sxs-lookup"><span data-stu-id="9d640-201">Initialize e-Commerce</span></span>

<span data-ttu-id="9d640-202">Führen Sie folgende Schritte aus, um e-Commerce zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="9d640-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9d640-203">Prüfen Sie auf der Registerkarte **E-Commerce** die Evaluierungseinwilligung und wählen Sie dann **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="9d640-204">Geben Sie im Feld **E-Commerce-Evaluierungsname** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="9d640-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="9d640-205">Beachten Sie, dass dieser Name in einigen URLs sichtbar ist, die auf Ihre E-Commerce-Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="9d640-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="9d640-206">Wählen Sie im Feld **Commerce Scale Unit Name** Ihre CSU in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="9d640-207">(Die Liste sollte nur eine Option haben.)</span><span class="sxs-lookup"><span data-stu-id="9d640-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="9d640-208">Das Feld **E-Commerce-Geografie** wird automatisch eingestellt.</span><span class="sxs-lookup"><span data-stu-id="9d640-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="9d640-209">Wählen Sie **Weiter** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="9d640-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="9d640-210">Geben Sie im Feld **Unterstützte Hostnamen** eine gültige Domäne, wie `www.fabrikam.com`, ein.</span><span class="sxs-lookup"><span data-stu-id="9d640-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="9d640-211">Geben Sie in das Feld **AAD-Sicherheitsgruppe für Systemadministrator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9d640-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="9d640-212">Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="9d640-213">Geben Sie in das Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ersten Buchstaben des Namens der Sicherheitsgruppe ein, die Sie verwenden möchten, und wählen Sie dann das Lupensymbol aus, um die Suchergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9d640-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="9d640-214">Wählen Sie die richtige Sicherheitsgruppe in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="9d640-215">Lassen Sie die Option **Bewertungs- und Prüfungsdienst aktivieren** auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9d640-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="9d640-216">Wählen Sie **Initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9d640-216">Select **Initialize**.</span></span> <span data-ttu-id="9d640-217">In der Ansicht **Commerce-Verwaltung** wird erneut angezeigt, wo die Registerkarte **E-Commerce** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="9d640-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="9d640-218">Die E-Commerce-Initialisierung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="9d640-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="9d640-219">Warten Sie, bevor Sie fortfahren, bis Ihr E-Commerce-Initialisierungsstatus **Initialisierung erfolgreich** lautet.</span><span class="sxs-lookup"><span data-stu-id="9d640-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="9d640-220">Notieren Sie sich unten rechts im Bereich **Links** die URLs für die folgenden Links:</span><span class="sxs-lookup"><span data-stu-id="9d640-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="9d640-221">**E-Commerce-Website** – Der Link zum Stammverzeichnis Ihrer E-Commerce-Website.</span><span class="sxs-lookup"><span data-stu-id="9d640-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="9d640-222">**Commerce-Site-Builder** – Der Link zum Site-Management-Tool.</span><span class="sxs-lookup"><span data-stu-id="9d640-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9d640-223">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9d640-223">Next steps</span></span>

<span data-ttu-id="9d640-224">Um den Prozess zum Bereitstellen und Konfigurieren Ihrer Commerce-Evaluierungsumgebung fortzusetzen, schauen Sie sich [Konfigurieren Sie eine Commerce-Evaluierungsumgebung](cpe-post-provisioning.md) an.</span><span class="sxs-lookup"><span data-stu-id="9d640-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d640-225">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9d640-225">Additional resources</span></span>

[<span data-ttu-id="9d640-226">Dynamics 365 Commerce-Evaluierungsumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="9d640-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="9d640-227">Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="9d640-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="9d640-228">BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9d640-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="9d640-229">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9d640-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9d640-230">Dynamics 365 Commerce-Evaluierungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="9d640-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="9d640-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="9d640-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="9d640-232">Commerce Scale Unit (Cloud)</span><span class="sxs-lookup"><span data-stu-id="9d640-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="9d640-233">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="9d640-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="9d640-234">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="9d640-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
