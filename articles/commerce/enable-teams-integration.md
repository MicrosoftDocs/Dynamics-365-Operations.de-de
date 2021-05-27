---
title: Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren
description: In diesem Thema wird beschrieben, wie die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams aktiviert wird.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019834"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="ea60c-103">Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren</span><span class="sxs-lookup"><span data-stu-id="ea60c-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea60c-104">In diesem Thema wird beschrieben, wie die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ea60c-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="ea60c-105">Um Teams mit Informationen aus Dynamics 365 Commerce zu versorgen und die Funktionen der Aufgabenverwaltung zwischen Teams und der Point-of-Sale-Anwendung (POS-Anwendung) zu synchronisieren, müssen Sie die Integrationsfunktionen in der Commerce-Zentralverwaltung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="ea60c-106">Wenn Sie die Teams-Integration aktivieren, stimmen Sie zu, Ihre Daten für Teams freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ea60c-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="ea60c-107">Daten, die mit Teams geteilt werden, befinden sich möglicherweise in einem anderen Land als Ihre Commerce-Daten und unterliegen möglicherweise anderen Compliance-Standards.</span><span class="sxs-lookup"><span data-stu-id="ea60c-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="ea60c-108">Weitere Informationen dazu, finden Sie unter [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="ea60c-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="ea60c-109">Informationen zu den Microsoft-Datenschutzrichtlinien finden Sie in den [Microsoft-Datenschutzbestimmungen](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="ea60c-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="ea60c-110">Teams-Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="ea60c-110">Enable Teams integration</span></span>

<span data-ttu-id="ea60c-111">Bevor Sie die Microsoft Teams-Integration in Commerce aktivieren können, müssen Sie die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal registrieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="ea60c-112">Führen Sie die folgenden Schritte aus, um die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="ea60c-113">Befolgen Sie die Schritte in [Schnellstart: Registrieren einer Anwendung bei Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app), um die Teams-Anwendung mit Ihrem Mandanten im Azure-Portal zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="ea60c-114">Kopieren Sie den Wert **Anwendungs-ID (Client-ID)** aus der Seite **Überblick** der registrierten App.</span><span class="sxs-lookup"><span data-stu-id="ea60c-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="ea60c-115">Sie werden diesen Wert verwenden, um die Teams-Integration in der Commerce-Zentralverwaltung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="ea60c-116">Kopieren Sie den Zertifikatswert, der beim [Hinzufügen eines Zertifikats](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in Schritt 1 eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ea60c-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="ea60c-117">Das Zertifikat wird auch als öffentlicher Schlüssel oder Anwendungsschlüssel bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ea60c-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="ea60c-118">Sie werden diesen Wert verwenden, um die Teams-Integration in der Commerce-Zentralverwaltung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="ea60c-119">Führen Sie die folgenden Schritte aus, um die Teams-Integration in der Commerce-Zentralverwaltung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ea60c-120">Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ea60c-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="ea60c-121">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ea60c-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ea60c-122">Legen Sie die Option **Microsoft Teams-Integration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ea60c-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="ea60c-123">Geben Sie in den Feldern **Anwendungs-ID** und **Anwendungsschlüssel** die Werte ein, die Sie erhalten haben, als Sie die Teams-Anwendung im Azure-Portal registriert haben.</span><span class="sxs-lookup"><span data-stu-id="ea60c-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="ea60c-124">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ea60c-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="ea60c-125">Die folgende Abbildung zeigt ein Beispiel für die Konfiguration der Teams-Integration in der Commerce-Zentralverwaltung.</span><span class="sxs-lookup"><span data-stu-id="ea60c-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Konfiguration der Teams-Integration in der Commerce-Zentralverwaltung](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="ea60c-127">Teams-Integration deaktivieren</span><span class="sxs-lookup"><span data-stu-id="ea60c-127">Disable Teams integration</span></span>

<span data-ttu-id="ea60c-128">Führen Sie die folgenden Schritte aus, um die Microsoft Teams-Integration in der Commerce-Zentralverwaltung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea60c-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ea60c-129">Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ea60c-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="ea60c-130">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ea60c-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="ea60c-131">Legen Sie die Option **Microsoft Teams-Integration aktivieren** auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="ea60c-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="ea60c-132">Löschen Sie die Werte aus den Feldern **Anwendungs-ID** und **Anwendungsschlüssel**.</span><span class="sxs-lookup"><span data-stu-id="ea60c-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="ea60c-133">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ea60c-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ea60c-134">Nachdem Sie die Teams-Integration in Commerce deaktiviert haben, werden auf den POS-Terminals keine Aufgaben mehr angezeigt, die in der Teams-Anwendung veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="ea60c-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea60c-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ea60c-135">Additional resources</span></span>

[<span data-ttu-id="ea60c-136">Überblick Integration Dynamics 365 Commerce und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ea60c-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ea60c-137">Microsoft Teams aus Dynamics 365 Commerce bereitstellen</span><span class="sxs-lookup"><span data-stu-id="ea60c-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ea60c-138">Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ea60c-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ea60c-139">Benutzerrollen in Microsoft Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="ea60c-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ea60c-140">Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="ea60c-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="ea60c-141">Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ</span><span class="sxs-lookup"><span data-stu-id="ea60c-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)