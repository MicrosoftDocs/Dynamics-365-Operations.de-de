---
title: Quellensteuerbehörden für den Steuertyp „TDS“ einrichten
description: In diesem Thema wird erklärt, wie die Behörden für die Quellenbesteuerung (TDS) einrichten.
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023260"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="a3347-103">Quellensteuerbehörden für den Steuertyp „TDS“ einrichten</span><span class="sxs-lookup"><span data-stu-id="a3347-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3347-104">In diesem Thema wird erklärt, wie die Behörden für die Quellenbesteuerung (TDS) einrichten.</span><span class="sxs-lookup"><span data-stu-id="a3347-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="a3347-105">Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuerbehörden**.</span><span class="sxs-lookup"><span data-stu-id="a3347-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="a3347-106">[![Seite „Quellensteuerbehörden“](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="a3347-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="a3347-107">Wählen Sie im Feld **Steuertyp** **TDS** aus, um Quellensteuerbehörden für den Steuertyp „TDS“ einzurichten.</span><span class="sxs-lookup"><span data-stu-id="a3347-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="a3347-108">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3347-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="a3347-109">Geben Sie im Feld **Quellensteuerkomponente** einen Namen für die TDS-Behörde ein.</span><span class="sxs-lookup"><span data-stu-id="a3347-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="a3347-110">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="a3347-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="a3347-111">Wählen Sie im Inforegister **Allgemein** im Feld **Kreditorenkonto** das Kreditorenkonto für die TDS-Behörde aus.</span><span class="sxs-lookup"><span data-stu-id="a3347-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3347-112">Sie müssen den Namen der Bank festlegen, bei der Gelder, die dem TDS-Behördekreditor geschuldet werden, eingezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="a3347-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="a3347-113">Der Name der Bank wird auf der Seite **Bankkonten** festgelegt (**Kreditorenkonten \> Alle Kreditoren \> Kreditoren \> Einrichten \> Bankkonten**).</span><span class="sxs-lookup"><span data-stu-id="a3347-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="a3347-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a3347-114">Close the page.</span></span>
