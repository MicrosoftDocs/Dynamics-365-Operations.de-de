---
title: Während der ersten Bereitstellung kann keine Sicherheitsgruppe für den Commerce-Website-Generator konfiguriert werden
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Microsoft Azure Active Directory (Azure AD)-Sicherheitsgruppe für den Commerce-Website-Generator beim Erstellen von E-Commerce-Komponenten in Microsoft Dynamics Lifecycle Services (LCS) nicht während der ersten Bereitstellung eines neuen E-Commerce-Mandanten als Option angezeigt werden.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585342"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="684cf-103">Während der ersten Bereitstellung kann keine Sicherheitsgruppe für den Commerce-Website-Generator konfiguriert werden</span><span class="sxs-lookup"><span data-stu-id="684cf-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="684cf-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn die Microsoft Azure Active Directory (Azure AD)-Sicherheitsgruppe für den Commerce-Website-Generator beim Erstellen von E-Commerce-Komponenten in Microsoft Dynamics Lifecycle Services (LCS) nicht während der ersten Bereitstellung eines neuen E-Commerce-Mandanten als Option angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="684cf-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="684cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="684cf-105">Description</span></span>

<span data-ttu-id="684cf-106">Wenn Sie die E-Commerce-Komponenten im Rahmen der Bereitstellung eines neuen E-Commerce-Mandanten erstellen, der die Commerce-Website-Generator-Komponente enthält, wird die Azure AD-Sicherheitsgruppe im Dialogfeld nicht als Option angezeigt.</span><span class="sxs-lookup"><span data-stu-id="684cf-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="684cf-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="684cf-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="684cf-108">Der E-Commerce-Website einen Benutzer im richtigen Mandanten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="684cf-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="684cf-109">Gehen Sie zu [Azure-Portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="684cf-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="684cf-110">Befolgen Sie in dem Mandanten, für den das LCS-Projekt Ihrer E-Commerce-Website bereitgestellt wurde, die Anweisungen in [Erstellen einer Basisgruppe und Hinzufügen von Mitglieder mit Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="684cf-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="684cf-111">Rufen Sie [LCS](https://lcs.dynamics.com/) auf, und melden Sie sich mit einem Konto an, das über denselben Mandanten wie die Azure AD-Sicherheitsgruppe verfügt, die Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="684cf-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="684cf-112">Das Konto muss Zugriff haben, um die Azure AD-Sicherheitsgruppe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="684cf-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="684cf-113">Führen Sie die Einrichtungsschritte aus, um die E-Commerce-Website zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="684cf-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="684cf-114">Wenn Sie die E-Commerce-Komponenten bereitstellen, sollte die Sicherheitsgruppe jetzt als Option im Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="684cf-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="684cf-115">Um sicherzustellen, dass das Feld im Dialogfeld mit der Liste der Sicherheitsgruppen ausgefüllt ist, müssen Sie **Eingeben** auswählen, sobald Sie den Namen der erstellten Azure AD-Sicherheitsgruppe eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="684cf-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="684cf-116">In den Suchergebnissen werden alle Azure AD-Sicherheitsgruppen aufgelistet, die mit dem Suchtext beginnen und auf die der Benutzer Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="684cf-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="684cf-117">Sie können einen kürzeren Suchbegriff verwenden, um breitere Suchergebnisse zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="684cf-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="684cf-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="684cf-118">Additional resources</span></span>

[<span data-ttu-id="684cf-119">Erstellen einer Basisgruppe und Hinzufügen von Mitgliedern mit Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="684cf-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="684cf-120">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="684cf-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
