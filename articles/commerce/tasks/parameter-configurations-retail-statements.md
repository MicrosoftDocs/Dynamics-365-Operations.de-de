---
title: Parameter konfigurieren, die Auswirkungen auf Einzelhandelsaufstellungen haben
description: In diesem Thema werden Konfigurationen für Commerce-Parameter demonstriert, die sich darauf auswirken, wie Retail-Anweisungen erstellt und gebucht werden.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140833"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="85445-103">Parameter konfigurieren, die Auswirkungen auf Einzelhandelsaufstellungen haben</span><span class="sxs-lookup"><span data-stu-id="85445-103">Configure parameters that affect retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85445-104">In diesem Thema werden Konfigurationen für Commerce-Parameter demonstriert, die sich darauf auswirken, wie Retail-Anweisungen erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="85445-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="85445-105">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="85445-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="85445-106">Gehen Sie im Navigationsbereich zu **Module > Retail and Commerce > Hauptsitz-Setup > Parameter > Commerceparameter**.</span><span class="sxs-lookup"><span data-stu-id="85445-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="85445-107">Wählen Sie die Registerkarte **Buchung**.</span><span class="sxs-lookup"><span data-stu-id="85445-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="85445-108">Wählen Sie **Ja**, wenn Sie die periodischen Rabattbeträge gezielt buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="85445-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="85445-109">Wählen Sie **Standard**, um Standardkonten zu verwenden, oder wählen Sie **Periodisch**, wenn Sie festlegen möchten, welches Konto für jeden periodischen Rabatt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85445-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="85445-110">Wählen Sie **Zusammenfassung**, wenn die Bestandszeilen nach Möglichkeit aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85445-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="85445-111">Wählen Sie **Ja**, wenn Rechnungen und Zahlungen im Rahmen der Rechnungsbuchung automatisch abgerechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85445-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="85445-112">Wählen Sie **Ja**, wenn sichere Drop-Transaktionen aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85445-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="85445-113">Wählen Sie **Ja**, wenn Bank-Drop-Transaktionen aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85445-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="85445-114">Wählen Sie **Ja**, um die Aggregation für die Auszugsbuchung einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="85445-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="85445-115">Wählen Sie **Ja**, um beim Buchen von Bescheinigungen Aufträge anzulegen und parallel zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="85445-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="85445-116">Geben Sie die Höchstmenge der Aufträge ein, die in jeder Stapelverarbeitungsaufgabe bearbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85445-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="85445-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="85445-117">Select **Save**.</span></span>

