---
title: Auftragssperren
description: "Dieses Thema beschreibt das Sperren von Aufträgen mithilfe von Einzelhandel und Handel in Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a><span data-ttu-id="8b438-103">Auftragssperren</span><span class="sxs-lookup"><span data-stu-id="8b438-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="8b438-104">Dieses Thema beschreibt das Sperren von Aufträgen mithilfe von Einzelhandel und Handel in Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="8b438-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="8b438-105">Ein Auftrag kann aus unterschiedlichen Gründen gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="8b438-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="8b438-106">Sie können beispielsweise einen Auftrag sperren, bis eine Debitorenadresse oder eine Zahlungsmethode überprüft werden kann oder bis ein Manager das Kreditlimit des Debitors prüfen kann.</span><span class="sxs-lookup"><span data-stu-id="8b438-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="8b438-107">Während des Verkaufsprozesses kann es vorkommen, dass Aufträge gesperrt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8b438-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="8b438-108">Beispielsweise kann ein Auftrag aufgrund von Problemen bei einer Debitorenzahlung oder eines möglichen Betrugs oder weil ein Manger den Auftrag überprüfen muss, gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="8b438-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="8b438-109">Wenn ein Auftrag gesperrt wird, wird diesem ein Code für Auftragssperren zugewiesen, um die Ursache für die Sperre anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8b438-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="8b438-110">Auftragssperrcodes werden unter **Vertrieb und Marketing** &gt; **Einstellungen** &gt; **Aufträge** &gt; **Auftragssperrcodes** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8b438-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="8b438-111">Ein Auftrag kann zum Zeitpunkt der Auftragserstellung oder später manuell gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="8b438-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="8b438-112">Außerdem kann ein Auftrag basierend auf Betrugsregeln automatisch gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="8b438-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="8b438-113">Während ein Auftrag gesperrt ist, müssen Sie ihn möglicherweise mit weitere Informationen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8b438-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="8b438-114">Vielleicht möchten Sie den Auftrag auschecken, während Sie weiter daran arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8b438-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="8b438-115">Sie können einen Auftrag auschecken, ihn wieder einchecken und sogar das Auschecken von einem anderen Benutzer überschreiben, indem Sie die Workbench Auftragssperre (**Einzelhandel** &gt; **Debitoren** &gt; **Auftragssperren**) verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b438-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="8b438-116">Wenn ein Auftrag abgeschlossen werden kann, müssen Sie die Sperre entfernen, bevor Sie den Bestellvorgang abschließen können.</span><span class="sxs-lookup"><span data-stu-id="8b438-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




