---
title: Retail-Parameter konfigurieren, die Auswirkungen auf Einzelhandelsaufstellungen haben
description: In diesem Thema werden Konfigurationen für Retail-Parameter demonstriert, die sich darauf auswirken, wie Retail-Anweisungen erstellt und gebucht werden.
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
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867270"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="7ec3e-103">Retail-Parameter konfigurieren, die Auswirkungen auf Einzelhandelsaufstellungen haben</span><span class="sxs-lookup"><span data-stu-id="7ec3e-103">Configure Retail parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7ec3e-104">In diesem Thema werden Konfigurationen für Retail-Parameter demonstriert, die sich darauf auswirken, wie Retail-Anweisungen erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-104">This topic demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="7ec3e-105">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="7ec3e-106">Gehen Sie im Navigationsbereich zu **Module > Retail and Commerce > Hauptsitz-Setup > Parameter > Einzelhandelsparameter**.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-106">In the navigation pane, go to **Modules > Retail and commerce > Headquarters setup  > Parameters > Retail parameters**.</span></span>
2. <span data-ttu-id="7ec3e-107">Wählen Sie die Registerkarte **Buchung**.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="7ec3e-108">Wählen Sie **Ja**, wenn Sie die periodischen Rabattbeträge gezielt buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="7ec3e-109">Wählen Sie **Standard**, um Standardkonten zu verwenden, oder wählen Sie **Periodisch**, wenn Sie festlegen möchten, welches Konto für jeden periodischen Rabatt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="7ec3e-110">Wählen Sie **Zusammenfassung**, wenn die Bestandszeilen nach Möglichkeit aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="7ec3e-111">Wählen Sie **Ja**, wenn Rechnungen und Zahlungen im Rahmen der Rechnungsbuchung automatisch abgerechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="7ec3e-112">Wählen Sie **Ja**, wenn sichere Drop-Transaktionen aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="7ec3e-113">Wählen Sie **Ja**, wenn Bank-Drop-Transaktionen aggregiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="7ec3e-114">Wählen Sie **Ja**, um die Aggregation für die Auszugsbuchung einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="7ec3e-115">Wählen Sie **Ja**, um beim Buchen von Bescheinigungen Aufträge anzulegen und parallel zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="7ec3e-116">Geben Sie die Höchstmenge der Aufträge ein, die in jeder Stapelverarbeitungsaufgabe bearbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="7ec3e-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7ec3e-117">Select **Save**.</span></span>

