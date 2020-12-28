---
title: Fehlerbehebung bei Teilfreigaben und Teillieferungen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit Teilfreigaben und Teillieferungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645947"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="858b0-103">Fehlerbehebung bei Teilfreigaben und Teillieferungen</span><span class="sxs-lookup"><span data-stu-id="858b0-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="858b0-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit Teilfreigaben und Teillieferungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="858b0-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="858b0-105">Der Freigabestatus eines Verkaufsauftrags bleibt teilweise freigegeben, auch nachdem der Auftrag fakturiert wurde.</span><span class="sxs-lookup"><span data-stu-id="858b0-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="858b0-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="858b0-106">Issue description</span></span>

<span data-ttu-id="858b0-107">Ein Verkaufsauftrag ist ein Lieferauftrag, aber ein oder mehrere Elemente auf ihm haben eine andere Lieferart.</span><span class="sxs-lookup"><span data-stu-id="858b0-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="858b0-108">Nachdem der Auftrag fakturiert wurde, hat er immer noch einen Freigabestatus von *Teilweise freigegeben*.</span><span class="sxs-lookup"><span data-stu-id="858b0-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="858b0-109">Ein Verkaufsauftrag hat z. B. zwei Elemente: eines zur Lieferung und eines zur Abholung.</span><span class="sxs-lookup"><span data-stu-id="858b0-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="858b0-110">Sowohl die Lieferung als auch die Abholung sind erfolgt.</span><span class="sxs-lookup"><span data-stu-id="858b0-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="858b0-111">Daher sind beide Zeilen fakturiert worden.</span><span class="sxs-lookup"><span data-stu-id="858b0-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="858b0-112">Der Freigabestatus wird jedoch immer noch als *Teilweise freigegeben* angezeigt, was irreführend ist.</span><span class="sxs-lookup"><span data-stu-id="858b0-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="858b0-113">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="858b0-113">Issue resolution</span></span>

<span data-ttu-id="858b0-114">Der Freigabestatus gilt nur für Auftragszeilen, bei denen die Elemente für die Lagerortverwaltung freigegeben sind.</span><span class="sxs-lookup"><span data-stu-id="858b0-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="858b0-115">Daher bleibt der Freigabestatus in diesem Szenario *Teilweise freigegeben*.</span><span class="sxs-lookup"><span data-stu-id="858b0-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="858b0-116">Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="858b0-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="858b0-117">Im Rahmen des Lieferschein- und Fakturierungsprozesses könnte eine Erweiterung hinzugefügt werden, um den Freigabestatus zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="858b0-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
