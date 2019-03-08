---
title: Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren
description: Diese Prozedur zeigt, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei über die ISO2022 Kreditübertragung erstellen.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "340544"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="e5e63-103">Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren</span><span class="sxs-lookup"><span data-stu-id="e5e63-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5e63-104">Dieses Thema erläutert, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei mit dem Beispiel zur ISO2022-Banküberweisung erstellen.</span><span class="sxs-lookup"><span data-stu-id="e5e63-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="e5e63-105">Dies ist der fünfte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="e5e63-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="e5e63-106">Verwenden Sie die Demodaten DEMF, um dieses Beispiel abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e5e63-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="e5e63-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e5e63-107">Example</span></span>

1.  <span data-ttu-id="e5e63-108">Gehen Sie zu **Kreditorenkonten > Zahlungen > Zahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="e5e63-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-109">Click **New**.</span></span>
3.  <span data-ttu-id="e5e63-110">Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e5e63-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="e5e63-111">Klicken Sie auf **Positionen > Zahlungsvorschlag > Zahlungsvorschlag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="e5e63-112">Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="e5e63-113">Klicken Sie auf **Filter**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="e5e63-114">In der Liste wählen Sie die Zeile für **Kreditorentabelle** und **Kreditorenkonto-Feld** aus.</span><span class="sxs-lookup"><span data-stu-id="e5e63-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="e5e63-115">Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e5e63-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="e5e63-116">Sie können alle beliebigen Kriterien für die Auswahl von Kreditorenbuchungen anwenden. In diesem Beispiel verwenden Sie DE-001 als Kreditorenkonto.</span><span class="sxs-lookup"><span data-stu-id="e5e63-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="e5e63-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-117">Click **OK**.</span></span>
13. <span data-ttu-id="e5e63-118">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-118">Click **OK**.</span></span>
14. <span data-ttu-id="e5e63-119">Klicken Sie auf **Zahlungen erstellen**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="e5e63-120">Generieren Sie eine ISO20022-Zahlungsdatei.</span><span class="sxs-lookup"><span data-stu-id="e5e63-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="e5e63-121">Klicken Sie auf **Zahlungen generieren**.</span><span class="sxs-lookup"><span data-stu-id="e5e63-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="e5e63-122">Geben Sie im Feld **Zahlungsmethode** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e5e63-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="e5e63-123">Geben Sie im Feld **Dateiname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e5e63-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="e5e63-124">In vorliegenden Beispiel ist die generierte Datei aufgrund der EUR-Zahlung SEPA-konform.</span><span class="sxs-lookup"><span data-stu-id="e5e63-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="e5e63-125">Die ISO20022-Banküberweisung und andere Kreditorenzahlungsformate können ebenfalls zum Generieren von Zahlungen in anderen Währungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5e63-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="e5e63-126">Geben Sie im Feld **Bankkonto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e5e63-126">In the **Bank account** field, enter or select a value.</span></span>

