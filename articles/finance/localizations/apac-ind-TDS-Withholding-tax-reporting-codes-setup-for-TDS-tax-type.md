---
title: Quellensteuererklärungscodes für den Steuertyp „TDS“ einrichten
description: Quellensteuererklärungscodes werden verwendet, um Erklärungen mit den Formularen 26Q und 27Q für die Quellenbesteuerung (TDS) zu erstellen. In diesem Thema wird erklärt, wie Sie Quellensteuererklärungscodes einrichten, damit Sie TDS-Erklärungscodes einrichten können.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023278"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="71cca-104">Quellensteuererklärungscodes für den Steuertyp „TDS“ einrichten</span><span class="sxs-lookup"><span data-stu-id="71cca-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71cca-105">Quellensteuererklärungscodes werden verwendet, um Erklärungen mit den Formularen 26Q und 27Q für die Quellenbesteuerung (TDS) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="71cca-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="71cca-106">In diesem Thema wird erklärt, wie Sie Quellensteuererklärungscodes einrichten, damit Sie TDS-Erklärungscodes einrichten können.</span><span class="sxs-lookup"><span data-stu-id="71cca-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="71cca-107">Wechseln Sie zu **Setup \> Quellensteuer \> Quellensteuer \> Quellensteuererklärungscodes**.</span><span class="sxs-lookup"><span data-stu-id="71cca-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="71cca-108">[![Seite „Quellensteuererklärungscodes“](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="71cca-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="71cca-109">Wählen Sie im Feld **Steuertyp** **TDS** aus, um Quellensteuererklärungscodes für den Steuertyp „TDS“ festzulegen.</span><span class="sxs-lookup"><span data-stu-id="71cca-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="71cca-110">Wählen Sie im Feld **Quellensteuerkomponente** die TDS-Komponente aus, für die Sie den Quellensteuererklärungscode festlegen.</span><span class="sxs-lookup"><span data-stu-id="71cca-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="71cca-111">Das Feld **Quellensteuerkomponentengruppe** zeigt die TDS-Komponentengruppe an, die für die von Ihnen definierte TDS-Komponente festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="71cca-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="71cca-112">Das Feld **Abschnittscode** im Inforegister **Allgemein** zeigt den Abschnittscode an, der mit der TDS-Komponentengruppe verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="71cca-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="71cca-113">Wählen Sie im Inforegister **Allgemein** im Feld **Berichtscode**, den TDS-Berichtscode aus:</span><span class="sxs-lookup"><span data-stu-id="71cca-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="71cca-114">TDS</span><span class="sxs-lookup"><span data-stu-id="71cca-114">TDS</span></span>
    - <span data-ttu-id="71cca-115">TCS</span><span class="sxs-lookup"><span data-stu-id="71cca-115">TCS</span></span>
    - <span data-ttu-id="71cca-116">Zuschlag</span><span class="sxs-lookup"><span data-stu-id="71cca-116">Surcharge</span></span>
    - <span data-ttu-id="71cca-117">PE\_-Sondersteuer</span><span class="sxs-lookup"><span data-stu-id="71cca-117">PE\_Cess</span></span>
    - <span data-ttu-id="71cca-118">SHE\_-Sondersteuer</span><span class="sxs-lookup"><span data-stu-id="71cca-118">SHE\_Cess</span></span>

5. <span data-ttu-id="71cca-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="71cca-119">Close the page.</span></span>
