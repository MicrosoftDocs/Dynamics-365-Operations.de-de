---
title: Berichtigung einer Freitextrechnung
description: In diesem Artikel wird beschrieben, wie eine Freitextrechnung, die gebucht wurde, korrigiert und als korrekte Rechnung erfasst wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c8c1b90b7b2c02a53e53cc13d70445a237b126d4
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="b4ef1-103">Berichtigung einer Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="b4ef1-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4ef1-104">In diesem Artikel wird beschrieben, wie eine Freitextrechnung, die gebucht wurde, korrigiert und als korrekte Rechnung erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="b4ef1-105">Um eine Freitextrechnung zu korrigieren, die bereit gebucht wurde, öffnen Sie die gebuchte Freitextrechnung.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="b4ef1-106">Auf der Seite **Rechnung**  wählen Sie **Abbrechen**, und dann **Rechnung korrigieren**.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="b4ef1-107">Wählen Sie einen Ursachencode aus, und geben Sie Kommentare ein, und wählen Sie Datum für die korrigierte Rechnung ein.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="b4ef1-108">Sie können die berichtigte Rechnung bearbeiten und buchen.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="b4ef1-109">Wenn Sie die berichtigte Rechnung buchen, wird eine Stornorechnung für einen Habenbetrag erstellt, der mit dem ursprünglichen Rechnungsbetrag übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="b4ef1-110">Dadurch wird der kombinierte Saldo der ursprünglichen Rechnung und der Stornierung auf 0 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="b4ef1-111">Die Stornorechnung wird mit der ursprünglichen Rechnung ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="b4ef1-112">Nachdem Sie die berichtigte Rechnung buchen, haben Sie drei Rechnungen:</span><span class="sxs-lookup"><span data-stu-id="b4ef1-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="b4ef1-113">**Ursprüngliche Rechnung** – Die Rechnung mit den zu korrigierenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="b4ef1-114">**Stornorechnung** – Die vom System generierte Ausgleichsrechnung, die zur Stornierung der zuletzt berichtigten Rechnung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="b4ef1-115">**Korrigierte Rechnung** – Die Rechnung mit den korrigierten Rechnungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="b4ef1-116">Sie können Storno- und Korrekturrechnungen auf zwei Arten identifizieren:</span><span class="sxs-lookup"><span data-stu-id="b4ef1-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="b4ef1-117">Die **Alle Freitextrechnungen**-Seite umfasst eine **Korrektur**-Spalte, in der Sie sehen können, welche Rechnungen Stornorechnungen und berichtigte Rechnungen sind.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="b4ef1-118">Der Kopf der Freitextrechnung zeigt den Status **Rechnung stornieren**\[Rechnungsnummer\]oder**korrekte Rechnungsnummer '\[Rechnungsnummer\]'**.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="b4ef1-119">Diese Funktion ist nur verfügbar, wenn der Konfigurarionsschlüsse **Freitext-Rechnungskorrektur** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b4ef1-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>




