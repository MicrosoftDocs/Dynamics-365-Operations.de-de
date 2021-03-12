---
title: Budgetvorschläge aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Budgetvorschlag“ in Finance Insights aktivieren.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995139"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="2dec7-103">Budgetvorschläge aktivieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="2dec7-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2dec7-104">In diesem Thema wird erläutert, wie Sie die Funktion „Budgetvorschlag“ in Finance Insights aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2dec7-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="2dec7-105">Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2dec7-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="2dec7-106">Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2dec7-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="2dec7-107">(Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)</span><span class="sxs-lookup"><span data-stu-id="2dec7-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="2dec7-108">Wenn es sich bei Ihrer Bereitstellung von Microsoft Dynamics 365 Finance um eine Service Fabric-Bereitstellung handelt, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="2dec7-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="2dec7-109">Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="2dec7-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="2dec7-110">Wenn Sie die Funktion im **Funktionsverwaltung**-Arbeitsbereich nicht sehen oder wenn beim Versuch, ihn einzuschalten, Probleme auftreten, senden Sie eine E-Mail an das [Finance Insights App Preview-Team](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="2dec7-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="2dec7-111">Öffnen Sie den **Funktionsverwaltung**-Arbeitsbereich, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="2dec7-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="2dec7-112">Wählen Sie **Nach Updates suchen**.</span><span class="sxs-lookup"><span data-stu-id="2dec7-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="2dec7-113">Suchen Sie nach **Budgetvorschlag** und aktivieren Sie diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="2dec7-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="2dec7-114">Gehen Sie zu **Budgetierung \> Einrichten \> Grundlegende Budgetierung \> Budgetvorschlag (Vorschau)** und wählen Sie **Funktion aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="2dec7-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="2dec7-115">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="2dec7-115">Privacy notice</span></span>
<span data-ttu-id="2dec7-116">Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.</span><span class="sxs-lookup"><span data-stu-id="2dec7-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
