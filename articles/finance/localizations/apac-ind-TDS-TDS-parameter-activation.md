---
title: TDS-Parameter festlegen
description: In diesem Thema wird erklärt, wie Sie Parameter festlegen, um die in bestimmten Buchungen die Funktionalität für die Quellenbesteuerung (TDS) zu aktivieren. Dies ist ein notwendiger Schritt, um die Quellenbesteuerungsfunktion (TDS-Funktion) zu verwenden.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023266"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="d6413-104">TDS-Parameter festlegen</span><span class="sxs-lookup"><span data-stu-id="d6413-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6413-105">In diesem Thema wird erklärt, wie Sie Parameter festlegen, um die in bestimmten Buchungen die Funktionalität für die Quellenbesteuerung (TDS) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d6413-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="d6413-106">Dies ist ein notwendiger Schritt, um die Quellenbesteuerungsfunktion (TDS-Funktion) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6413-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="d6413-107">Wechseln Sie zu **Hauptbuch \> Sachkonto-Einstellungen \> Hauptbuchparameter**.</span><span class="sxs-lookup"><span data-stu-id="d6413-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="d6413-108">Stellen Sie auf der Registerkarte **Direkte Steuern** im Abschnitt **Quellenbesteuerung** die Option **TDS aktivieren** auf **Ja**, um die TDS-Funktionalität und die dafür verwendeten Seiten und Felder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d6413-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="d6413-109">Stellen Sie die Option **Rechnung** auf **Ja**, um die Felder zu aktivieren, mit denen TDS auf Rechnungsebene berechnet und abgezogen werden.</span><span class="sxs-lookup"><span data-stu-id="d6413-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="d6413-110">Stellen Sie die Option **Zahlung** auf **Ja**, um die Felder zu aktivieren, mit denen TDS auf Zahlungsebene berechnet und abgezogen werden.</span><span class="sxs-lookup"><span data-stu-id="d6413-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="d6413-111">[![Registerkarte „Direkte Steuern“](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="d6413-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="d6413-112">Suchen Sie in der Registerkarte **Nummerkreise** die Zeile, bei der das Feld **Referenz** auf **Quellensteuerzahlung** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="d6413-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="d6413-113">Wählen Sie dann im Feld **Nummernkreiscode** der Zeile den Nummernkreiscode aus.</span><span class="sxs-lookup"><span data-stu-id="d6413-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="d6413-114">Der Nummernkreiscode wird verwendet, um Belegnummern für den periodischen TDS-Ausgleichsprozess zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d6413-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6413-115">Um den periodischen TDS-Ausgleichsprozess auszuführen, gehen Sie zu **Steuern \> Erklärung \> Quellensteuer \> Quellensteuerzahlung**.</span><span class="sxs-lookup"><span data-stu-id="d6413-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="d6413-116">[![Registerkarte Nummernkreise](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="d6413-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="d6413-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d6413-117">Close the page.</span></span>
