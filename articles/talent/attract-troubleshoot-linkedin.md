---
title: 'Problembehandlungsintegration mit LinkedIn und Microsoft Dynamics 365 Talent: Attract'
description: 'In diesem Thema wird erläutert, wie mögliche Probleme behandelt werden, wenn Sie versuchen, Stellen in LinkedIn von Microsoft Dynamics 365 Talent: Attract zu veröffentlichen.'
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ec095642f556b8d0087dd22f35097671a30047a6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461246"
---
# <a name="troubleshoot-integration-with-linkedin-and-attract"></a><span data-ttu-id="54b97-103">Problembehandlungsintegration mit LinkedIn und Microsoft</span><span class="sxs-lookup"><span data-stu-id="54b97-103">Troubleshoot integration with LinkedIn and Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="54b97-104">Verwenden Sie die folgenden Informationen, um Probleme zu beheben, die Sie möglicherweise haben, wenn Sie versuchen, Stellen auf LinkedIn von Microsoft Dynamics 365 Talent: Attract zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="54b97-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="54b97-105">Sie können sich von Attract nicht bei LinkedIn anmelden</span><span class="sxs-lookup"><span data-stu-id="54b97-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="54b97-106">Wenn Sie Schwierigkeiten bei der Anmeldung zu LinkedIn von Attract haben, versuchen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="54b97-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="54b97-107">Überprüfen Sie, dass die LinkedIn Anmeldeinformationen, die Sie in Attract eingegeben haben, gültig und korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="54b97-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="54b97-108">Wenn die Anmeldeinformationen gültig sind und korrekt sind, kontaktieren Sie den [LinkedIn Support](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="54b97-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="54b97-109">Wenn das Problem weiterhin besteht, kontaktieren Sie den [Microsoft Support](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="54b97-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="54b97-110">Stellen von Attract werden nicht auf LinkedIn veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="54b97-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="54b97-111">Wenn Ihre Stelle nicht auf LinkedIn angezeigt wird nach 24 Stunden, versuchen Sie diese Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="54b97-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="54b97-112">Stellen Sie sicher, dass die LinkedIn-Unternehmenskennungszuordnungen korrekt mit Ihrer LinkedIn-Unternehmensseite verknüpft sind und ordnungsgemäß im Attract Admin Center eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="54b97-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="54b97-113">Weitere Informationen dazu, wie LinkedIn-Einstellungen im Admin Center geändert werden, finden Sie unter [Einrichten der Integration mit LinkedIn für Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="54b97-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span></span> <span data-ttu-id="54b97-114">Weitere Informationen zur LinkedIn Unternehmungskennungen, finden Sie unter [Ihre LinkedIn-Unternehmenskennung der LinkedIn-Stellenbörse zuordnen - häufig gestellte Fragen](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="54b97-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="54b97-115">Überprüfen Sie die Stellendetails auf LinkedIn, um zu überprüfen, ob die Adresse abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="54b97-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="54b97-116">Um eine Stelle erfolgreich zu veröffentlichen, muss LinkedIn mindestens den Ort und das Land bzw. die Region der Stelle haben.</span><span class="sxs-lookup"><span data-stu-id="54b97-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="54b97-117">Stellen Sie sicher, dass die Stelle kein Duplikat einer Stelle ist, die bereits auf LinkedIn veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="54b97-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="54b97-118">LinkedIn veröffentlicht keine Stellen, die entweder Duplikate von Premium Stellen oder begrenzten Listen aus einer anderen Quelle sind.</span><span class="sxs-lookup"><span data-stu-id="54b97-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="54b97-119">Überprüfen Sie, ob eine andere Person in Ihrem Unternehmen nicht bereits manuell die Stelle veröffentlicht hat.</span><span class="sxs-lookup"><span data-stu-id="54b97-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="54b97-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54b97-120">See also</span></span>

[<span data-ttu-id="54b97-121">Attract Integration mit LinkedIn FAQ</span><span class="sxs-lookup"><span data-stu-id="54b97-121">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="54b97-122">Veröffentlichen von Stellenausschreibungen auf LinkedIn mit Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="54b97-122">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="54b97-123">Kandidaten mithilfe von LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract anwerben</span><span class="sxs-lookup"><span data-stu-id="54b97-123">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="54b97-124">Erstellen, Genehmigen und Buchen von Aufträgen in Attract</span><span class="sxs-lookup"><span data-stu-id="54b97-124">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="54b97-125">Problembehandlungsintegration mit LinkedIn und Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="54b97-125">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
