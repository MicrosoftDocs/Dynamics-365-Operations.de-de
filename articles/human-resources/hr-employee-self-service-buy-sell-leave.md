---
title: Urlaub kaufen und verkaufen
description: In Dynamics 365 Human Resources können Sie Anfragen zum Kauf und Verkauf von Urlaub auf der Grundlage der von Ihrem Unternehmen eingerichteten Richtlinien für den Kauf und Verkauf von Urlaub stellen.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271483"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="89cec-103">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="89cec-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="89cec-104">In Dynamics 365 Human Resources können Sie Anfragen zum Kauf und Verkauf von Urlaub auf der Grundlage der von Ihrem Unternehmen eingerichteten Richtlinien für den Kauf und Verkauf von Urlaub stellen.</span><span class="sxs-lookup"><span data-stu-id="89cec-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="89cec-105">Antrag auf Urlaub kaufen</span><span class="sxs-lookup"><span data-stu-id="89cec-105">Request to buy leave</span></span>

1. <span data-ttu-id="89cec-106">In dem **Mitarbeiter Selbstservice** Arbeitsbereich wählen Sie **Antrag auf Urlaub kaufen** in der Kachel **Freizeitguthaben**.</span><span class="sxs-lookup"><span data-stu-id="89cec-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="89cec-107">Fügen Sie **Urlaubstyp** hinzu und geben Sie einen **Menge** für die Menge an Urlaub ein, die Sie kaufen möchten.</span><span class="sxs-lookup"><span data-stu-id="89cec-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="89cec-108">Wählen **einreichen**, wenn Sie bereit sind, Ihre Anfrage einzureichen.</span><span class="sxs-lookup"><span data-stu-id="89cec-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="89cec-109">Ihre Guthaben werden entweder automatisch aktualisiert oder durchlaufen vor der Aktualisierung einen Genehmigungsprozess.</span><span class="sxs-lookup"><span data-stu-id="89cec-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="89cec-110">Dies hängt davon ab, wie die Kaufrichtlinie konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="89cec-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="89cec-111">Antrag, Urlaub zu verkaufen</span><span class="sxs-lookup"><span data-stu-id="89cec-111">Request to sell leave</span></span>

1. <span data-ttu-id="89cec-112">Wählen Sie im Arbeitsbereich **Employee Self-Service** die Option **Urlaubsanforderung verkaufen** in der Kachel **Salden arbeitsfreier Zeiten**.</span><span class="sxs-lookup"><span data-stu-id="89cec-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="89cec-113">Fügen Sie einen **Urlaubstyp** hinzu und geben Sie eine **Menge** für die Menge an Urlaub ein, die Sie verkaufen möchten.</span><span class="sxs-lookup"><span data-stu-id="89cec-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="89cec-114">Wählen **einreichen**, wenn Sie bereit sind, Ihre Anfrage einzureichen.</span><span class="sxs-lookup"><span data-stu-id="89cec-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="89cec-115">Ihre Guthaben werden entweder automatisch aktualisiert oder durchlaufen vor der Aktualisierung einen Genehmigungsprozess.</span><span class="sxs-lookup"><span data-stu-id="89cec-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="89cec-116">Dies hängt davon ab, wie die Kaufrichtlinie konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="89cec-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="89cec-117">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="89cec-117">Troubleshooting</span></span> 

<span data-ttu-id="89cec-118">Wenn ein Workflow für eine Kauf- oder Verkaufsabwesenheitsanforderung fehlschlägt, können Benutzer mit der Berechtigung **EssLeaveBuySellRequestApprover** das Nachrichtenprotokoll für alle Kauf- und Verkaufsabwesenheitsanforderungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="89cec-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="89cec-119">Gehen Sie dazu auf **Urlaub und Abwesenheit > Link > Urlaubskäufe und -verkäufe > Meldungsprotokoll** (links oben).</span><span class="sxs-lookup"><span data-stu-id="89cec-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="89cec-120">Das **Meldungsprotokoll** zeigt dem Benutzer, wie die Transaktionen verarbeitet wurden und die dazugehörige Workflow-Historie.</span><span class="sxs-lookup"><span data-stu-id="89cec-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="89cec-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89cec-121">See also</span></span>

[<span data-ttu-id="89cec-122">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="89cec-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="89cec-123">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="89cec-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
