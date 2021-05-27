---
title: TaxTrans-Datensatz wird nicht generiert
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die helfen können, wenn ein TaxTrans-Datensatz nicht generiert wird.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018780"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="44f7a-103">TaxTrans-Datensatz wird nicht generiert</span><span class="sxs-lookup"><span data-stu-id="44f7a-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44f7a-104">Wenn Sie **Gebuchte Mehrwertsteuer** für eine Transaktion wählen, aber die Seite **Gebuchte Mehrwertsteuer** entweder keine Steuerzeilen anzeigt oder eine Steuerzeile fehlt, wurde der **TaxTrans** Datensatz möglicherweise nicht erzeugt.</span><span class="sxs-lookup"><span data-stu-id="44f7a-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="44f7a-105">[![Seite „Gebuchte Mehrwertsteuer“, die keine Zeilen enthält](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="44f7a-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="44f7a-106">Um dieses Problem zu beheben, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="44f7a-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="44f7a-107">Prüfen Sie die Mehrwertsteuer, bevor Sie die Transaktion buchen</span><span class="sxs-lookup"><span data-stu-id="44f7a-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="44f7a-108">Bevor Sie die Transaktion buchen, wählen Sie auf der Seite **Rechnung buchen** die Schaltfläche **Mehrwertsteuer**, um die Berechnung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="44f7a-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="44f7a-109">[![Schaltfläche „Mehrwertsteuer“ auf der Seite „Rechnung buchen“](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="44f7a-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="44f7a-110">Prüfen Sie auf der Seite **Vorläufige Transaktionen der Mehrwertsteuer** das Ergebnis der Berechnung.</span><span class="sxs-lookup"><span data-stu-id="44f7a-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="44f7a-111">Wenn keine Steuer berechnet wird, siehe [Steuer wird nicht berechnet oder der Steuerbetrag ist Null](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="44f7a-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="44f7a-112">Finden Sie den TaxTrans-Datensatz in allen gebuchten Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="44f7a-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="44f7a-113">Gehen Sie zu **Steuern** \> **Abfragen und Berichte** \> **Umsatzsteuer-Abfragen** > **Umsatzsteuer**.</span><span class="sxs-lookup"><span data-stu-id="44f7a-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="44f7a-114">Wählen Sie in der Spaltenüberschrift **Beleg** das Filtersymbol, um den Datensatz **TaxTrans** zu finden.</span><span class="sxs-lookup"><span data-stu-id="44f7a-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="44f7a-115">Wenn Sie die gesuchten Mehrwertsteuersätze finden, überprüfen Sie das Datum.</span><span class="sxs-lookup"><span data-stu-id="44f7a-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="44f7a-116">Wenn das Datum von dem Datum der Journalüberschrift abweicht, erstellen Sie eine Microsoft-Serviceanfrage für zusätzliche Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="44f7a-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="44f7a-117">[![Veröffentlichte Umsatzsteuer-Seite](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="44f7a-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="44f7a-118">Debuggen, um Details zu prüfen</span><span class="sxs-lookup"><span data-stu-id="44f7a-118">Debug to check details</span></span>

1. <span data-ttu-id="44f7a-119">Informationen darüber, wie Sie Fehler beheben und feststellen können, ob **TmpTaxWorkTrans** und **TaxUncommitted** korrekt erzeugt werden, finden Sie unter [Feldwert in TaxTrans ist falsch](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="44f7a-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="44f7a-120">Wenn **TaxTmpWorkTrans** oder **TaxUncommitted** korrekt generiert wird, fügen Sie einen Haltepunkt bei **TaxPost ::SaveAndPost()** und **Tax ::SaveAndPost** ein, um den Grund zu debuggen, warum **TaxTrans** nicht eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="44f7a-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="44f7a-121">[![Haltepunkte im Code hinzugefügt](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="44f7a-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="44f7a-122">[![Ergebnisse der hinzugefügten Haltepunkte](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="44f7a-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="44f7a-123">Ermitteln Sie, ob eine Anpassung vorliegt</span><span class="sxs-lookup"><span data-stu-id="44f7a-123">Determine whether customization exists</span></span>

<span data-ttu-id="44f7a-124">Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="44f7a-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="44f7a-125">Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.</span><span class="sxs-lookup"><span data-stu-id="44f7a-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
