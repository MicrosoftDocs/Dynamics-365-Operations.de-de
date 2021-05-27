---
title: Funktionalität zum Teilen von Rechnungen
description: Dieses Thema beschreibt das Setup und die Funktionalität zum Teilen von Rechnungen nach Lieferadresse und Steuerkontonummer (TAN).
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023273"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="6c271-103">Funktionalität zum Teilen von Rechnungen</span><span class="sxs-lookup"><span data-stu-id="6c271-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c271-104">Dieses Thema beschreibt das Setup und die Funktionalität zum Teilen von Rechnungen nach Lieferadresse und Steuerkontonummer (TAN).</span><span class="sxs-lookup"><span data-stu-id="6c271-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="6c271-105">Wählen Sie auf der Seite **Kreditorenbuchhaltungsparameter** auf der Registerkarte **Allgemein** **Produktzugang** oder **Rechnung** aus, um einen Produktzugang oder eine Rechnung mit unterschiedlichen Lieferadressen und TAN auf der Seite **Bestellung** zu buchen und zu teilen.</span><span class="sxs-lookup"><span data-stu-id="6c271-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="6c271-106">Die gebuchte Rechnung wird dann nach Lieferadresse und TAN aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="6c271-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="6c271-107">Legen Sie auf der Registerkarte **Sammelaktualisierung** unter dem Inforegister **Aufteilung basierend auf** in der Reihe **Lieferinformationen** die Option **Bestätigung**, **Kommissionierliste**, **Lieferschein** oder **Rechnung** auf **Ja**, um eine Bestätigung, Kommissionierliste, einen Lieferschein oder eine Rechnung zu buchen und aufzuteilen, in denen unterschiedliche Lieferadressen und TAN für unterschiedliche Rechnungspositionen auf der Seite **Auftrag** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6c271-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="6c271-108">Die Rechnung wird dann zuerst nach Lieferadresse und dann nach TAN aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="6c271-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="6c271-109">Wenn keine Optionen für **Lieferinformationen** auf **Ja** festgelegt sind, wird die Rechnung als Einzelrechnung gebucht.</span><span class="sxs-lookup"><span data-stu-id="6c271-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="6c271-110">Es erfolgt keine Rechnungsaufteilung.</span><span class="sxs-lookup"><span data-stu-id="6c271-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="6c271-111">Um einen Lieferschein zu teilen und zu buchen, bei dem die Rechnungspositionen unterschiedliche Lieferadressen und TAN haben, müssen Sie die Option **Lieferschein** für **Lieferinformationen** auf **Ja** setzen.</span><span class="sxs-lookup"><span data-stu-id="6c271-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="6c271-112">Um eine Rechnung zu teilen und zu buchen, bei der die Rechnungspositionen unterschiedliche Lieferadressen und TAN haben, müssen Sie die Option **Rechnung** für **Lieferinformationen** auf **Ja** setzen.</span><span class="sxs-lookup"><span data-stu-id="6c271-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="6c271-113">Um eine Rechnung zu teilen, bei der die Rechnungspositionen unterschiedliche Lieferadressen, aber die gleiche TAN haben, müssen Sie die Option **Rechnung** für **Lieferinformationen** auf **Nein** setzen.</span><span class="sxs-lookup"><span data-stu-id="6c271-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="6c271-114">Die Rechnung wird dann nach Lieferadresse aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="6c271-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="6c271-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c271-115">Example</span></span>

<span data-ttu-id="6c271-116">In diesem Beispiel ist die Option **Rechnung** für **Lieferinformationen** auf der Registerkarte **Sammelaktualisierung** der Seite **Kreditorenkontenparameter** auf **Ja** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="6c271-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="6c271-117">Es wird eine Einkaufsrechnung mit dem folgenden Setup für Lieferadressen und TAN in den Positionen gebucht:</span><span class="sxs-lookup"><span data-stu-id="6c271-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="6c271-118">**Artikelposition 1:** Lieferadresse 1, TAN ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="6c271-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="6c271-119">**Artikelposition 2:** Lieferadresse 1, TAN ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="6c271-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="6c271-120">**Artikelposition 3:** Lieferadresse 2, TAN ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="6c271-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="6c271-121">**Artikelposition 4:** Lieferadresse 3, TAN ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="6c271-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="6c271-122">In diesem Fall wird die Originalrechnung in zwei Rechnungen aufgeteilt und folgendermaßen gebucht:</span><span class="sxs-lookup"><span data-stu-id="6c271-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="6c271-123">Rechnung 1 wird für Artikelposition 1 und 2 gebucht, da beide Positionen dieselbe Lieferadresse und TAN haben.</span><span class="sxs-lookup"><span data-stu-id="6c271-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="6c271-124">Rechnung 2 wird für Artikelposition 3 gebucht.</span><span class="sxs-lookup"><span data-stu-id="6c271-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="6c271-125">Rechnung 3 wird für Artikelposition 4 gebucht.</span><span class="sxs-lookup"><span data-stu-id="6c271-125">Invoice 3 is posted for item line 4.</span></span>
