---
title: TDS-Parameter für Kreditoren- und Debitorenkonten einrichten
description: In diesem Thema wird erklärt, wie Sie Parameter in Kreditoren- und Debitorenkonten festlegen, um Abzüge aus der Quellenbesteuerung (TDS) zu unterstützen.
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023268"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="9cc1c-103">TDS-Parameter für Kreditoren- und Debitorenkonten einrichten</span><span class="sxs-lookup"><span data-stu-id="9cc1c-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cc1c-104">In diesem Thema wird erklärt, wie Sie Parameter in Kreditoren- und Debitorenkonten festlegen, um Abzüge aus der Quellenbesteuerung (TDS) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="9cc1c-105">Gehen Sie zu **Steuern \> Setup \> Parameter \> Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="9cc1c-106">Wählen Sie in der Registerkarte **Aktualisierungen** **Auftragspositionen aktualisieren**, um das Dialogfeld **Auftragspositionen aktualisieren** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="9cc1c-107">Geben Sie im Abschnitt **TDS-Gruppe** im Feld **TDS-Gruppe aktualisieren** die Methode an, mit der die TDS-Gruppe auf Positionsebene aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="9cc1c-108">Diese Einstellung wird verwendet, wenn die TDS-Gruppe in einer Auftragskopfzeile aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="9cc1c-109">Die folgenden Optionen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="9cc1c-109">The following options are available:</span></span>

    - <span data-ttu-id="9cc1c-110">**Nie**: Die TDS-Gruppe wird in den Auftragspositionen nicht aktualisiert, wenn sie in der Auftragskopfzeile aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="9cc1c-111">**Immer**: Die TDS-Gruppe wird automatisch in den Auftragspositionen aktualisiert, wenn sie in der Auftragskopfzeile aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="9cc1c-112">**Eingabeaufforderung**: Benutzer erhalten eine Nachricht, die sie auffordert, die TDS-Gruppe in den Auftragspositionen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="9cc1c-113">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-113">Select **OK**.</span></span>

    <span data-ttu-id="9cc1c-114">[![Dialogfeld „Auftragspositionen aktualisieren“](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="9cc1c-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="9cc1c-115">Gehen Sie zu **Steuern \> Setup \> Parameter \> Kreditorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="9cc1c-116">Stellen Sie auf der Registerkarte **Allgemein** im Inforegister **Aufteilung basierend auf Lieferinformationen** die Option **Produktzugang** auf **Ja** ein, um einen Produktzugang mit unterschiedlichen Lieferadressen und Steuerkontonummern (TAN) zu buchen und aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="9cc1c-117">Wenn diese Option auf **Nein** gesetzt ist, können Sie keinen Lieferschein mit unterschiedlichen Lieferadressen und TAN buchen.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="9cc1c-118">Stellen Sie die Option **Rechnung** auf **Ja** um eine Einkaufsrechnung mit unterschiedlichen Lieferadressen und TAN zu buchen und aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="9cc1c-119">[![Inforegister „Aufteilung basierend auf Lieferinformationen“](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="9cc1c-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="9cc1c-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9cc1c-120">Close the page.</span></span>
