---
title: Sammlung von Webaktivitätsereignissen kündigen
description: In diesem Thema wird erläutert, wie Sie Besuchern Ihrer Website erlauben können, die Sammlung von Webaktivitätsereignissen in Microsoft Dynamics 365 Commerce zu kündigen.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791556"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="4078b-103">Erfassung von Webaktivitätsereignissen deaktivieren</span><span class="sxs-lookup"><span data-stu-id="4078b-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="4078b-104">In diesem Thema wird erläutert, wie Sie Kunden erlauben können, die Sammlung von Webaktivitätsereignissen in Microsoft Dynamics 365 Commerce zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="4078b-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4078b-105">Dynamics 365 Commerce ermöglicht den Websiteadministratoren die Analyse der Webaktivität der Benutzer ihrer E-Commerce-Sites.</span><span class="sxs-lookup"><span data-stu-id="4078b-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="4078b-106">Auf diese Weise können sie besser verstehen, wie ihre Websites verwendet werden, und die Websites optimieren, um eine verbesserte Benutzererfahrung zu erzielen und Geschäftsziele zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="4078b-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="4078b-107">Möglichkeiten für Administratoren, ein Abmeldungs-Erlebnis zu implementieren</span><span class="sxs-lookup"><span data-stu-id="4078b-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="4078b-108">Administratoren haben drei Möglichkeiten, ein Abmeldungs-Erlebnis zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="4078b-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="4078b-109">Kündigen im Namen der Benutzer</span><span class="sxs-lookup"><span data-stu-id="4078b-109">Opt out on behalf of users</span></span>

<span data-ttu-id="4078b-110">In der Kontoverwaltung in der Commerce-Zentrale können sich Administrator für Benutzer abmelden.</span><span class="sxs-lookup"><span data-stu-id="4078b-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="4078b-111">Im HQ-Client auf der Seite **Alle Kunden** suchen und wählen Sie einen Kunden aus.</span><span class="sxs-lookup"><span data-stu-id="4078b-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="4078b-112">Auf der Kundendetailseite im Inforegister **Einzelhandel**, im Abschnitt **Privatsphäre** stellen Sie die Option **Webaktivität nicht verfolgen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4078b-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Datenschutzeinstellungen](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="4078b-114">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4078b-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="4078b-115">Erfahrung mit modulbasierter Abmeldungs-Erfahrung</span><span class="sxs-lookup"><span data-stu-id="4078b-115">Module-based opt-out experience</span></span>

<span data-ttu-id="4078b-116">Administratoren können authentifizierte Benutzer die Erfassung von Webaktivitätsereignissen selbst deaktivieren lassen.</span><span class="sxs-lookup"><span data-stu-id="4078b-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="4078b-117">Fügen Sie das Benutzer-Deaktivierungsmodul zu den Profilseiten des Kundenkontos hinzu, um diese Deaktivierungsfunktion zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="4078b-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="4078b-118">Benutzerdefinierte Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="4078b-118">Custom extensions</span></span>

<span data-ttu-id="4078b-119">Administratoren können ihre eigenen Erweiterungen erstellen, um das Abmelde-Erlebnis für Benutzer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="4078b-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="4078b-120">Weitere Informationen finden Sie unter [Rufen Sie die Retail Server APIs auf](e-commerce-extensibility/call-retail-server-apis.md) und [Online-Kanal-Erweiterbarkeit](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="4078b-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
