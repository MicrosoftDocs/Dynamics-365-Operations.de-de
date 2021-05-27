---
title: Zahlungsplänen mit TDS-Zuteilung einrichten
description: In diesem Thema wird erklärt, wie Zahlungspläne mit Zuteilung für die Quellenbesteuerung (TDS) einrichten.
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023276"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="da66a-103">Zahlungsplänen mit TDS-Zuteilung einrichten</span><span class="sxs-lookup"><span data-stu-id="da66a-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da66a-104">In diesem Thema wird erklärt, wie Zahlungspläne mit Zuteilung für die Quellenbesteuerung (TDS) einrichten.</span><span class="sxs-lookup"><span data-stu-id="da66a-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="da66a-105">Gehen Sie zu **Kreditorenkonten \> Zahlungseinstellungen \> Zahlungspläne**.</span><span class="sxs-lookup"><span data-stu-id="da66a-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="da66a-106">[![Seite „Zahlungspläne“](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="da66a-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="da66a-107">Wählen Sie im Aktionsbereich die Option **Neu** aus, um einen Zahlungsplan zu erstellen und die erforderlichen Details einzugeben.</span><span class="sxs-lookup"><span data-stu-id="da66a-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="da66a-108">Wählen Sie im Feld **Zuteilung** die Methode aus, mit der die Zahlung dem Zahlungsplan zugeteilt werden soll:</span><span class="sxs-lookup"><span data-stu-id="da66a-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="da66a-109">Summe</span><span class="sxs-lookup"><span data-stu-id="da66a-109">Total</span></span>
    - <span data-ttu-id="da66a-110">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="da66a-110">Fixed amount</span></span>
    - <span data-ttu-id="da66a-111">Feste Menge</span><span class="sxs-lookup"><span data-stu-id="da66a-111">Fixed quantity</span></span>
    - <span data-ttu-id="da66a-112">Angegeben</span><span class="sxs-lookup"><span data-stu-id="da66a-112">Specified</span></span>

    <span data-ttu-id="da66a-113">Das Feld **Quellensteuerzuteilung** zeigt die TDS-Zuteilungsmethode für den Zahlungsplan.</span><span class="sxs-lookup"><span data-stu-id="da66a-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="da66a-114">Wenn Sie **Gesamt** im Feld **Zuteilung** auswählen, wird die **Quellensteuerzuteilung** automatisch auf **Gesamt** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="da66a-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="da66a-115">Wenn Sie **Fester Betrag**, **Feste Menge** oder **Angegeben** im Feld **Zuteilung** auswählen, wird die **Quellensteuerzuteilung** automatisch auf **Anteilig** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="da66a-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da66a-116">Wenn das Feld **Quellensteuerzuteilung** auf **Gesamt** gesetzt ist, werden die Zahlungsraten auf Grundlage des Bruttobetrags berechnet, der den TDS-Betrag enthält.</span><span class="sxs-lookup"><span data-stu-id="da66a-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="da66a-117">Wenn das Feld **Quellensteuerzuteilung** auf **Anteilig** gesetzt ist, werden die Zahlungsraten auf Grundlage des Nettorechnungsbetrags nach Abzug des TDS-Betrag berechnet.</span><span class="sxs-lookup"><span data-stu-id="da66a-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="da66a-118">Geben Sie im Formular die restlichen erforderlichen Informationen ein und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="da66a-118">Enter the other required details, and then close the page.</span></span>
