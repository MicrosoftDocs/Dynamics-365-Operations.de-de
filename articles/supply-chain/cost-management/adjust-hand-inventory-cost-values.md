---
title: Regulieren der Einstandswerte für verfügbaren Bestand
description: Verwenden Sie die Seite "Anpassung des verfügbaren Lagerbestands", um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nachdem ein Lagerabschlusses durchgeführt wurde.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556114"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="55bd3-103">Regulieren der Einstandswerte für verfügbaren Bestand</span><span class="sxs-lookup"><span data-stu-id="55bd3-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55bd3-104">Verwenden Sie die Seite "Anpassung des verfügbaren Lagerbestands", um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nachdem ein Lagerabschlusses durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="55bd3-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="55bd3-105">Verwenden Sie die Seite **Anpassung des verfügbaren Lagerbestands**, um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nach Ausführung eines Lagerabschlusses.</span><span class="sxs-lookup"><span data-stu-id="55bd3-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="55bd3-106">**Hinweis:** Um die Seite **Anpassung des verfügbaren Lagerbestands** auf der Seite **Abschluss und Regulierung** zu öffnen, wählen Sie den Datensatz eines bereits abgeschlossenen Lagerabschlussprozess aus und klicken Sie anschließend auf **Regulierung** &gt; **Verfügbar**.</span><span class="sxs-lookup"><span data-stu-id="55bd3-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="55bd3-107">**Beispiel:** Im Februar liegen die folgenden Buchungen vor:</span><span class="sxs-lookup"><span data-stu-id="55bd3-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="55bd3-108">1. Februar: Wertmäßiger Lagerzugang für die Menge "2" mit einem Einstandspreis von EUR 10,00</span><span class="sxs-lookup"><span data-stu-id="55bd3-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="55bd3-109">5. Februar: Wertmäßiger Lagerzugang für die Menge "1" mit einem Einstandspreis von EUR 13,00</span><span class="sxs-lookup"><span data-stu-id="55bd3-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="55bd3-110">19. Februar: Wertmäßiger Lagerabgang für die Menge "1" mit einem laufenden Durchschnittseinstandspreis von EUR 11,00</span><span class="sxs-lookup"><span data-stu-id="55bd3-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="55bd3-111">Dieser Artikel wurde mit dem FIFO-Lagermodell (First In, First Out) eingerichtet, und der Lagerabschluss erfolgte am 28. Februar.</span><span class="sxs-lookup"><span data-stu-id="55bd3-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="55bd3-112">Die wertmäßige Abgangsbuchung in Höhe von EUR 11,00 wird mit dem wertmäßigen Zugang vom 1. Februar ausgeglichen, und eine Regulierung von EUR 1,00 wird vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="55bd3-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="55bd3-113">Die folgenden Lagerzugänge enthalten dann offene Lagermengen:</span><span class="sxs-lookup"><span data-stu-id="55bd3-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="55bd3-114">1. Februar: Menge "1" mit einem Einstandspreis von EUR 10,00</span><span class="sxs-lookup"><span data-stu-id="55bd3-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="55bd3-115">5. Februar: Menge "1" mit einem Einstandspreis von EUR 13,00</span><span class="sxs-lookup"><span data-stu-id="55bd3-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="55bd3-116">Verwenden Sie die Option für die Regulierung des verfügbaren Bestands, um die Kosten dieser beiden Artikel auf EUR 15,00 festzulegen, und regulieren Sie die offenen verfügbaren Bestandsmengen zum Datum der letzten Lagerabschlussperiode.</span><span class="sxs-lookup"><span data-stu-id="55bd3-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="55bd3-117">**Hinweis:** Als Buchungsdatum für die Regulierung des verfügbaren Bestands wird das Datum des letzten Lagerabschlusses verwendet.</span><span class="sxs-lookup"><span data-stu-id="55bd3-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="55bd3-118">Dieses Datum kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="55bd3-118">This date can't be modified.</span></span>
