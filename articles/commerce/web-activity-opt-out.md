---
title: Sammlung von Webaktivitätsereignissen kündigen
description: In diesem Thema wird erläutert, wie Sie Besuchern Ihrer Website erlauben können, die Sammlung von Webaktivitätsereignissen in Microsoft Dynamics 365 Commerce zu kündigen.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 244d612fa01529df4fff250df50a06526632fcf1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210922"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="521ce-103">Erfassung von Webaktivitätsereignissen deaktivieren</span><span class="sxs-lookup"><span data-stu-id="521ce-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="521ce-104">In diesem Thema wird erläutert, wie Sie Kunden erlauben können, die Sammlung von Webaktivitätsereignissen in Microsoft Dynamics 365 Commerce zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="521ce-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="521ce-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="521ce-105">Overview</span></span>

<span data-ttu-id="521ce-106">Dynamics 365 Commerce ermöglicht den Websiteadministratoren die Analyse der Webaktivität der Benutzer ihrer E-Commerce-Sites.</span><span class="sxs-lookup"><span data-stu-id="521ce-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="521ce-107">Auf diese Weise können sie besser verstehen, wie ihre Websites verwendet werden, und die Websites optimieren, um eine verbesserte Benutzererfahrung zu erzielen und Geschäftsziele zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="521ce-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="521ce-108">Möglichkeiten für Administratoren, ein Abmeldungs-Erlebnis zu implementieren</span><span class="sxs-lookup"><span data-stu-id="521ce-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="521ce-109">Administratoren haben drei Möglichkeiten, ein Abmeldungs-Erlebnis zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="521ce-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="521ce-110">Kündigen im Namen der Benutzer</span><span class="sxs-lookup"><span data-stu-id="521ce-110">Opt out on behalf of users</span></span>

<span data-ttu-id="521ce-111">In der Kontoverwaltung in der Commerce-Zentrale können sich Administrator für Benutzer abmelden.</span><span class="sxs-lookup"><span data-stu-id="521ce-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="521ce-112">Im HQ-Client auf der Seite **Alle Kunden** suchen und wählen Sie einen Kunden aus.</span><span class="sxs-lookup"><span data-stu-id="521ce-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="521ce-113">Auf der Kundendetailseite im Inforegister **Einzelhandel**, im Abschnitt **Privatsphäre** stellen Sie die Option **Webaktivität nicht verfolgen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="521ce-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Datenschutzeinstellungen](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="521ce-115">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="521ce-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="521ce-116">Erfahrung mit modulbasierter Abmeldungs-Erfahrung</span><span class="sxs-lookup"><span data-stu-id="521ce-116">Module-based opt-out experience</span></span>

<span data-ttu-id="521ce-117">Administratoren können authentifizierte Benutzer die Erfassung von Webaktivitätsereignissen selbst deaktivieren lassen.</span><span class="sxs-lookup"><span data-stu-id="521ce-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="521ce-118">Fügen Sie das Benutzer-Deaktivierungsmodul zu den Profilseiten des Kundenkontos hinzu, um diese Deaktivierungsfunktion zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="521ce-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="521ce-119">Benutzerdefinierte Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="521ce-119">Custom extensions</span></span>

<span data-ttu-id="521ce-120">Administratoren können ihre eigenen Erweiterungen erstellen, um das Abmelde-Erlebnis für Benutzer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="521ce-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="521ce-121">Weitere Informationen finden Sie unter [Rufen Sie die Retail Server APIs auf](e-commerce-extensibility/call-retail-server-apis.md) und [Online-Kanal-Erweiterbarkeit](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="521ce-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]