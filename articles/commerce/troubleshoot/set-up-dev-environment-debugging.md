---
title: Eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine einrichten
description: Dieses Thema erläutert, wie eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine (VM) eingerichtet wird.
author: Reza-Assadi
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
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801482"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="40dec-103">Eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine einrichten</span><span class="sxs-lookup"><span data-stu-id="40dec-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40dec-104">Dieses Thema erläutert, wie eine E-Commerce-Entwicklungsumgebung für das Debuggen auf einer virtuellen Ebene 1 einer Retail Server-Maschine (VM) eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="40dec-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="40dec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40dec-105">Description</span></span>

<span data-ttu-id="40dec-106">Microsoft Dynamics 365 Commerce-Ebene 1-Umgebungen werden normalerweise für Commerce Runtime (CRT) und die Entwicklung von Verkaufsstellen (POS)-Erweiterungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="40dec-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="40dec-107">Sie sind eigenständige Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="40dec-107">They are standalone environments.</span></span> <span data-ttu-id="40dec-108">Aufgrund der SaaS-Natur (Software-as-a-Service) der Architektur enthalten sie keine E-Commerce-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="40dec-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="40dec-109">In einigen Szenarien möchten Sie möglicherweise Aufrufe von Erweiterungen in einer Ebene 1-Umgebung testen, damit Sie Erweiterungen von E-Commerce-Komponenten debuggen können.</span><span class="sxs-lookup"><span data-stu-id="40dec-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="40dec-110">Allgemeine Anweisungen finden Sie unter [In einer Commerce-Entwicklungsumgebung der Ebene 1 debuggen](../e-commerce-extensibility/debug-tier-1.md)</span><span class="sxs-lookup"><span data-stu-id="40dec-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="40dec-111">Wenn Sie in einer Ebene 1-Umgebung debuggen, da die Website jetzt einen anderen Retail Server aufruft, können serverübergreifende Aufrufe verschiedene Fehler verursachen, die mit der Inhaltssicherheitsrichtlinie zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="40dec-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="40dec-112">Die folgende Abbildung zeigt ein Beispiel für einen Fehler, der auftreten kann, wenn eine Variante auf einer Produktdetailseite ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="40dec-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Fehler beim Auswählen einer Variante auf einer Produktdetailseite](media/unhandled-rejection-error.jpg)

<span data-ttu-id="40dec-114">Die folgende Abbildung zeigt ein Beispiel für einen ähnlichen Fehler in den Debugger-Tools eines Browsers (F12-Entwicklertools).</span><span class="sxs-lookup"><span data-stu-id="40dec-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="40dec-115">In der Fehlermeldung wird ein Verstoß gegen die Inhaltssicherheitsrichtlinie erwähnt.</span><span class="sxs-lookup"><span data-stu-id="40dec-115">The error message mentions violation of the content security policy directive.</span></span>

![Debugger-Tool-Fehler](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="40dec-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="40dec-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="40dec-118">Inhaltssicherheitsrichtlinie für die Website im Commerce-Website-Generator deaktivieren</span><span class="sxs-lookup"><span data-stu-id="40dec-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="40dec-119">Wählen Sie die Website aus, an der Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="40dec-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="40dec-120">Wählen Sie **Einstellungen** und anschließend **Erweiterungen** aus.</span><span class="sxs-lookup"><span data-stu-id="40dec-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="40dec-121">Wählen Sie auf der Registerkarte **Inhaltssicherheitsrichtlinie** die Option **Inhaltssicherheitsrichtlinie deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="40dec-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="40dec-122">Wählen Sie **Speichern und veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="40dec-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="40dec-123">Die Business-to-Consumer(B2C)-Anmeldung funktioniert in einer lokalen Entwicklungsumgebung nicht.</span><span class="sxs-lookup"><span data-stu-id="40dec-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="40dec-124">Sie können jedoch als Gast auschecken oder Pseudoseiten erstellen, um eine Benutzeranmeldung nach Bedarf zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="40dec-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40dec-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40dec-125">Additional resources</span></span>

[<span data-ttu-id="40dec-126">Erste Schritte mit der Entwicklung der E-Commerce-Online-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="40dec-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="40dec-127">Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) auf E-Commerce-Website verwalten</span><span class="sxs-lookup"><span data-stu-id="40dec-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
